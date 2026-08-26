# Component Responsibilities

<!--
STARTER KIT GUIDANCE — DELETE BEFORE PHASE-GATE SUBMISSION

This file defines the responsibilities and boundaries of the system's major
architectural components.

The goal is to make clear:

- what each component owns;
- what each component does;
- what each component explicitly does NOT own;
- what it depends on;
- what depends on it; and
- where important responsibility boundaries exist.

This is not a class list, package inventory, or source-code directory listing.

Use the same component names used in:

/docs/architecture/architecture.md

Remove instructional comments like this one as you complete the artifact.
-->

## Component Responsibility Matrix

<!--
Replace the sample rows below with your actual major components.

Component:
Use the authoritative architectural component name.

Primary Responsibilities:
Describe what the component is accountable for.

Does Not Own:
Explicitly identify responsibilities that might otherwise be ambiguous.
This helps prevent responsibility leakage and architectural drift.

Depends On:
Identify important architectural dependencies.

Used By:
Identify important consumers.

Related Requirements:
Reference requirements materially served or constrained by the component.
-->

| Component | Primary Responsibilities | Does Not Own | Depends On | Used By | Related Requirements |
|---|---|---|---|---|---|
| Web Client | Present workflow information, collect user input, initiate authorized application actions | Business workflow rules, durable data storage, authentication authority | Application Service | End Users | REQ-001, REQ-002 |
| Application Service | Enforce workflow behavior, coordinate domain operations, apply authorization decisions | User-interface rendering, identity-provider internals, database implementation details | Identity Provider, Persistence Layer | Web Client | REQ-001, REQ-002 |
| Persistence Layer | Provide controlled durable storage and retrieval of application state | Workflow policy, presentation logic, user authentication | Database | Application Service | REQ-001, REQ-002 |
| Identity Provider | Establish authenticated user identity | Application workflow authorization and business rules | External identity infrastructure | Application Service | REQ-001 |

<!--
DELETE THE SAMPLE ROWS ABOVE and replace them with actual project components.

Do not create a component simply because a folder exists in the repository.
Include components that represent meaningful engineering responsibilities or
boundaries.
-->

## Detailed Component Responsibilities

<!--
Use one subsection for each major component when the responsibility matrix
alone is insufficient.

Copy and adapt the following structure as needed:

### Component Name

**Purpose**

Describe why the component exists.

**Owns**

- Responsibility or state owned by this component.

**Does Not Own**

- Responsibility intentionally assigned elsewhere.

**Inputs**

- Important information, commands, events, or requests received.

**Outputs**

- Important responses, events, state changes, or information produced.

**Dependencies**

- Important internal or external dependencies.

**Failure Responsibilities**

Describe what the component is expected to do when a dependency fails,
input is invalid, or the component cannot complete its responsibility.

**Related Evidence**

- Requirements:
- Acceptance Criteria:
- API / Interface Contracts:
- Decisions:
- Tests:

Delete this instructional comment before submission.
-->

### Web Client

<!--
SAMPLE COMPONENT — DELETE OR REPLACE BEFORE SUBMISSION
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
- database access.

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
manufacturing successful state or silently losing user-visible errors.

**Related Evidence**

- Requirements: `REQ-001`, `REQ-002`
- API / Interface Contracts: `API-001`, `API-002`

### Application Service

<!--
SAMPLE COMPONENT — DELETE OR REPLACE BEFORE SUBMISSION
-->

**Purpose**

Coordinate application behavior and enforce workflow-level rules.

**Owns**

- workflow orchestration;
- application-level validation;
- authorization decisions based on trusted identity;
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
DELETE THE SAMPLE COMPONENT SECTIONS ABOVE after creating actual component
descriptions.

You do not need a detailed subsection for every component if the matrix is
sufficient. Use additional detail where boundaries, failure responsibilities,
or ownership would otherwise remain unclear.
-->

## Responsibility Boundaries

<!--
Document boundaries where confusion could create defects or architectural drift.

Questions worth considering:

- Where is input validated?
- Where are authorization decisions made?
- Which component owns authoritative state?
- Who may modify that state?
- Where are business rules enforced?
- Who handles retries or failures?
- Who converts between internal and external representations?
- Who owns audit or logging responsibilities?
- Which component is responsible for transaction boundaries?

Do not answer questions that are irrelevant to your system.

The goal is not to distribute every possible responsibility. The goal is to
make IMPORTANT boundaries explicit.
-->

| Concern | Owning Component | Boundary / Rule |
|---|---|---|
| Workflow rule enforcement | Application Service | User-interface code may guide users but does not establish authoritative workflow validity. |
| Persistent workflow state | Persistence Layer / Database | Application components access durable state through the persistence boundary. |
| User authentication | Identity Provider | Application consumes trusted identity but does not manage user credentials. |

<!--
DELETE THE SAMPLE ROWS ABOVE and replace them with actual project boundaries.
-->

## Shared Responsibilities

<!--
Some engineering concerns legitimately span multiple components.

Examples:

- observability;
- security;
- error handling;
- validation;
- performance;
- logging;
- traceability.

Do not assign a cross-cutting concern vaguely to "everyone."

Identify how responsibility is divided.
-->

| Concern | Components | Responsibility Split |
|---|---|---|
| Security | Web Client, Application Service, Identity Provider | Identity Provider establishes identity; Application Service enforces authorization; Web Client presents permitted actions but is not the authoritative security boundary. |

<!--
DELETE THE SAMPLE ROW ABOVE and replace it with actual shared responsibilities,
or remove this section if no cross-component responsibility needs clarification.
-->

## Component Changes

<!--
Component boundaries may evolve.

When a component is added, removed, split, merged, or given materially
different responsibilities:

1. update this file;
2. update architecture.md;
3. update the architecture diagram;
4. update affected API/interface contracts;
5. record a decision when the change is architecturally significant; and
6. review affected requirements, tests, risks, and operational evidence.

Use the table below for significant changes when appropriate.
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
Before the applicable phase-gate submission:

1. Replace all sample component data.
2. Confirm every listed component exists in the current architecture.
3. Confirm responsibilities agree with architecture.md.
4. Confirm important component interactions agree with api-contracts.md.
5. Review for overlapping, missing, or ambiguous responsibility ownership.
6. Remove instructional HTML comments.

A reviewer should be able to use this file to answer:

"Which component is responsible for this behavior, state, or decision?"
-->
