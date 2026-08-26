# Defect Log

<!--
STARTER KIT GUIDANCE — DELETE BEFORE PHASE-GATE SUBMISSION

This file records actual defects discovered during development, review,
verification, integration, deployment, or operation.

A defect is observed behavior or implementation that does not meet an expected
condition.

A defect may relate to:

- a requirement;
- an acceptance criterion;
- an interface contract;
- expected architecture behavior;
- test expectations;
- security;
- reliability;
- usability;
- deployment;
- operations; or
- another documented engineering expectation.

Do NOT create fictional defects merely to populate this file.

At the beginning of the project, a blank defect log is correct.

This file is not intended to replace GitHub Issues or another defect-tracking
system if your team uses one. It provides a concise engineering evidence view
and may reference the authoritative issue.

IMPORTANT:

- Everything inside HTML comments is Starter Kit guidance.
- Remove all instructional comments before the applicable phase-gate submission.
- Examples inside comments are guidance only.
- Record only defects that actually occurred.
-->

## Defects

<!--
TEAM CONTENT REQUIRED WHEN DEFECTS ARE DISCOVERED

Use stable identifiers:

DEF-###

Examples:

DEF-001
DEF-002
DEF-003

Do not reuse an identifier for another defect.

COLUMN GUIDANCE

Summary
Briefly identify the observed problem.

Detected In
Identify where the defect was discovered.

Examples:
- unit test;
- integration test;
- pull-request review;
- manual verification;
- deployed environment;
- runtime observation.

Related Evidence
Reference requirements, acceptance criteria, API contracts, tests, issues,
runtime evidence, or other relevant artifacts.

Severity
Use the team's defined severity categories below.

Status
Suggested values:

- Open
- Investigating
- Fix In Progress
- Ready for Verification
- Closed
- Deferred
- Rejected / Not a Defect

Owner
Identify who is responsible for driving the defect toward disposition.

Resolution / Evidence
Reference the fix, PR, test, or other evidence demonstrating the outcome.

EXAMPLE ONLY:

| ID | Summary | Detected In | Related Evidence | Severity | Status | Owner | Resolution / Evidence |
|---|---|---|---|---|---|---|---|
| DEF-001 | Submission accepts whitespace-only required description | Integration verification | REQ-001, AC-REQ-001-02 | Medium | Open | Jordan Smith | Issue #14 |

DELETE the example and populate the actual table below.
-->

| ID | Summary | Detected In | Related Evidence | Severity | Status | Owner | Resolution / Evidence |
|---|---|---|---|---|---|---|---|
|  |  |  |  |  |  |  |  |

## Severity Guidance

<!--
TEAM CONTENT REQUIRED

Define a simple severity model appropriate to your project.

Severity describes the CONSEQUENCE of the defect.

It is different from priority, which describes how urgently the team intends
to address it.

A simple model is sufficient.

EXAMPLE ONLY:

Critical
- prevents core system operation;
- creates serious security or data-integrity exposure; or
- has another unacceptable system-level consequence.

High
- significantly impairs an important capability with no practical workaround.

Medium
- causes incorrect behavior but impact is limited or a reasonable workaround
  exists.

Low
- minor defect with limited engineering or user impact.

Your team may use another model, but define it clearly and use it consistently.

Replace this comment with your team's actual severity definitions.
-->

## Detailed Defect Records

<!--
OPTIONAL TEAM CONTENT

Use a detailed record when a row in the table is not sufficient.

Do not create lengthy records for trivial defects.

Suggested structure:

### DEF-### — Short Defect Title

**Detected:** YYYY-MM-DD
**Environment / Context:**
**Severity:**
**Status:**
**Owner:**
**Related Issue / PR:**
**Related Requirement(s):**
**Related Acceptance Criteria:**

#### Observed Behavior

What actually happened?

#### Expected Behavior

What should have happened, and what evidence establishes that expectation?

#### Reproduction

How can the problem be reproduced?

#### Investigation

What evidence was reviewed?

What component, condition, assumption, or interaction appears responsible?

Do not state a cause as fact unless evidence supports it.

#### Resolution

What changed?

#### Verification

What evidence demonstrates that the defect is fixed or otherwise resolved?

#### Remaining Concerns

Identify any remaining limitation, risk, or follow-up work.

Copy this structure only when additional defect evidence is useful.
-->

## Defect Lifecycle

<!--
STARTER KIT GUIDANCE — DELETE BEFORE PHASE-GATE SUBMISSION

A useful defect lifecycle is:

Detected
  ->
Recorded
  ->
Investigated
  ->
Fixed or otherwise dispositioned
  ->
Verified
  ->
Closed

Do not close a defect merely because code was changed.

Closure should normally require evidence that the expected behavior is now
satisfied.

A defect may also be:

Deferred
- the team accepts that it will not be corrected in the current delivery scope;

Rejected / Not a Defect
- investigation demonstrates that observed behavior is consistent with the
  actual requirement or intended design.

When a defect reveals that the requirement itself is wrong or unclear, update
the requirement rather than forcing implementation to satisfy an incorrect
expectation.
-->

## Defect-to-Requirement Traceability

<!--
TEAM CONTENT REQUIRED WHEN DEFECTS AFFECT REQUIREMENTS OR ACCEPTANCE CRITERIA

A defect may reveal:

- implementation failure;
- missing acceptance criteria;
- ambiguous requirement;
- incorrect assumption;
- architecture weakness;
- interface-contract weakness;
- test gap.

Reference affected engineering evidence rather than treating the defect as an
isolated coding problem.

EXAMPLE ONLY:

| Defect ID | Requirement / Criterion | Relationship | Evidence Updated |
|---|---|---|---|
| DEF-001 | AC-REQ-001-02 | Existing criterion exposed missing validation | Integration test added |

Populate actual relationships below when useful.
-->

| Defect ID | Requirement / Criterion | Relationship | Evidence Updated |
|---|---|---|---|
|  |  |  |  |

## Deferred Defects

<!--
TEAM CONTENT REQUIRED WHEN A KNOWN DEFECT IS INTENTIONALLY DEFERRED

A deferred defect remains known engineering debt.

Do not silently remove it from the log.

Document:

- why it is being deferred;
- impact;
- remaining risk;
- when it should be reconsidered.

A blank table is correct when no defects are deferred.
-->

| Defect ID | Reason Deferred | Impact / Risk | Reconsider By | Related Evidence |
|---|---|---|---|---|
|  |  |  |  |  |

## Defect Evidence Integrity

<!--
STARTER KIT GUIDANCE — DELETE BEFORE PHASE-GATE SUBMISSION

Do not hide defects because they make the project appear imperfect.

Defect discovery is normal engineering evidence.

A useful defect record may demonstrate that the team:

- found a problem;
- understood the expectation it violated;
- investigated the cause;
- corrected the system;
- verified the correction; and
- improved related engineering evidence.

Do not:

- fabricate defects;
- fabricate fixes;
- claim verification that did not occur;
- delete meaningful defect history merely because the defect was fixed.
-->

<!--
FINAL STARTER KIT CHECK — DELETE BEFORE PHASE-GATE SUBMISSION

Before submission:

1. Keep the table blank if no actual defects have been discovered.
2. Confirm every DEF-### entry represents a real observed defect.
3. Confirm severity uses the team's defined model.
4. Confirm related requirements and acceptance criteria actually exist.
5. Confirm Closed defects have meaningful resolution or verification evidence.
6. Preserve deferred defects and their known risk.
7. Update affected engineering artifacts when a defect exposes a deeper issue.
8. Remove ALL instructional HTML comments.

The completed defect log should preserve factual evidence about actual quality
problems and their disposition.
-->
