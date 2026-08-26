# API and Interface Contracts

<!--
STARTER KIT GUIDANCE — DELETE BEFORE PHASE-GATE SUBMISSION

This file records significant contracts between architectural components and
between the system and external systems.

"API" does not mean only public HTTP endpoints.

A contract may describe:

- HTTP/REST interactions;
- internal service interfaces;
- events or messages;
- external service integrations;
- command/query boundaries;
- file or data exchange formats; or
- other interactions where both sides need a stable, reviewable agreement.

Do not document every function call.

Document interfaces whose behavior, data, errors, security expectations, or
evolution matter to the architecture.

Use component names consistent with:

/docs/architecture/architecture.md
/docs/architecture/component-responsibilities.md

IMPORTANT:

- Text inside HTML comments like this is Starter Kit guidance.
- Delete instructional comments before the applicable phase-gate submission.
- Sample contracts and sample data must be replaced with your team's actual
  interface contracts.
- Do not simply rename the example endpoints or fields.
-->

## Contract Summary

<!--
TEAM CONTENT REQUIRED

Use unique identifiers in the form:

API-###

Examples:

API-001
API-002
API-003

The API prefix may be used for significant interface contracts even when the
interaction is not HTTP.

If your team adopts another consistent identifier convention, document it and
use it throughout the repository.

Recommended status values:

- Proposed
- Accepted
- Implemented
- Verified
- Changed
- Deprecated
- Removed

THE ROWS BELOW ARE SAMPLE DATA.
DELETE AND REPLACE THEM WITH ACTUAL PROJECT CONTRACTS.
-->

| ID | Consumer | Provider | Purpose | Interface / Protocol | Related Requirements | Status |
|---|---|---|---|---|---|---|
| API-001 | Web Client | Application Service | Submit a new workflow request | HTTPS / JSON | REQ-001 | Proposed |
| API-002 | Web Client | Application Service | Retrieve workflow request status | HTTPS / JSON | REQ-002 | Proposed |
| API-003 | Application Service | Identity Provider | Obtain trusted authenticated identity | Provider-defined authentication protocol | REQ-001 | Proposed |

<!--
DELETE AND REPLACE ALL SAMPLE ROWS ABOVE.
-->

## Detailed Contracts

<!--
TEAM CONTENT REQUIRED FOR SIGNIFICANT CONTRACTS

Use a detailed subsection for each important interface contract.

Suggested structure:

### API-### — Contract Name

**Consumer:**
**Provider:**
**Purpose:**
**Related Requirements:**
**Status:**

#### Interaction

Describe the interaction and its direction.

For HTTP:
- include method and path when known.

For events:
- identify producer, consumer, and event.

For internal interfaces:
- identify the architectural boundary.

#### Request / Input

Describe meaningful input.

Use a table, schema, example, or link to authoritative schema evidence.

#### Response / Output

Describe expected output.

#### Failure Behavior

Describe important failure conditions and how they are represented.

#### Authentication / Authorization

Describe security expectations relevant to the interaction.

#### Contract Rules

Describe important:

- invariants;
- preconditions;
- postconditions;
- idempotency expectations;
- ordering requirements;
- transaction expectations; or
- other behavior both sides must understand.

#### Verification

Reference tests or other evidence demonstrating that the implementation
conforms to the contract.

#### Notes / Open Questions

Reference unresolved questions instead of inventing missing contract details.

The contracts below are WORKED EXAMPLES ONLY.

DELETE AND REPLACE THEM WITH YOUR ACTUAL PROJECT CONTRACTS.
-->

### API-001 — Submit Workflow Request

<!--
SAMPLE CONTRACT — DELETE AND REPLACE BEFORE SUBMISSION
-->

**Consumer:** Web Client  
**Provider:** Application Service  
**Purpose:** Submit a new workflow request for processing.  
**Related Requirements:** `REQ-001`  
**Status:** Proposed

#### Interaction

`POST /api/requests`

The Web Client sends an authenticated request to create a workflow request.

#### Request / Input

| Field | Required | Description |
|---|---|---|
| `requestType` | Yes | Identifies the type of workflow being requested. |
| `description` | Yes | User-provided information required to process the request. |

<!--
THE FIELDS ABOVE ARE SAMPLE DATA.

DELETE AND REPLACE THEM WITH YOUR ACTUAL CONTRACT.

Do not infer project fields merely because they appear in this example.
-->

#### Response / Output

On successful creation, the service returns a representation containing the
new request identifier and current workflow status.

<!--
As the contract matures, document protocol details such as response structures
or status codes when they are actually known.

Do not invent protocol detail simply to make an early artifact look complete.
-->

#### Failure Behavior

The service rejects requests that are invalid or unauthorized and returns
enough structured information for the consumer to distinguish relevant
failure conditions.

#### Authentication / Authorization

The interaction requires an authenticated user.

The Application Service remains responsible for authoritative authorization
decisions.

#### Contract Rules

- A successful response represents a workflow request that was actually created.
- Invalid required input must not create a workflow request.
- The client must not infer success solely from local state.

#### Verification

`AC-REQ-001-01`, `AC-REQ-001-02`

<!--
THE REFERENCES ABOVE ARE SAMPLE DATA.

Replace them with actual verification evidence.

As implementation matures, verification may also reference:

- integration tests;
- contract tests;
- end-to-end tests; or
- other repository-visible evidence.
-->

#### Notes / Open Questions

None currently documented.

---

### API-002 — Retrieve Workflow Status

<!--
SAMPLE CONTRACT — DELETE AND REPLACE BEFORE SUBMISSION
-->

**Consumer:** Web Client  
**Provider:** Application Service  
**Purpose:** Retrieve the current state of a workflow request.  
**Related Requirements:** `REQ-002`  
**Status:** Proposed

#### Interaction

`GET /api/requests/{requestId}`

#### Request / Input

The consumer provides the identifier of the workflow request being retrieved.

#### Response / Output

The service returns the request's current workflow status when the authenticated
user is authorized to view the request.

#### Failure Behavior

The contract must distinguish relevant conditions such as:

- request does not exist;
- caller is not authorized to view the request; and
- service cannot currently complete the operation.

#### Authentication / Authorization

The caller must be authenticated.

The provider determines whether the caller is authorized to view the identified
request.

#### Contract Rules

- A caller must not receive protected request information solely because they know a request identifier.
- Returned status must represent authoritative application state.

#### Verification

`AC-REQ-002-01`

#### Notes / Open Questions

None currently documented.

<!--
DELETE AND REPLACE ALL SAMPLE CONTRACTS ABOVE.

The examples demonstrate the expected structure and level of reasoning.

They do NOT define required behavior for your project.
-->

## Data Contract Guidance

<!--
STARTER KIT GUIDANCE — DELETE BEFORE PHASE-GATE SUBMISSION

Where an interface exchanges structured data, document the contract at an
appropriate level of precision.

Possible approaches include:

- Markdown field tables;
- JSON examples;
- JSON Schema;
- OpenAPI;
- protocol definitions;
- typed interfaces; or
- another repository-visible schema.

Avoid maintaining several independent definitions of the same contract.

If OpenAPI or another machine-readable artifact becomes authoritative, this
file may summarize the architectural contract and link to that source instead
of duplicating every field.

Example:

Authoritative schema:
/openapi/openapi.yaml

Architecture evidence:
This file summarizes the interface and links to the authoritative schema.
-->

## Failure Contracts

<!--
STARTER KIT GUIDANCE — DELETE BEFORE PHASE-GATE SUBMISSION

Failure behavior is part of an interface contract.

Do not define only the successful path.

Consider relevant conditions such as:

- invalid input;
- missing required data;
- unauthorized access;
- forbidden operations;
- missing resources;
- duplicate requests;
- dependency failures;
- timeout;
- concurrency conflicts;
- unavailable services; or
- partial completion.

Not every contract needs every failure condition.

Document failures consumers need to understand or that materially affect
system behavior.
-->

## Security Boundaries

<!--
STARTER KIT GUIDANCE — DELETE BEFORE PHASE-GATE SUBMISSION

For contracts crossing trust boundaries, consider:

- authentication;
- authorization;
- confidentiality;
- integrity;
- input validation;
- secret handling;
- sensitive-data exposure;
- least privilege;
- replay behavior; and
- duplicate-operation concerns.

Do not rely on a user interface to enforce an authoritative security rule.

Reference authoritative security requirements or decisions rather than
unnecessarily duplicating them.
-->

## Contract Compatibility and Change

<!--
STARTER KIT GUIDANCE — DELETE BEFORE PHASE-GATE SUBMISSION

An interface change may affect multiple components.

Before materially changing an accepted contract:

1. identify consumers;
2. identify affected requirements and acceptance criteria;
3. determine compatibility impact;
4. update provider and consumer evidence;
5. update tests;
6. record a significant architectural decision when appropriate; and
7. preserve enough history to understand the change.

Do not silently change one side of a contract while leaving the other side
documented against an older interface.

The blank table below is intentional at project start.
-->

| Effective Gate | Contract | Change | Compatibility Impact | Related Evidence |
|---|---|---|---|---|
|  |  |  |  |  |

## Verification and Traceability

<!--
STARTER KIT GUIDANCE — DELETE BEFORE PHASE-GATE SUBMISSION

Important contracts should become traceable to implementation and verification.

A useful evidence chain may look like:

REQ-001
  ->
AC-REQ-001-01
  ->
API-001
  ->
Provider implementation
  ->
Consumer implementation
  ->
Contract or integration test

The exact chain will evolve as the project matures.

Do not claim that a contract is Verified until appropriate evidence exists.
-->

## Expectations

- Use stable identifiers for significant interface contracts.
- Use component names consistent with the architecture.
- Identify both consumer and provider.
- Describe meaningful input and output behavior.
- Document important failure behavior.
- Make security expectations explicit where relevant.
- Link contracts to requirements and acceptance criteria.
- Reference authoritative schemas rather than creating unnecessary duplicate definitions.
- Update both sides of a contract when it changes.
- Add verification evidence as implementation matures.
- Record unresolved behavior explicitly rather than inventing contract details.

<!--
FINAL STARTER KIT CHECK — DELETE BEFORE PHASE-GATE SUBMISSION

Before submission:

1. Delete and replace all sample contracts and sample data.
2. Confirm every retained contract represents an actual architectural interface.
3. Confirm consumer and provider names agree with component-responsibilities.md.
4. Confirm component names agree with architecture.md.
5. Confirm requirement and acceptance-criteria references are valid.
6. Confirm documented interfaces match the current implementation where implementation exists.
7. Confirm important failure and security behavior is represented.
8. Remove all instructional HTML comments.

A reviewer should be able to understand what each side of an important
architectural boundary is entitled to expect from the other.
-->
