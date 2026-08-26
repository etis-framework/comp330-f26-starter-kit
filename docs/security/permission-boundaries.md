# Permission Boundaries

<!--
STARTER KIT GUIDANCE — DELETE BEFORE PHASE-GATE SUBMISSION

This file documents who or what is permitted to perform important system
actions and where those permissions are authoritatively enforced.

This is broader than:

"Which buttons are visible?"

A user interface may hide an action, but hiding a button is NOT sufficient
authorization if a caller can invoke the underlying operation directly.

This artifact should help answer:

- What actors or roles exist?
- What resources or capabilities can they access?
- Which operations are permitted?
- Which operations are denied?
- What component makes the authoritative authorization decision?
- What ownership or resource-level rules apply?
- What happens when authorization fails?
- How is permission behavior verified?

Use terminology consistent with requirements, architecture, APIs, and
implementation.

IMPORTANT:

- Everything inside HTML comments is Starter Kit guidance.
- Remove ALL instructional comments before the applicable phase-gate submission.
- Examples are guidance only.
- Do not invent roles or permissions that the actual system does not contain.
-->

## Permission Model

<!--
TEAM CONTENT REQUIRED

Describe the overall authorization model.

Possible models may include:

- role-based access control;
- resource ownership;
- explicit permissions;
- attribute-based rules;
- a simple authenticated/unauthenticated boundary;
- a combination.

Do not choose a security acronym merely because it sounds sophisticated.

Explain how YOUR system actually decides whether an operation is allowed.

Replace this comment with the team's actual permission model.
-->

## Actors / Roles

<!--
TEAM CONTENT REQUIRED

Identify actors that have meaningfully different permissions.

Examples might include:

- unauthenticated user;
- student;
- staff reviewer;
- administrator;
- service identity.

Do not create application roles merely to fill the table.

EXAMPLE ONLY:

| Actor / Role | Description | Identity Source | Notes |
|---|---|---|---|
| Student | Authenticated user who owns submitted workflow requests | Identity Provider | Can view own requests only |

DELETE the example and populate actual actors below.
-->

| Actor / Role | Description | Identity Source | Notes |
|---|---|---|---|
|  |  |  |  |

## Permission Matrix

<!--
TEAM CONTENT REQUIRED

Document meaningful authorization rules.

Use:

Allow
Deny
Conditional

where useful.

Resource / Capability
What is being accessed or changed?

Operation
Examples:
- Create
- Read
- Update
- Delete
- Approve
- Submit
- Export
- Administer

Authoritative Enforcement
Identify the component or trusted boundary that makes the authorization
decision.

Condition / Scope
Examples:
- own records only;
- assigned workflow only;
- administrator role required.

Related Evidence
Reference requirements, acceptance criteria, API contracts, or tests.

EXAMPLE ONLY:

| Actor / Role | Resource / Capability | Operation | Permission | Condition / Scope | Authoritative Enforcement | Related Evidence |
|---|---|---|---|---|---|---|
| Student | Workflow Request | Read | Allow | Own requests only | Application Service | REQ-008, AC-REQ-008-01 |

DELETE the example and populate the actual table below.
-->

| Actor / Role | Resource / Capability | Operation | Permission | Condition / Scope | Authoritative Enforcement | Related Evidence |
|---|---|---|---|---|---|---|
|  |  |  |  |  |  |  |

## Resource Ownership Rules

<!--
TEAM CONTENT REQUIRED WHEN RESOURCE-LEVEL AUTHORIZATION EXISTS

Role alone may not be enough.

Example:

Two users may both have the Student role, but one student should not
automatically be allowed to read another student's private request.

Document ownership or resource-level rules explicitly.

EXAMPLE ONLY:

| Resource | Ownership / Scope Rule | Enforcement | Evidence |
|---|---|---|---|
| Workflow Request | Requester may read only records associated with their authenticated identity | Application Service query authorization | AC-REQ-008-02 |

Populate actual rules below.

Remove this section if resource ownership is genuinely irrelevant.
-->

| Resource | Ownership / Scope Rule | Enforcement | Evidence |
|---|---|---|---|
|  |  |  |  |

## Authorization Boundaries

<!--
TEAM CONTENT REQUIRED

Identify where authorization MUST occur.

This helps prevent accidental reliance on an untrusted layer.

Questions to consider:

- Can the UI call an API directly?
- Can a caller bypass client-side restrictions?
- Does an API verify both identity and resource access?
- Are database operations reachable only through authorized application logic?
- Are privileged operations separated from normal-user operations?

EXAMPLE ONLY:

| Boundary | Trusted for Authorization? | Responsibility |
|---|---|---|
| Web Client | No | May hide unavailable actions for usability but does not establish authoritative permission |
| Application Service | Yes | Makes authoritative authorization decisions for workflow operations |

Populate actual boundaries below.
-->

| Boundary | Trusted for Authorization? | Responsibility |
|---|---|---|
|  |  |  |

## Authentication vs. Authorization

<!--
STARTER KIT GUIDANCE — DELETE BEFORE PHASE-GATE SUBMISSION

Authentication answers:

"Who are you?"

Authorization answers:

"Are you allowed to do this?"

A valid login does NOT automatically authorize every application action.

The completed permission model should make this distinction visible through
actual system rules.

Do not leave this instructional comment in the finished artifact.
-->

## Permission Failure Behavior

<!--
TEAM CONTENT REQUIRED

Document what happens when an unauthorized operation is attempted.

Consider:

- response behavior;
- information exposure;
- logging;
- whether the caller can distinguish "not found" from "not authorized";
- whether failed attempts modify state.

Do not expose sensitive information through permission errors.

EXAMPLE ONLY:

| Scenario | Expected Behavior | Evidence |
|---|---|---|
| Student requests another student's private workflow record | Request is denied without returning protected workflow data | AC-REQ-008-02 |

Populate actual failure behavior below.
-->

| Scenario | Expected Behavior | Evidence |
|---|---|---|
|  |  |  |

## Privileged Operations

<!--
TEAM CONTENT REQUIRED WHEN HIGHER-PRIVILEGE OPERATIONS EXIST

Identify operations capable of significant impact.

Examples:

- user administration;
- role changes;
- data deletion;
- workflow override;
- export;
- configuration change.

Consider whether stronger verification, audit evidence, or review is
appropriate.

Do not invent privileged operations that do not exist.
-->

| Operation | Authorized Actor / Role | Additional Condition | Evidence / Audit Expectation |
|---|---|---|---|
|  |  |  |  |

## External Service Permissions

<!--
TEAM CONTENT REQUIRED WHEN EXTERNAL SERVICES OR SERVICE IDENTITIES ARE USED

Applications may have permissions independent of human-user roles.

Examples:

- database identity;
- cloud service identity;
- GitHub integration;
- storage credentials;
- external API token.

Document the permission boundary WITHOUT recording secret values.

Consider least privilege:

Does the service have only the permissions it actually requires?

Populate actual evidence below or remove this section if no external service
permissions matter.
-->

| Service / Identity | Required Permission | Why Needed | How Managed | Limitation / Risk |
|---|---|---|---|---|
|  |  |  |  |  |

## Permission Verification

<!--
TEAM CONTENT REQUIRED

Important permission behavior should be verified.

Testing should include denied operations as well as allowed ones.

Possible evidence:

- automated authorization test;
- integration test using different identities;
- manual verification;
- API contract test;
- code review;
- runtime evidence.

Do not claim authorization is verified merely because the UI does not display
a button.

EXAMPLE ONLY:

| Permission Rule | Verification Method | Result | Evidence |
|---|---|---|---|
| Student cannot view another student's request | Integration test with two authenticated identities | Passed | test reference |

DELETE the example and populate actual evidence below.
-->

| Permission Rule | Verification Method | Result | Evidence |
|---|---|---|---|
|  |  |  |  |

## Open Permission Questions

<!--
TEAM CONTENT REQUIRED

Reference unresolved permission questions maintained in:

/docs/requirements/assumptions-open-questions.md

Do not invent answers simply because this document needs completion.

EXAMPLE ONLY:

| Question Reference | Permission Impact | Needed By |
|---|---|---|
| Q-006 | Determines whether staff can view requests outside assigned workflow | A3 |

Populate actual unresolved questions below.

Remove this section when none remain.
-->

| Question Reference | Permission Impact | Needed By |
|---|---|---|
|  |  |  |

## Permission Changes

<!--
TEAM CONTENT REQUIRED WHEN AUTHORIZATION RULES CHANGE MATERIALLY

Authorization changes can have significant downstream impact.

When permission behavior changes, review:

- requirements;
- acceptance criteria;
- API contracts;
- implementation;
- tests;
- security review;
- release limitations.

Do not silently change permission rules.

A blank table is intentional at project start.
-->

| Date / Gate | Permission Change | Reason | Affected Evidence |
|---|---|---|---|
|  |  |  |  |

<!--
FINAL STARTER KIT CHECK — DELETE BEFORE PHASE-GATE SUBMISSION

Before submission:

1. Define only actors and roles that actually exist.
2. Confirm important actions have explicit permission rules.
3. Identify where authorization is authoritatively enforced.
4. Do not treat UI visibility as security enforcement.
5. Document resource ownership rules when relevant.
6. Include denied-operation behavior.
7. Confirm privileged operations receive appropriate attention.
8. Confirm external service permissions do not expose secret values.
9. Verify important permission rules with real evidence.
10. Preserve material permission changes.
11. Remove ALL instructional HTML comments.

The completed artifact should let a reviewer determine who may perform
important operations and where the system enforces those boundaries.
-->
