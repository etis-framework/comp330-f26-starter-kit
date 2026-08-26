# Runtime Evidence

<!--
STARTER KIT GUIDANCE — DELETE BEFORE PHASE-GATE SUBMISSION

This file records actual evidence observed from the running system.

This is different from:

/docs/observability/observability-plan.md
which describes what the team intends to observe,

and:

/docs/observability/metrics-notes.md
which defines what metrics mean.

This file should contain ACTUAL runtime observations and references to
repository-visible evidence.

Examples of runtime evidence may include:

- successful or failed execution of an important workflow;
- observed health-check behavior;
- captured metric values;
- relevant log evidence;
- dependency-failure behavior;
- recovery behavior;
- performance observations;
- deployment verification;
- runtime evidence supporting acceptance criteria.

Do not fabricate runtime evidence.

If something has not yet been observed or tested, state that as a gap rather
than manufacturing a result.

IMPORTANT:

- Everything inside HTML comments is Starter Kit guidance.
- Delete instructional comments before the applicable phase-gate submission.
- Example evidence inside comments is NOT project evidence.
-->

## Runtime Evidence Summary

<!--
TEAM CONTENT REQUIRED

Briefly summarize:

- what environment was observed;
- what major runtime behaviors were examined;
- whether important evidence was captured successfully; and
- any significant limitations or unresolved concerns.

Keep this concise.

Replace this comment with the actual summary.
-->

## Evidence Records

<!--
TEAM CONTENT REQUIRED

Use stable runtime evidence IDs:

RUN-###

Examples:

RUN-001
RUN-002
RUN-003

COLUMN GUIDANCE

Date / Time
Record when the observation occurred. Include enough context to distinguish
separate runs.

Environment
Examples might include local development, CI, test deployment, staging, or
another actual environment.

Scenario
Describe what was exercised or observed.

Evidence
Reference repository-visible or otherwise reviewable evidence when practical.

Examples:
- log artifact;
- test result;
- screenshot stored in an approved evidence location;
- workflow output;
- metric capture;
- issue;
- PR;
- deployment evidence.

Observation
State what actually happened.

Related Evidence
Reference requirements, acceptance criteria, metrics, API contracts, issues,
or other evidence when appropriate.

Result / Action
Examples:
- Passed
- Failed
- Investigate
- Defect opened
- Requirement updated
- No action required

EXAMPLE ONLY:

| ID | Date / Time | Environment | Scenario | Evidence | Observation | Related Evidence | Result / Action |
|---|---|---|---|---|---|---|---|
| RUN-001 | 2026-09-15 14:30 | Test deployment | Submit valid workflow request | Integration test output and application log | Request completed successfully and generated expected identifier | REQ-001, AC-REQ-001-01, MET-002 | Passed |

DELETE the example and populate the actual table below.
-->

| ID | Date / Time | Environment | Scenario | Evidence | Observation | Related Evidence | Result / Action |
|---|---|---|---|---|---|---|---|
|  |  |  |  |  |  |  |  |

## Detailed Runtime Evidence

<!--
OPTIONAL TEAM CONTENT

Use a detailed subsection when a table row is not sufficient to preserve
important runtime evidence.

Suggested structure:

### RUN-### — Short Description

**Date / Time:**
**Environment:**
**Related Requirement(s):**
**Related Acceptance Criteria:**
**Related Metric(s):**

#### Scenario

What was executed or observed?

#### Evidence

Where is the reviewable evidence?

#### Observation

What actually happened?

#### Interpretation

What does the observation mean?

#### Result / Action

What did the team do because of this evidence?

Possible actions include:

- no action required;
- defect opened;
- implementation changed;
- requirement refined;
- architecture reconsidered;
- additional verification required;
- observability gap identified.

Do not create detailed entries for trivial observations.
-->

## Metric Observations

<!--
TEAM CONTENT REQUIRED WHEN METRICS ARE ACTUALLY OBSERVED

Reference metric IDs from:

/docs/observability/metrics-notes.md

Record actual observations rather than expected values.

EXAMPLE ONLY:

| Evidence ID | Metric ID | Observed Value | Context / Window | Interpretation |
|---|---|---|---|---|
| RUN-004 | MET-001 | 0% | 25 valid submission attempts during acceptance verification | No submission failures observed in this run |

DELETE the example and populate actual values below where applicable.
-->

| Evidence ID | Metric ID | Observed Value | Context / Window | Interpretation |
|---|---|---|---|---|
|  |  |  |  |  |

## Failure and Recovery Evidence

<!--
TEAM CONTENT REQUIRED WHEN FAILURE OR RECOVERY BEHAVIOR HAS BEEN EXERCISED

Successful execution is not the only useful runtime evidence.

When appropriate, capture evidence involving:

- invalid input;
- failed dependency;
- unauthorized access;
- service startup failure;
- retry or recovery behavior;
- degraded operation;
- other relevant failure conditions.

EXAMPLE ONLY:

| Evidence ID | Failure Scenario | Expected Behavior | Observed Behavior | Result |
|---|---|---|---|---|
| RUN-005 | Persistence dependency unavailable | Health check reports unhealthy and request fails without false success | Expected behavior observed | Passed |

DELETE the example and populate actual evidence below where appropriate.
-->

| Evidence ID | Failure Scenario | Expected Behavior | Observed Behavior | Result |
|---|---|---|---|---|
|  |  |  |  |  |

## Known Runtime Evidence Gaps

<!--
TEAM CONTENT REQUIRED

Record important evidence the team does not yet have.

Examples ONLY:

- recovery from dependency outage has not yet been tested;
- no sustained-load evidence exists yet;
- metrics have not yet been observed in the deployed environment;
- alert behavior has not yet been verified.

Do not treat an evidence gap as a failure unless the applicable requirement or
phase gate requires the evidence already.

Use the table below to make gaps explicit and manageable.
-->

| Gap | Why It Matters | Planned Evidence / Action | Target Gate / Milestone |
|---|---|---|---|
|  |  |  |  |

## Evidence Integrity

<!--
STARTER KIT GUIDANCE — DELETE BEFORE PHASE-GATE SUBMISSION

Runtime evidence should represent what actually occurred.

Do not:

- claim a test was executed when it was not;
- record expected results as observed results;
- modify evidence to hide a failure;
- omit a significant failure merely because the desired result was different;
- describe an AI-generated prediction as runtime evidence.

Unexpected or failed runtime evidence can be highly valuable because it may
identify defects, incorrect assumptions, weak requirements, or architectural
problems.

Preserve meaningful failures and document the resulting engineering action.
-->

<!--
FINAL STARTER KIT CHECK — DELETE BEFORE PHASE-GATE SUBMISSION

Before submission:

1. Remove all example guidance and instructional comments.
2. Confirm every retained RUN-### entry represents an actual observation.
3. Confirm environments and dates are accurate.
4. Confirm evidence references point to real, reviewable evidence where practical.
5. Confirm metric IDs agree with metrics-notes.md.
6. Confirm related requirements and acceptance criteria exist.
7. Clearly distinguish observed behavior from interpretation.
8. Preserve meaningful failures and resulting engineering actions.
9. Identify important evidence gaps honestly.
10. Remove ALL instructional HTML comments.

The finished file is evidence of what the running system actually did, not
what the team hoped or expected it would do.
-->
