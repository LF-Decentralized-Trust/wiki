1. [Hyperledger Caliper](index.html)
2. [Hyperledger Caliper](Hyperledger-Caliper_23101442.html)

# Hyperledger Caliper : Caliper Development Plan

Created by qinghui hou, last modified by Attila Klenik on Nov 06, 2019

# Distributed Client Design

## v0.2.0 Caliper-core control flow (master and client processes)

Plant UML source: [caliper-flow.puml](attachments/23101526/23101551.puml)

Sequence diagram (click to enlarge/download):

![](attachments/23101526/23101552.svg?height=400)

## Points of interests/issues

### Processing of round configurations

1. The round entries in the benchmark configuration file are processed both by **caliper-flow** and **default-test**. This is partly because of the convenience array notation in the round configs, but with that, the processing should be performed entirely by **default-test**, which should be renamed to **TestOrchestrator**.
2. The mentioned array notation is rarely used, plus its intended functionality is easy to replicate with YAML anchors. To this end, it should be removed, and one round entry should have exactly one associated rate controller, tx number/duration, etc. This would make the processing easier.

### Separation of concerns

1. The package should be restructured based on what modules are used in the master process and client processes. A **lib/master** and **/lib/worker** directory structure would help (**lib/common** for the reusable modules).
2. Processing of TX result collections is also scattered among multiple modules (like the **\*TxStats** functions on the **Blockchain** base class). Maybe this will be easier to resolve once the observer/monitor/reporter concerns are a bit formalized.

### Inter-process communication

The IPC is all around the **ClientOrchestrator** module. We must hide the actual communication technology from the module. It should only interact with "client handle objects" that map high-level calls (like init, or test) to IPC and wrap the replies with easy-to-manage Promises. Each worker should have a corresponding "handle object" in the master process, that hides the entire IPC. This will make it easy to switch to other messaging libs.

### Observers, monitors, reporters

The above concepts are kind of fuzzy right now, meaning they don't have a well-defined purpose. What kind of data do they need? When do they need it? What output do they produce? Are they present in the master process or in the workers?

These objects occur in both the master and worker processes.

#### **Worker**

The worker process has two parts that process TX data somehow: the Prometheus Pushgateway updates, and the updates sent to the master process. 

- Pushgateway part
  
  - **What kind** of data does it need: aggregated TX data since the last update. So it essentially needs every TX data since the last update (regardless of actually what component does the aggregation)
  - **When** does it need it: the data is aggregated and the output is produced at specified (configurable) intervals
  - **What output** does it produce: pushes the following client-specific metrics (calculated for the current update interval) to the gateway: *caliper\_tps*, *caliper\_latency*, *caliper\_txn\_submit\_rate*, *caliper\_txn\_success*, *caliper\_txn\_failure*, *caliper\_txn\_pending*
  - Remarks:
    
    - Calculated such derived metrics on the Caliper-side is not desirable, Prometheus is probably better at this, plus the users can specify whatever time-window they want.
    - The following *per-client* metrics (i.e., metrics have a *client* label) should suffice for deriving every other metric: *caliper\_txn\_submitted*, *caliper\_txn\_finished{status="success|failed"}*, *caliper\_txn\_e2e\_latency* (histogram/summary). This requires only two counters and a histogram/summary, whose update is trivial, no other calculations are needed.
      
      - **Goodput**: caliper\_tps\_success = rate(sum(caliper\_txn\_finished{status="success"})\[1s])
      - **Failure rate**: caliper\_tps\_failed = rate(sum(caliper\_txn\_finished{status="failed"})\[1s])
      - **Total TPS**: caliper\_tps = rate(sum(caliper\_txn\_finished)\[1s])
      - **Send rate:** caliper\_txn\_send\_rate = rate(sum(caliper\_txn\_submitted)\[1s])
      - **Pending:** caliper\_txn\_pending = sum(caliper\_txn\_submitted) - sum(caliper\_txn\_finished)
    - Additional labels can be used based on the SUT, like channel, chaincode.
- Updates to the master process
  
  - **What kind** of data does it need: aggregated TX data since the last update. So it essentially needs every TX data since the last update (regardless of actually what component does the aggregation)
  - **When** does it need it: the data is aggregated and the output is produced at specified (configurable) intervals
  - **What output** does it produce: sends an inter-process *txUpdate* message to the master process

General remarks for these worker components:

1. Currently, they are mutually exclusive. This restriction can be lifted. For example, if we decide to expose Prometheus metrics the traditional (pull-based) way, we can have two Prometheus-related modules. One exposes Nodejs-related metrics (for profiling), the other pushes business-metrics to a Pushgateway
2. There should be as little metric calculation in the workers as possible. They already have their hands full with high-rate TX generation.
3. A pattern is starting to emerge from the above:
   
   1. Both components "monitor" TXs and do something at some point with the data. Let's dub such a component as **TxObserver**.
   2. Multiple TxObserver could be active at the same time. They need the usual "orchestrator" service, similarly to monitors.
      
      1. This TxObserverDispatch should notify the observers about the following events: a Tx is submitted (submitCallback is called), a Tx is finished (the user callback returned the results). From these two events, the above data can be gathered and maintained
      2. Other life-cycle events should be provided, like round ID, client ID (or even the callback arguments from the benchconfig)

#### **Master Process**

The master process currently contains test observers, monitors, and reporters (currently only the HTML reporter). 

**Test observers**: they report the benchmark progress (and some related metrics) at the configured frequency.

- Null observer: does nothing
- Local observer: 
  
  - **What kind** of data does it need: aggregated TX data sent by the worker processes.
  - **When** does it need it: the data is pulled from the client orchestrator at specified (configurable) intervals
  - **What output** does it produce: logs the current statistics (Round info, submitted, succeeded, failed, pending)
  - Remarks:
    
    - This pull approach has a drawback. The client orchestrator stores the data. It should only orchestrate clients. As soon as an update is available from the client, it should be forwarded (broadcasted) to every observer (could be more than one, why not) and then discarded. Then it's the responsibility of every observer to either store the data, or do incremental aggregation (which shouldn't be hard for basic metrics), or ignore it.
    - The differentiating trait of this reporter, that it relies on worker messages. So "local observer" might not be the most representative name, the direct messaging pattern is still valid in distributed cases.
- Prometheus observer: 
  
  - **What kind** of data does it need: query results from a Prometheus node (that scraped the data from the clients or from a gateway)
  - **When** does it need it: the data is queried at specified (configurable) intervals
  - **What output** does it produce: logs the current statistics (Round info, submitted, succeeded, failed, pending)
  - Remarks:
    
    - A good example for an observer that doesn't need the client orchestrator, yet it's on its API. A TX data update from clients would also be ignored, but it would be a more lightweight dependency than the client orchestrator

General test observer remarks:

1. These modules as of now perform only progress reports and are usually mutually exclusive (although enabling both would be a nice validation of the progress report since they should reflect similar numbers during a round, and definitely should equal at the end of a round).
2. They report data based on some data source (worker messages, Prometheus timelines, etc). If we have multiple TxObservers in the workers, and multiple ProgressReporters in the master process, then data format compatibility might be an issue. The source data should include some correlation ID (i.e., target specifier), for example, the WorkerTxObserver would add the **target: "worker-progress-reporter"** field to its TX updates and ProgressReporters could filter data based on this.

**Monitors:** these modules monitor different resources throughout the benchmark run and aggregate them. They expose different aggregated metrics, usually for each round and for the total benchmark execution. Some require periodic metric scraping (process and container monitoring), while others acquire the metrics at the end of rounds or the benchmark run (like the Prometheus-based monitor). 

Remarks: the monitor "output" format should be unified. Currently, this is almost true, but the report generation, for example, depends on whether Prometheus is used or not.  A unified format would decouple the reporters from the monitors.

**Reporters**: they generate some kind of report usually at the end of the benchmark run. The current reporter prints to the console (and its table format is not really log-friendly) and also generates an HTML report. This could be split into two reporters. The reporters get their data from the monitors (hopefully in a unified format). Pluggable reporters would allow the easy addition of, for example, a Grafana-based (or any other plotting lib-based) reporter, that could visualize time-series data (and ignore the monitor's aggregated data).

## Attachments:

![](images/icons/bullet_blue.gif) [caliper-flow.puml](attachments/23101526/23101551.puml) (application/octet-stream)  
![](images/icons/bullet_blue.gif) [caliper-flow.svg](attachments/23101526/23101552.svg) (image/svg+xml)  
![](images/icons/bullet_blue.gif) [hyperledger-caliper-architecture-vnext-preview.pptx](attachments/23101526/23101558.pptx) (application/vnd.openxmlformats-officedocument.presentationml.presentation)

Document generated by Confluence on Nov 26, 2024 12:37

[Atlassian](http://www.atlassian.com/)
