1. [Hyperledger Labs](index.html)
2. [Hyperledger Labs Home](Hyperledger-Labs-Home_20283400.html)
3. [VS Code Plugin for Chaincode Developers](VS-Code-Plugin-for-Chaincode-Developers_20294626.html)
4. [Mentorship Meetings](Mentorship-Meetings_20294627.html)

# Hyperledger Labs : Sample Code - Plugin

Created by Arun .S.M., last modified on Nov 23, 2024

```
import * as vscode from 'vscode';
import { DelveDebugAdapterDescriptorFactory } from './delveDebugAdapterFactory';

export function activate(context: vscode.ExtensionContext) {
    console.log('Hyperledger Chaincode Debugger is active.');

    // Register the debug adapter factory
    context.subscriptions.push(
        vscode.debug.registerDebugAdapterDescriptorFactory('delve', new DelveDebugAdapterDescriptorFactory())
    );

    // Listen for debugging session events
    vscode.debug.onDidStartDebugSession((session) => {
        console.log(`Debugging started: ${session.name}`);
        vscode.window.showInformationMessage(`Debugging started: ${session.name}`);
    });

    vscode.debug.onDidTerminateDebugSession((session) => {
        console.log(`Debugging terminated: ${session.name}`);
        vscode.window.showInformationMessage(`Debugging terminated: ${session.name}`);
    });
}

export function deactivate() {
    console.log('Hyperledger Chaincode Debugger is deactivated.');
}
```

```
import * as vscode from 'vscode';
import { spawn, ChildProcess } from 'child_process';
import * as path from 'path';
import { DelveDebugAdapter } from './delveDebugAdapter';

export class DelveDebugAdapterDescriptorFactory implements vscode.DebugAdapterDescriptorFactory {
    private delveProcess: ChildProcess | undefined;

    createDebugAdapterDescriptor(
        session: vscode.DebugSession
    ): vscode.ProviderResult<vscode.DebugAdapterDescriptor> {
        const config = session.configuration;
        const program = config.program;
        const port = config.port || 2345;

        if (!program) {
            vscode.window.showErrorMessage('No program specified to debug.');
            return;
        }

        // Start Delve as a headless server
        this.delveProcess = spawn('dlv', [
            'debug',
            '--headless',
            `--listen=127.0.0.1:${port}`,
            '--log',
            '--api-version=2',
            program
        ], {
            cwd: path.dirname(program),
            env: process.env
        });

        this.delveProcess.stdout.on('data', (data) => {
            console.log(`Delve: ${data}`);
        });

        this.delveProcess.stderr.on('data', (data) => {
            console.error(`Delve Error: ${data}`);
        });

        this.delveProcess.on('exit', (code) => {
            console.log(`Delve exited with code ${code}`);
        });

        // Return a custom debug adapter to handle requests
        return new DelveDebugAdapter(port, '127.0.0.1');
    }

    dispose() {
        if (this.delveProcess) {
            this.delveProcess.kill();
            this.delveProcess = undefined;
        }
    }
}
```

```
import { DebugSession, InitializedEvent, StoppedEvent, TerminatedEvent } from '@vscode/debugadapter';
import { DebugProtocol } from '@vscode/debugprotocol';
import { Socket } from 'net';

export class DelveDebugAdapter extends DebugSession {
    private socket: Socket;

    constructor(port: number, host: string) {
        super();

        // Connect to the Delve server
        this.socket = new Socket();
        this.socket.connect(port, host, () => {
            console.log('Connected to Delve server');
        });

        this.socket.on('data', (data) => {
            console.log(`Received data from Delve: ${data}`);
        });

        this.socket.on('error', (err) => {
            console.error(`Socket error: ${err.message}`);
        });

        this.socket.on('close', () => {
            console.log('Connection to Delve server closed');
        });
    }

    protected async dispatchRequest(request: DebugProtocol.Request): Promise<void> {
        console.log(`Received request: ${request.command}`);

        switch (request.command) {
            case 'initialize':
                console.log('Debugging session initialized');
                break;

            case 'next':
                console.log('User clicked Step Over');
                break;

            case 'stepIn':
                console.log('User clicked Step In');
                break;

            case 'stepOut':
                console.log('User clicked Step Out');
                break;

            case 'continue':
                console.log('User clicked Continue');
                break;

            case 'pause':
                console.log('User clicked Pause');
                break;

            default:
                console.log(`Unhandled command: ${request.command}`);
        }

        // Forward the request to Delve
        this.socket.write(JSON.stringify(request));
        await super.dispatchRequest(request);
    }

    dispose() {
        this.socket.destroy();
    }
}
```

```
{
  "version": "0.2.0",
  "configurations": [
    {
      "name": "Debug Hyperledger Chaincode (Delve Server)",
      "type": "delve",
      "request": "launch",
      "program": "${workspaceFolder}/path/to/chaincode",
      "port": 2345
    }
  ]
}
```

Document generated by Confluence on Nov 26, 2024 15:09

[Atlassian](http://www.atlassian.com/)
