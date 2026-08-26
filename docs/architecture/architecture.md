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

IMPORTANT:

- Text inside HTML comments like this is Starter Kit guidance.
- Delete instructional comments before the applicable phase-gate submission.
- Sample tables and examples are provided only to demonstrate structure.
- Replace all sample project data with your team's actual engineering evidence.
- Do not simply rename the sample components and treat the example as your architecture.
-->

## System Context

<!--
TEAM CONTENT REQUIRED

Describe the system from the outside looking in.

Identify, where relevant:

- primary users or actors;
- external systems or services;
- important data sources or destinations;
- trust or organizational boundaries; and
- what is inside versus outside the system being engineered.

Keep this at the SYSTEM level. Detailed component interactions belong later.

EXAMPLE ONLY — DELETE AND REPLACE:

"The Workflow System allows students to submit requests and authorized staff
to review and process them. Users access the system through a web application.
The system relies on an external identity provider for authentication and a
database for persistent workflow records."

Replace this entire comment with your team's actual system-context description.
-->

## Architectural Structure

<!--
TEAM CONTENT REQUIRED

Describe the overall architectural approach.

Possible structures might include:

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

If the architecture is still provisional, state that explicitly.

Replace this entire comment with your team's actual architectural description.
-->

## Major Components and Responsibilities

<!--
TEAM CONTENT REQUIRED

Summarize the major architectural components.

Keep this table at a high level. More detailed responsibility boundaries
belong in:

/docs/architecture/component-responsibilities.md

Use stable component names consistently across:

- architecture.md;
- component-responsibilities.md;
- api-contracts.md;
- architecture diagrams;
- decision records;
- implementation; and
- verification evidence.

THE ROWS BELOW ARE SAMPLE DATA.
DELETE AND REPLACE THEM WITH YOUR ACTUAL COMPONENTS.
-->

| Component | Primary Responsibility | Key Dependencies |
|---|---|---|
| Web Client | Provides the user-facing workflow interface and communicates user actions to the application service. | Application Service |
| Application Service | Enforces application workflows and coordinates domain operations. | Identity Provider, Persistence Layer |
| Persistence Layer | Stores and retrieves durable workflow data. | Database |
| Identity Provider | Authenticates users and provides trusted identity information. | External service |

<!--
DELETE AND REPLACE ALL SAMPLE ROWS ABOVE.

Do not list every class, file, package, or library.

A component should represent a meaningful architectural responsibility or
boundary.
-->

## Interfaces and Dependencies

<!--
TEAM CONTENT REQUIRED

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
- whether a formal interface contract is required.

Detailed contracts belong in:

/docs/architecture/api-contracts.md

THE ROWS BELOW ARE SAMPLE DATA.
DELETE AND REPLACE THEM WITH YOUR ACTUAL INTERACTIONS.
-->

| Source | Target | Interaction | Interface / Protocol | Notes |
|---|---|---|---|---|
| Web Client | Application Service | Submit and retrieve workflow requests | HTTPS / JSON | Authenticated requests |
| Application Service | Identity Provider | Obtain trusted user identity | Provider-defined protocol | External dependency |
| Application Service | Persistence Layer | Store and retrieve workflow state | Internal interface | Application-controlled boundary |

<!--
DELETE AND REPLACE ALL SAMPLE ROWS ABOVE.
-->

## Data and State Ownership

<!--
TEAM CONTENT REQUIRED WHEN DATA OR STATE OWNERSHIP IS ARCHITECTURALLY SIGNIFICANT

Identify where important system state is authoritative.

This is not intended to become a complete database design.

Consider:

- Which component owns important state?
- Where is authoritative persistent data stored?
- Which data is derived or cached?
- Which external systems remain authoritative for information they provide?
- Which components are permitted to modify important state?
- What consistency assumptions exist?

THE ROWS BELOW ARE SAMPLE DATA.
DELETE AND REPLACE THEM WITH YOUR ACTUAL STATE OWNERSHIP.

If this section is genuinely not useful for your architecture, the team may
remove the section after making that decision.
-->

| Data / State | Authoritative Owner | Persistence | Notes |
|---|---|---|---|
| Workflow request | Application Service | Database | Persistence Layer provides durable storage |
| User identity | Identity Provider | External | Application consumes identity but does not own it |

<!--
DELETE AND REPLACE ALL SAMPLE ROWS ABOVE.
-->

## Constraints and Assumptions

<!--
TEAM CONTENT REQUIRED

Record constraints and assumptions that materially influence the architecture.

A CONSTRAINT is something the architecture must operate within.

Examples may include:

- required deployment platform;
- required programming language;
- required external service;
- security requirement;
- institutional technology limitation; or
- compatibility requirement.

An ASSUMPTION is something currently being treated as true without sufficient
confirmation.

Do not recreate detailed assumption tracking here.

Reference authoritative assumptions in:

/docs/requirements/assumptions-open-questions.md

Similarly, reference risks and decision records rather than duplicating them.

THE ROW BELOW IS SAMPLE DATA.
DELETE AND REPLACE IT WITH ACTUAL PROJECT EVIDENCE.
-->

| ID / Reference | Type | Description | Architectural Impact |
|---|---|---|---|
| ASM-001 | Assumption | Users authenticate through an institution-supported identity provider. | Architecture relies on external authentication rather than local credential storage. |

<!--
DELETE AND REPLACE THE SAMPLE ROW ABOVE.
-->

## Architecture Diagram

<!--
TEAM CONTENT REQUIRED

Replace this comment with your team's current architecture diagram.

A diagram should make important system structure easier to understand than
prose alone.

Mermaid is acceptable because GitHub renders Mermaid diagrams.

EXAMPLE ONLY — DO NOT RETAIN AS YOUR PROJECT ARCHITECTURE:

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
    ```

Your actual diagram should:

- use the same component names as the architecture documentation;
- show important system and external boundaries;
- show meaningful interaction or dependency directions;
- remain understandable without requiring source-code knowledge; and
- remain current when the architecture changes.

DELETE THIS ENTIRE COMMENT and replace it with your actual diagram.
-->

## Architectural Qualities and Tradeoffs

<!--
TEAM CONTENT REQUIRED

Identify qualities that materially influence your architecture.

Examples might include:

- maintainability;
- reliability;
- security;
- testability;
- scalability;
- performance;
- usability;
- recoverability; or
- deployability.

Do not create a generic list of desirable qualities.

Document qualities that actually influenced architectural choices and explain
the consequences or tradeoffs involved.

THE ROW BELOW IS SAMPLE DATA.
DELETE AND REPLACE IT WITH ACTUAL PROJECT EVIDENCE.
-->

| Quality / Concern | Architectural Response | Tradeoff / Consequence |
|---|---|---|
| Maintainability | Separate workflow logic from presentation and persistence responsibilities. | Adds explicit interfaces and some structural overhead. |

<!--
DELETE AND REPLACE THE SAMPLE ROW ABOVE.
-->

## Key Architectural Decisions

<!--
TEAM CONTENT REQUIRED

Summarize significant architectural decisions here without duplicating the
complete decision records.

Reference the authoritative ADR or other decision artifact.

A decision belongs here when it materially shapes the architecture.

If a decision has not yet been made, reference the appropriate open question
rather than pretending the architecture is settled.

THE ROW BELOW IS SAMPLE DATA.
DELETE AND REPLACE IT WITH ACTUAL PROJECT DECISIONS.
-->

| Decision | Summary | Evidence |
|---|---|---|
| ADR-001 | Use a modular application structure for the initial system. | `/docs/decisions/ADR-001.md` |

<!--
DELETE AND REPLACE THE SAMPLE ROW ABOVE.
-->

## Architecture Evolution

<!--
Architecture may evolve as:

- requirements become clearer;
- implementation produces evidence;
- assumptions are validated or invalidated;
- risks are discovered; and
- engineering decisions change.

When the architecture changes materially:

1. update this file;
2. update affected diagrams;
3. update component-responsibilities.md;
4. update api-contracts.md;
5. record significant decisions;
6. review affected requirements and acceptance criteria;
7. review affected risks; and
8. update relevant tests and operational evidence.

Use the table below only for meaningful architectural changes.

A blank table is intentional at project start.
-->

| Effective Gate | Change | Reason | Related Evidence |
|---|---|---|---|
|  |  |  |  |

## Expectations

- Describe the actual architecture rather than an aspirational architecture.
- Use consistent component and interface names across engineering artifacts.
- Keep system context, structure, responsibilities, and dependencies current.
- Maintain a useful architecture diagram.
- Separate requirements from architecture and architecture from low-level implementation detail.
- Reference assumptions, risks, decisions, and contracts rather than unnecessarily duplicating them.
- Make significant architectural tradeoffs explicit.
- Record uncertainty rather than manufacturing architectural certainty.
- Update related engineering evidence when the architecture materially changes.

<!--
FINAL STARTER KIT CHECK — DELETE BEFORE PHASE-GATE SUBMISSION

Before submission:

1. Replace all sample project data.
2. Replace all placeholder sections with actual team content.
3. Confirm component names agree with component-responsibilities.md.
4. Confirm important interfaces agree with api-contracts.md.
5. Confirm decision and assumption references are valid.
6. Confirm the architecture diagram represents the current system.
7. Review the document for stale or contradictory information.
8. Remove all instructional HTML comments.

A reviewer should be able to understand the major system structure and the
engineering reasoning behind it without reading the source code.
-->
