# Code Review Example

<!--
STARTER KIT GUIDANCE — DELETE BEFORE PHASE-GATE SUBMISSION IF THIS FILE IS
USED AS AN ACTUAL REVIEW RECORD

This file demonstrates the structure and depth expected from a meaningful code
review.

For an actual review, either:

1. copy and rename this file; or
2. use the same structure in the applicable GitHub pull-request review.

Do NOT treat code review as:

"Looks good."

A useful code review evaluates the change against engineering expectations.

Possible review areas include:

- requirement correctness;
- acceptance criteria;
- design and architecture;
- readability;
- maintainability;
- error handling;
- security;
- data integrity;
- interface contracts;
- test coverage;
- edge conditions;
- operational impact.

Not every review must examine every area.

Review depth should be proportional to the significance and risk of the change.

IMPORTANT:

- All content inside HTML comments is Starter Kit guidance.
- If this file is copied for a real review, remove instructional comments.
- Never fabricate a review or approval.
-->

## Review Identification

**Reviewer:**  
**Date:**  
**Pull Request / Change:**  
**Commit / Baseline Reviewed:**  
**Author(s):**  

<!--
TEAM CONTENT REQUIRED FOR AN ACTUAL REVIEW

Reference the exact change being reviewed.

Where possible, use the GitHub PR number or commit.

Do not review an undefined or moving baseline.
-->

## Change Summary

<!--
TEAM CONTENT REQUIRED

Briefly explain what the change is intended to do.

The reviewer should understand the purpose before evaluating the implementation.

Reference requirements, issues, or acceptance criteria when appropriate.

Replace this comment with the actual change summary.
-->

## Related Engineering Evidence

<!--
TEAM CONTENT REQUIRED WHEN APPLICABLE

Reference evidence relevant to understanding the change.

Examples:

- requirement ID;
- acceptance criterion;
- API contract;
- ADR;
- defect;
- issue;
- task;
- architecture component.

Do not add links that are unrelated merely to make the review appear thorough.
-->

| Evidence | Reference | Why It Matters |
|---|---|---|
|  |  |  |

## Review Areas

<!--
STARTER KIT GUIDANCE — DELETE FROM AN ACTUAL REVIEW

The review areas below are prompts, not a mandatory checklist.

Evaluate areas relevant to the change.

CORRECTNESS

- Does the change implement the intended behavior?
- Are important conditions missing?
- Does it contradict a requirement or acceptance criterion?

ARCHITECTURE / DESIGN

- Does the code respect component responsibilities?
- Does it introduce inappropriate coupling?
- Does it bypass an intended interface?

READABILITY / MAINTAINABILITY

- Can another engineer understand the code?
- Are names and abstractions meaningful?
- Is complexity justified?

FAILURE HANDLING

- What happens when input is invalid?
- What happens when a dependency fails?
- Can partial success produce an incorrect state?

SECURITY

- Is authentication or authorization affected?
- Is sensitive data exposed?
- Is input treated as trusted when it should not be?

DATA INTEGRITY

- Can state become inconsistent?
- Are transaction or concurrency issues relevant?

TESTING

- Do tests cover the important behavior?
- Are failure and boundary conditions represented?
- Could existing tests pass while the implementation is still wrong?

OPERATIONS

- Does the change affect logging, metrics, configuration, deployment, recovery,
  or runtime behavior?
-->

## Findings

<!--
TEAM CONTENT REQUIRED

Use stable review-finding IDs when useful:

CR-###

Examples:

CR-001
CR-002

Finding Type may include:

- Blocking
- Required Change
- Suggestion
- Question
- Positive Observation

A review does not need a finding in every category.

Do not invent findings merely to prove the review happened.

EXAMPLE ONLY:

| ID | Type | Finding | Evidence / Location | Required Action |
|---|---|---|---|---|
| CR-001 | Required Change | Validation occurs only in the client, allowing direct API calls to bypass the rule | `request-form.js`, API-001 | Enforce authoritative validation in Application Service |

DELETE the example and populate actual findings below.
-->

| ID | Type | Finding | Evidence / Location | Required Action |
|---|---|---|---|---|
|  |  |  |  |  |

## Test and Verification Review

<!--
TEAM CONTENT REQUIRED

Evaluate whether the change has appropriate verification.

Do not state only:

"Tests pass."

Ask whether the right behavior is being tested.

EXAMPLE ONLY:

| Area | Evidence | Review Result | Gap |
|---|---|---|---|
| Valid submission | integration test | Adequate | None |
| Missing required field | no test | Incomplete | Add negative-path test |

Populate actual evidence below.
-->

| Area | Evidence | Review Result | Gap |
|---|---|---|---|
|  |  |  |  |

## Architecture / Contract Impact

<!--
TEAM CONTENT REQUIRED WHEN THE CHANGE AFFECTS ARCHITECTURE OR INTERFACES

Review whether the implementation agrees with:

/docs/architecture/architecture.md
/docs/architecture/component-responsibilities.md
/docs/architecture/api-contracts.md

If the code requires a legitimate architecture or contract change, update the
engineering evidence rather than treating documentation inconsistency as
acceptable.

Remove this section when it genuinely does not apply.
-->

## Documentation / Traceability Impact

<!--
TEAM CONTENT REQUIRED WHEN ENGINEERING EVIDENCE MUST CHANGE

Consider whether the change requires updates to:

- requirements;
- acceptance criteria;
- architecture;
- API contracts;
- ADRs;
- tests;
- defect log;
- runbook;
- traceability.

Do not automatically require documentation changes for every small code edit.
-->

| Artifact | Update Needed? | Reason / Action |
|---|---|---|
|  |  |  |

## Positive Observations

<!--
OPTIONAL TEAM CONTENT

Good reviews may identify strengths as well as defects.

Examples:

- clear responsibility boundary;
- effective regression test;
- good failure handling;
- simpler implementation than previous design.

Use actual evidence.

Remove this section if there is nothing useful to record.
-->

- 

<!--
DELETE THE PLACEHOLDER BULLET ABOVE IN AN ACTUAL REVIEW.
-->

## Review Decision

<!--
TEAM CONTENT REQUIRED

Suggested outcomes:

Approve
- No required changes remain.

Approve with Non-Blocking Suggestions
- Change is acceptable, with optional improvements noted.

Changes Requested
- One or more required findings must be addressed.

Do not approve code merely because it compiles or tests pass.
-->

**Decision:**  

**Rationale:**  

## Follow-Up Verification

<!--
TEAM CONTENT REQUIRED WHEN CHANGES WERE REQUESTED

Record how required findings were resolved and rechecked.

EXAMPLE ONLY:

| Finding ID | Resolution Evidence | Re-Review Result |
|---|---|---|
| CR-001 | Commit abc1234, new integration test | Resolved |

Populate actual follow-up evidence below.

Remove this section if no follow-up was required.
-->

| Finding ID | Resolution Evidence | Re-Review Result |
|---|---|---|
|  |  |  |

<!--
FINAL STARTER KIT CHECK — DELETE FROM AN ACTUAL REVIEW

Before finalizing an actual code-review record:

1. Identify the exact PR / commit reviewed.
2. Understand the intended behavior before reviewing implementation.
3. Reference relevant engineering evidence.
4. Record actual findings rather than generic comments.
5. Review tests for adequacy, not merely pass/fail.
6. Consider architecture and interface impact when relevant.
7. Distinguish blocking findings from suggestions.
8. Record the actual review decision.
9. Verify required changes before closing the review.
10. Remove ALL instructional HTML comments.

A useful code review should show engineering judgment, not merely approval.
-->
