# Architecture

<!--
STARTER KIT GUIDANCE — DELETE BEFORE PHASE-GATE SUBMISSION

This file is the authoritative system-level description of your architecture.

It should explain:

- what the system is and what surrounds it;
- how the system is structurally organized;
- the major components and their responsibilities;
- important interfaces and dependencies;
- significant constraints and assumptions;
- the current architecture diagram; and
- the significant decisions that shaped the architecture.

At early gates, some architectural elements may still be proposed or
incomplete. State uncertainty explicitly rather than inventing detail.

Do not use this file as a source-code inventory. Focus on meaningful
architectural structure and engineering reasoning.

Remove instructional comments like this one as you complete the artifact.
-->

## System Context

<!--
Describe the system from the outside looking in.

Identify:

- primary users or actors;
- external systems or services;
- important data sources or destinations;
- trust or organizational boundaries when relevant; and
- what is inside versus outside the system being engineered.

Keep this at the SYSTEM level. Detailed component interactions belong later.

Example only — replace with your actual context:

"The Workflow System allows students to submit requests and authorized staff
to review and process them. Users access the system through a web application.
The system relies on an external identity provider for authentication and a
database for persistent workflow records."

Delete this instructional comment before submission.
-->

Describe the system context here.

## Architectural Structure

<!--
Describe the overall architectural approach.

Examples might include:

- layered application;
- client/server;
- modular monolith;
- service-oriented architecture;
- event-driven architecture;
- another justified structure; or
- a combination of patterns.

Do not choose an architectural label merely because it sounds appropriate.
Explain how the actual system is organized.

Consider:

- separation of concerns;
- major execution boundaries;
- data flow;
- control flow;
- state ownership;
- deployment boundaries; and
- major architectural patterns.

If the architecture is still provisional, say so.
-->

Describe the current architectural structure here.

## Major Components and Responsibilities

<!--
Summarize the major architectural components.

Keep this table at a high level. Detailed boundaries and responsibilities
belong in:

/docs/architecture/component-responsibilities.md

Use stable component names consistently across architecture documents,
diagrams, decisions, implementation, and verification.

Replace the sample rows below with your actual architectural components.
-->

| Component | Primary Responsibility | Key Dependencies |
|---|---|---|
| Web Client | Provides the user-facing workflow interface and communicates user actions to the application service. | Application Service |
| Application Service | Enforces application workflows and coordinates domain operations. | Identity Provider, Persistence Layer |
| Persistence Layer | Stores and retrieves durable workflow data. | Database |
| Identity Provider | Authenticates users and provides trusted identity information. | External service |

<!--
DELETE THE SAMPLE ROWS ABOVE and replace them with your actual major
architectural components.

Do not list every class, file, package, or library. A component should
represent a meaningful architectural responsibility or boundary.
-->

## Interfaces and Dependencies

<!--
Describe the important interactions among components and external systems.

Focus on dependencies that matter architecturally.

For each important interaction, consider:

- direction of dependency;
- type of interface;
- data exchanged;
- synchronous versus asynchronous behavior;
- failure behavior;
- trust boundaries;
- security implications; and
- whether a formal contract is required.

Detailed contracts belong in:

/docs/architecture/api-contracts.md
-->

| Source | Target | Interaction | Interface / Protocol | Notes |
|---|---|---|---|---|
| Web Client | Application Service | Submit and retrieve workflow requests | HTTPS / JSON | Authenticated requests |
| Application Service | Identity Provider | Validate user identity | Provider-defined protocol | External dependency |
| Application Service | Persistence Layer | Store and retrieve workflow state | Internal interface | Application-controlled boundary |

<!--
DELETE THE SAMPLE ROWS ABOVE and replace them with actual system interfaces
and dependencies.
-->

## Data and State Ownership

<!--
Identify where important system state is authoritative.

This does not need to become a complete database design.

Consider:

- Which component owns workflow state?
- Where is authoritative persistent data stored?
- Which data is derived or cached?
- Which external systems remain authoritative for information they provide?
- Are multiple components allowed to modify the same state?
- What consistency assumptions exist?

Delete this section if data/state ownership is genuinely not architecturally
significant to your system.
-->

| Data / State | Authoritative Owner | Persistence | Notes |
|---|---|---|---|
| Workflow request | Application Service | Database | Persistence Layer provides durable storage |
| User identity | Identity Provider | External | Application consumes identity but does not own it |

<!--
DELETE THE SAMPLE ROWS ABOVE and replace them with actual system state.
-->

## Constraints and Assumptions

<!--
Record architectural constraints and assumptions that materially influence
the design.

A CONSTRAINT is something the architecture must operate within.

Examples:

- required deployment platform;
- required programming language;
- required external service;
- security requirement;
- institutional technology limitation;
- compatibility requirement.

An ASSUMPTION is something currently being treated as true without sufficient
confirmation.

Do not duplicate detailed assumption tracking here. Reference the authoritative
entry in:

/docs/requirements/assumptions-open-questions.md

Architectural risks should similarly link to the project's risk documentation.
-->

| ID / Reference | Type | Description | Architectural Impact |
|---|---|---|---|
| ASM-001 | Assumption | Users authenticate through an institution-supported identity provider. | Architecture relies on external authentication rather than local credential storage. |

<!--
DELETE THE SAMPLE ROW ABOVE and replace it with actual constraints and
referenced assumptions.
-->

## Architecture Diagram

<!--
Replace this comment with your current architecture diagram.

A diagram should help a reviewer understand structure that is difficult to
communicate through prose alone.

Mermaid is appropriate when useful because GitHub renders Mermaid diagrams.

EXAMPLE ONLY:

```mermaid
flowchart LR
    User[User]
    Web[Web Client]
    App[Application Service]
    Identity[Identity Provider]
    Data[Persistence Layer]
    DB[(Database)]

    User --> Web
    Web --> App
    App --> Identity
    App --> Data
    Data --> DB
