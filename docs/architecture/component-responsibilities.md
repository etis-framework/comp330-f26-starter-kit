# Component Responsibilities

<!--
STARTER KIT GUIDANCE — DELETE BEFORE PHASE-GATE SUBMISSION

This file defines the responsibilities and boundaries of the system's major
architectural components.

It should make clear:

- what each component owns;
- what each component is responsible for;
- what each component explicitly does NOT own;
- what each component depends on;
- what depends on each component; and
- where important architectural responsibility boundaries exist.

This is NOT a source-code directory, package inventory, class list, or list
of every technical dependency.

Use the same component names used in:

/docs/architecture/architecture.md

IMPORTANT:

- Text inside HTML comments like this is Starter Kit guidance.
- Delete instructional comments before the applicable phase-gate submission.
- Sample rows and sample component descriptions must be replaced with your
  team's actual architecture.
- Do not simply rename the sample components and retain the example design.
-->

## Component Responsibility Matrix

<!--
TEAM CONTENT REQUIRED

Replace the sample rows below with your team's actual major components.

COLUMN GUIDANCE

Component
Use the authoritative architectural component name.

Primary Responsibilities
Describe what the component is accountable for.

Does Not Own
Explicitly identify responsibilities that could otherwise become ambiguous.
This helps prevent responsibility leakage and architectural drift.

Depends On
Identify significant architectural dependencies.

Used By
Identify significant consumers.

Related Requirements
Reference requirements materially implemented, constrained, or supported by
the component.

THE ROWS BELOW ARE SAMPLE DATA.
DELETE AND REPLACE THEM.
-->

| Component | Primary Responsibilities | Does Not Own | Depends On | Used By | Related Requirements |
|---|---|---|---|---|---|
| Web Client | Present workflow information, collect user input, and initiate application actions | Authoritative workflow rules, durable data storage, authentication authority | Application Service | End Users | REQ-001, REQ-002 |
| Application Service | Enforce workflow behavior, coordinate domain operations, and make application-level authorization decisions | User-interface rendering, identity-provider internals, physical database implementation | Identity Provider, Persistence Layer | Web Client | REQ-001, REQ-002 |
| Persistence Layer | Provide controlled durable storage and retrieval of application state | Workflow policy, presentation logic, user authentication | Database | Application Service | REQ-001, REQ-002 |
| Identity Provider | Establish authenticated user identity | Application workflow authorization and business rules | External identity infrastructure | Application Service | REQ-001 |

<!--
DELETE AND REPLACE ALL SAMPLE ROWS ABOVE.

Do not create a component merely because a repository folder or package exists.

A component should represent a meaningful architectural responsibility or
boundary.
-->

## Detailed Component Responsibilities

<!--
TEAM CONTENT REQUIRED WHERE ADDITIONAL DETAIL IS USEFUL

Use one subsection for each major component when the responsibility matrix
alone is not sufficient.

Suggested structure:

### Component Name

**Purpose**

Describe why the component exists.

**Owns**

- Important responsibility or state owned by this component.

**Does Not Own**

- Related responsibility intentionally assigned elsewhere.

**Inputs**

- Important commands, events, requests, or data received.

**Outputs**

- Important responses, events, state changes, or information produced.

**Dependencies**

- Important internal or external dependencies.

**Failure Responsibilities**

Describe what the component is responsible for when:

- input is invalid;
- a dependency fails;
- an operation cannot be completed; or
- another meaningful failure occurs.

**Related Evidence**

- Requirements:
- Acceptance Criteria:
- API / Interface Contracts:
- Decisions:
- Tests:

The two sections below are WORKED EXAMPLES ONLY.

DELETE AND REPLACE THEM WITH ACTUAL COMPONENT DESCRIPTIONS.
-->

### Web Client

<!--
SAMPLE COMPONENT — DELETE AND REPLACE BEFORE SUBMISSION
-->

**Purpose**

Provide the interactive interface through which users access workflow capabilities.

**Owns**

- presentation of workflow information;
- collection of user input;
- client-side interaction state; and
- communication of user-initiated operations to the Application Service.

**Does Not Own**

- authoritative workflow rules;
- durable workflow state;
- authentication authority; or
- direct database access.

**Inputs**

- user actions;
- application responses; and
- authenticated session context.

**Outputs**

- application requests; and
- rendered user-visible state.

**Dependencies**

- Application Service.

**Failure Responsibilities**

The client should present application or connectivity failures without
manufacturing successful state or silently hiding relevant failures.

**Related Evidence**

- Requirements: `REQ-001`, `REQ-002`
- API / Interface Contracts: `API-001`, `API-002`

### Application Service

<!--
SAMPLE COMPONENT — DELETE AND REPLACE BEFORE SUBMISSION
-->

**Purpose**

Coordinate application behavior and enforce workflow-level rules.

**Owns**

- workflow orchestration;
- application-level validation;
- application authorization decisions based on trusted identity;
- coordination of persistence operations; and
- application-level error handling.

**Does Not Own**

- browser presentation;
- external authentication mechanisms; or
- physical database implementation details.

**Inputs**

- authenticated application requests.

**Outputs**

- application responses;
- workflow state changes; and
- persistence operations.

**Dependencies**

- Identity Provider;
- Persistence Layer.

**Failure Responsibilities**

The service must reject invalid or unauthorized operations and must not report
a successful state change when the required operation was not completed.

**Related Evidence**

- Requirements: `REQ-001`, `REQ-002`
- API / Interface Contracts: `API-001`, `API-002`

<!--
DELETE AND REPLACE THE SAMPLE COMPONENT SECTIONS ABOVE.

You do not need a lengthy detailed subsection for every component if the
responsibility matrix already makes the boundary clear.

Use additional detail where ownership, failure behavior, or architectural
boundaries would otherwise remain ambiguous.
-->

## Responsibility Boundaries

<!--
TEAM CONTENT REQUIRED FOR IMPORTANT OR EASILY CONFUSED BOUNDARIES

Document boundaries where ambiguity could create defects or architectural
drift.

Questions to consider where relevant:

- Where is input validated?
- Where are authoritative authorization decisions made?
- Which component owns authoritative state?
- Which components may modify that state?
- Where are business rules enforced?
- Who handles retries or failures?
- Who converts between internal and external representations?
- Who owns audit or logging responsibilities?
- Where are transaction boundaries established?

Do not answer irrelevant questions merely to fill the table.

THE ROWS BELOW ARE SAMPLE DATA.
DELETE AND REPLACE THEM.
-->

| Concern | Owning Component | Boundary / Rule |
|---|---|---|
| Workflow rule enforcement | Application Service | User-interface code may guide users but does not establish authoritative workflow validity. |
| Persistent workflow state | Persistence Layer / Database | Application components access durable state through the persistence boundary. |
| User authentication | Identity Provider | The application consumes trusted identity but does not manage user credentials. |

<!--
DELETE AND REPLACE ALL SAMPLE ROWS ABOVE.
-->

## Shared Responsibilities

<!--
Some concerns legitimately span multiple components.

Examples may include:

- security;
- observability;
- validation;
- error handling;
- performance;
- logging; or
- traceability.

Do not assign an important cross-cutting concern vaguely to "everyone."

Describe how responsibility is divided.

THE ROW BELOW IS SAMPLE DATA.
DELETE AND REPLACE IT.

If this section adds no meaningful information to your architecture, the team
may remove it after making that decision.
-->

| Concern | Components | Responsibility Split |
|---|---|---|
| Security | Web Client, Application Service, Identity Provider | Identity Provider establishes identity; Application Service enforces authorization; Web Client presents permitted actions but is not the authoritative security boundary. |

<!--
DELETE AND REPLACE THE SAMPLE ROW ABOVE.
-->

## Component Changes

<!--
Component boundaries may evolve.

When a component is:

- added;
- removed;
- split;
- merged; or
- given materially different responsibilities;

review and update:

1. this file;
2. architecture.md;
3. the architecture diagram;
4. api-contracts.md;
5. significant decision records;
6. affected requirements and acceptance criteria;
7. tests; and
8. relevant risk or operational evidence.

Use the table below for meaningful changes.

A blank table is intentional at project start.
-->

| Effective Gate | Component | Change | Reason | Related Decision |
|---|---|---|---|---|
|  |  |  |  |  |

## Expectations

- Use the same component names throughout architecture evidence.
- Assign clear primary responsibilities.
- Make important non-responsibilities explicit where ambiguity could matter.
- Identify meaningful architectural dependencies.
- Document important failure responsibilities.
- Link components to relevant requirements and interface contracts.
- Avoid duplicating source-code structure without architectural meaning.
- Avoid vague shared ownership of critical responsibilities.
- Update component boundaries when the architecture changes.

<!--
FINAL STARTER KIT CHECK — DELETE BEFORE PHASE-GATE SUBMISSION

Before submission:

1. Delete and replace all sample component data.
2. Confirm every listed component exists in the current architecture.
3. Confirm component names agree with architecture.md.
4. Confirm interactions agree with api-contracts.md.
5. Review for missing, overlapping, or ambiguous responsibilities.
6. Confirm referenced requirements and contracts exist.
7. Remove all instructional HTML comments.

A reviewer should be able to use this file to answer:

"Which component is responsible for this behavior, state, or architectural
decision?"
-->
