1. [Community Events](index.html)
2. [Community Events Home](Community-Events-Home_21790731.html)
3. [Interoperability Event](Interoperability-Event_21793489.html)

# Community Events : Testing Room 1

Created by Helen Garneau, last modified by Simon Nazarenko on Aug 31, 2022

Host: Mike Ebert

# Aries Interop Event

### For Room Hosts:

Reminders: Please record the session

## Targets:

1. RFC 434, 023: Connect using OOB (invitation only) OR connect using OOB (OOB as handshake protocol)
2. OOB Reuse: Connect again using OOB (test connection reuse)
3. RFC 048: Send trust ping (both directions if possible)
4. RFC 557: Request "discover features" using one agent and send disclosure from other agent. Reverse roles if possible.

## Bonus:

5\. RFC 455: Test credential issuance--offer a credential using issuance v. 2 from one agent to the other. Reverse roles if applicable.  
6\. RFC 454: Request credential presentation from an agent holding a known credential (probably what was just issued in step 5). Reverse roles if applicable.  
7\. RFC 183: Revoke the credential from step 5. Reverse roles if possible.

# SESSION 1:

\*\*\*ASK TO RECORD SESSION\*\**

Host: Mike Ebert

Scribe: Simon Nazarenko

## Who participated?

- Name of Participants: Timo Glastra
- Company: Animo

## What did you test?

- Targets:
- - 434 OOB
  - 023 DID Exchange
  - 048 Trust Ping
  - 557 Discover Features
  - OOB Reuse

## Successes?

Was able to successfully connect Proven Issuer to Proven Verifier using connections OOB invitation

Was able to successfully connect Proven Issuer to Proven Verifier using DID exchange OOB invitation

Was able to successfully send a trust ping and receive a response from Proven Issuer to Proven Verifier

Was able to successfully send a discover features request and receive a response from Proven Issuer to Proven Verifier

Was able to successfully create a OOB invitation with ability for connection reuse, but we discovered that the Animo ACA-Py agent is on a different network than the Proven Issuer.

## Issues Identified?

Proven agents have a bug with contacts list state being improperly updated

Between Sessions NOTE: Jimmy Dorsey brought a demo using the VON network; let's find some people for him to talk to and interact with.

# SESSION 2:

\*\*\*ASK TO RECORD SESSION\*\**

Host: Kim Ebert, Mike Ebert

Scribe: Mike Ebert

## Who participated?

- Name of Participants: Timo Glastra
- Company: Animo

## What did you test?

- Targets:
- - 434 OOB
  - OOB Reuse

## Successes?

Was able to successfully connect Proven Issuer with Timo's mobile agent using the OOB invitation (connections v1) without connection reuse set to true

Was able to successfully connect Proven Issuer with Timo's mobile agent using the OOB invitation (connections v1) with connection reuse set to true

After Timo's mobile agent failed to connect using OOB v1.1 (mobile agent) vs OOB v1.0 (Proven issuer agent) he rolled back to use OOB v1.0 and he was able to successfully connect

## Issues Identified?

Was able to successfully connect Proven Issuer with Timo's mobile agent using (using the most recent version of AFJ) the OOB invitation (connections v1) with connection reuse set to true (connection was not reused, instead new connection was created). Timo's agent is using OOB v1.1, Proven is using OOB v1.0

Document generated by Confluence on Nov 26, 2024 16:18

[Atlassian](http://www.atlassian.com/)
