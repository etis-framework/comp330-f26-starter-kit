# Test Cases

<!--
STARTER KIT GUIDANCE — DELETE BEFORE PHASE-GATE SUBMISSION

This file records significant executable or manually verifiable test scenarios.

A test case should define enough information that another engineer can
understand:

- what behavior is being tested;
- what requirement or acceptance criterion it supports;
- what starting condition is required;
- what actions or inputs are used;
- what result is expected;
- what actually occurred when executed.

Not every unit test belongs in this file.

Use this artifact for tests important enough to support requirements,
acceptance criteria, release verification, defect regression, security,
integration, or other meaningful engineering evidence.

Automated test code may remain the authoritative executable artifact.

In that case, this file may summarize the important scenario and reference
the executable test rather than duplicating every detail.

IMPORTANT:

- Everything inside HTML comments is Starter Kit guidance.
- Remove ALL instructional comments before the applicable phase-gate submission.
- Examples are guidance only.
- Do not record a test as Passed unless it was actually executed.
-->

## Test Case Catalog

<!--
TEAM CONTENT REQUIRED

Use stable test-case IDs:

TC-###

Examples:

TC-001
TC-002
TC-003

COLUMN GUIDANCE

Test Case
Short descriptive title.

Related Requirement / Criterion
Reference REQ and AC identifiers.

Type
Examples:
- Functional
- Negative
- Security
- Regression
- Integration
- Acceptance
- Recovery

Automation
Suggested values:
- Automated
- Manual
- Mixed

Status
Suggested values:
- Draft
- Ready
- Passed
- Failed
- Blocked
- Not Run
- Deprecated

EXAMPLE ONLY:

| ID | Test Case | Related Requirement / Criterion | Type | Automation | Status |
|---|---|---|---|---|---|
| TC-001 | Submit valid workflow request | REQ-001 / AC-REQ-001-01 | Acceptance | Automated | Ready |
| TC-002 | Reject missing required description | REQ-001 / AC-REQ-001-02 | Negative | Automated | Ready |

DELETE the examples and populate the actual table below.
-->

| ID | Test Case | Related Requirement / Criterion | Type | Automation | Status |
|---|---|---|---|---|---|
|  |  |  |  |  |  |

## Detailed Test Cases

<!--
TEAM CONTENT REQUIRED

Use a detailed subsection for important test cases.

Suggested structure:

### TC-### — Test Case Name

**Purpose**
What behavior is this test intended to verify?

**Related Requirement(s)**
REQ-###

**Related Acceptance Criteria**
AC-REQ-###-##

**Type**
Functional / Negative / Security / Regression / Integration / Acceptance / etc.

**Automation**
Automated / Manual / Mixed

**Environment**
Where the test is executed.

#### Preconditions

What must already be true?

#### Test Data

What meaningful data is required?

Do not include passwords, tokens, or protected data.

#### Steps

1.
2.
3.

#### Expected Result

State observable behavior.

#### Actual Result

Populate only after execution.

#### Evidence

Reference:
- automated test;
- CI run;
- runtime evidence;
- screenshot where appropriate;
- issue;
- log;
- other reviewable evidence.

#### Status

Not Run / Passed / Failed / Blocked

#### Notes / Defects

Reference defects discovered during execution.

Copy and adapt this structure for each significant test case.
-->

## Positive-Path Cases

<!--
TEAM CONTENT REQUIRED

Ensure important valid workflows are covered.

Do not assume successful-path testing alone demonstrates correctness.

Use this section as an index or summary if useful.

Remove this section if the catalog already provides enough clarity.
-->

| Test Case ID | Behavior Verified | Result |
|---|---|---|
|  |  |  |

## Negative-Path Cases

<!--
TEAM CONTENT REQUIRED

Identify important invalid or prohibited conditions.

Possible areas include:

- missing required input;
- malformed input;
- unauthorized action;
- invalid state transition;
- duplicate operation;
- missing resource;
- dependency failure.

Do not create negative cases merely to increase test count.

Focus on meaningful behavior.
-->

| Test Case ID | Negative Condition | Expected Protection / Behavior | Result |
|---|---|---|---|
|  |  |  |  |

## Boundary and Edge Cases

<!--
TEAM CONTENT REQUIRED WHEN RELEVANT

Boundary testing may include:

- empty values;
- maximum/minimum values;
- duplicate input;
- unusual sequence;
- state transition boundary;
- timing or ordering edge.

Do not manufacture edge cases that are irrelevant to the system.

Populate actual meaningful cases below.
-->

| Test Case ID | Boundary / Edge Condition | Why It Matters | Result |
|---|---|---|---|
|  |  |  |  |

## Security Cases

<!--
TEAM CONTENT REQUIRED WHEN SECURITY BEHAVIOR IS TESTED

Reference:

/docs/security/permission-boundaries.md

Possible security test scenarios:

- unauthenticated request denied;
- unauthorized user denied;
- resource ownership enforced;
- invalid token handled;
- sensitive data not exposed.

Do not treat UI visibility as security verification.

Populate actual security cases below.

Remove this section if security cases are indexed elsewhere.
-->

| Test Case ID | Security Rule | Expected Result | Evidence |
|---|---|---|---|
|  |  |  |  |

## Regression Cases

<!--
TEAM CONTENT REQUIRED WHEN DEFECTS HAVE BEEN FIXED

Reference:

/docs/quality/defect-log.md

A meaningful fixed defect should often produce regression coverage when
practical.

EXAMPLE ONLY:

| Test Case ID | Defect ID | Behavior Protected | Evidence |
|---|---|---|---|
| TC-014 | DEF-006 | Whitespace-only description rejected | Automated integration test |

DELETE the example and populate actual regression cases below.
-->

| Test Case ID | Defect ID | Behavior Protected | Evidence |
|---|---|---|---|
|  |  |  |  |

## Test Execution Results

<!--
TEAM CONTENT REQUIRED AS TESTS ARE EXECUTED

Preserve actual execution results.

Do not change a failed result to Passed without preserving evidence that the
failure was corrected and the test rerun.

Use execution identifiers when useful:

TEST-RUN-###

EXAMPLE ONLY:

| Run ID | Date | Test Case | Environment | Result | Evidence | Defect / Follow-Up |
|---|---|---|---|---|---|---|
| TEST-RUN-001 | YYYY-MM-DD | TC-001 | CI | Passed | CI run reference | None |

DELETE the example and populate actual executions below.
-->

| Run ID | Date | Test Case | Environment | Result | Evidence | Defect / Follow-Up |
|---|---|---|---|---|---|---|
|  |  |  |  |  |  |  |

## Blocked or Not-Run Tests

<!--
TEAM CONTENT REQUIRED

Do not silently omit tests that were expected but could not run.

Document:

- which test;
- why it could not execute;
- release impact;
- planned action.

A blank table is correct when all planned important tests were executed.
-->

| Test Case ID | Reason Not Executed | Impact | Planned Action |
|---|---|---|---|
|  |  |  |  |

## Test Case Changes

<!--
TEAM CONTENT REQUIRED WHEN TEST CASES CHANGE MATERIALLY

A test case may change because:

- requirement changed;
- acceptance criterion changed;
- interface changed;
- defect exposed a missing condition;
- test expectation was incorrect.

Do not silently rewrite test history when a meaningful expectation changes.

A blank table is intentional at project start.
-->

| Date / Gate | Test Case ID | Change | Reason | Related Evidence |
|---|---|---|---|---|
|  |  |  |  |  |

<!--
FINAL STARTER KIT CHECK — DELETE BEFORE PHASE-GATE SUBMISSION

Before submission:

1. Include only test cases meaningful to project verification.
2. Confirm requirement and acceptance-criteria references exist.
3. Include negative and boundary behavior where relevant.
4. Verify security cases against actual permission rules.
5. Link fixed defects to regression tests where practical.
6. Record actual execution results honestly.
7. Do not claim Passed unless a test actually ran successfully.
8. Record blocked or unexecuted important tests.
9. Preserve meaningful test-case changes.
10. Remove ALL instructional HTML comments.

The completed artifact should show what important behaviors were tested and
what actually happened when those tests were executed.
-->
