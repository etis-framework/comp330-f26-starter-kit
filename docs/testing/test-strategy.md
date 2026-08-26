# Test Strategy

<!--
STARTER KIT GUIDANCE — DELETE BEFORE PHASE-GATE SUBMISSION

This file defines the team's overall approach to testing and verification.

A test strategy should answer questions such as:

- What kinds of defects are we trying to detect?
- What testing levels matter for this system?
- Which risks require deeper verification?
- What should be automated?
- What still requires human review or manual verification?
- How do requirements and acceptance criteria connect to tests?
- How do we handle negative paths, failures, and regression risk?
- What evidence will demonstrate that testing actually occurred?

This file defines the overall testing APPROACH.

Detailed execution planning belongs in:

/docs/testing/test-plan.md

Specific test scenarios belong in:

/docs/testing/test-cases.md

Automated pipeline evidence belongs in:

/docs/testing/ci-evidence.md

IMPORTANT:

- Everything inside HTML comments is Starter Kit guidance.
- Remove ALL instructional comments before the applicable phase-gate submission.
- Examples are guidance only.
- Do not claim a testing practice exists unless the team actually intends to use it.
-->

## Testing Objectives

<!--
TEAM CONTENT REQUIRED

Describe what the team is trying to accomplish through testing.

Possible objectives include:

- verify requirements;
- verify acceptance criteria;
- detect regressions;
- validate important architecture boundaries;
- verify failure handling;
- verify security behavior;
- verify operational behavior;
- reduce release risk.

Do not simply write:

"Make sure the system works."

Replace this comment with the team's actual testing objectives.
-->

## Testing Principles

<!--
TEAM CONTENT REQUIRED

Define the principles that guide testing decisions.

Examples ONLY:

- Test behavior against requirements, not implementation assumptions.
- Verify both successful and unsuccessful paths.
- Automate repeatable verification where practical.
- Use human review where judgment is required.
- Preserve evidence of meaningful test execution.
- Add regression coverage when a significant defect is fixed.

Do not retain generic principles merely because they sound good.

Replace this comment with principles the team actually intends to follow.
-->

## Test Levels

<!--
TEAM CONTENT REQUIRED

Define which test levels are appropriate for this system.

Possible levels include:

- Unit
- Component
- Integration
- Contract
- System
- End-to-End
- Acceptance
- Runtime / Operational

Do NOT include every possible test level automatically.

For each level, explain:

- what it verifies;
- what boundary it exercises;
- what kinds of defects it is intended to detect.

EXAMPLE ONLY:

| Test Level | Purpose | Typical Scope | Primary Defects Detected |
|---|---|---|---|
| Unit | Verify isolated business logic | Individual function or module | Logic and boundary-condition defects |
| Integration | Verify interaction among components | Application Service and Persistence | Interface and state-management defects |

DELETE the example and populate the actual table below.
-->

| Test Level | Purpose | Typical Scope | Primary Defects Detected |
|---|---|---|---|
|  |  |  |  |

## Test Types

<!--
TEAM CONTENT REQUIRED

Identify test types relevant to the actual system.

Possible types include:

- Functional
- Negative-path
- Regression
- Security
- Performance
- Reliability
- Usability
- Accessibility
- Compatibility
- Recovery
- Deployment verification

Do not add a category merely because it appears in this list.

EXAMPLE ONLY:

| Test Type | Why It Matters | Where Applied |
|---|---|---|
| Negative-path testing | Ensures invalid input does not create invalid state | Workflow submission and authorization |
| Regression testing | Prevents previously corrected defects from returning | Automated CI suite |

Populate actual testing types below.
-->

| Test Type | Why It Matters | Where Applied |
|---|---|---|
|  |  |  |

## Requirements and Acceptance-Criteria Coverage

<!--
TEAM CONTENT REQUIRED

Testing should connect to engineering expectations.

Reference:

/docs/requirements/requirements.md
/docs/requirements/acceptance-criteria.md
/docs/planning/traceability.md

A useful chain is:

Requirement
  ->
Acceptance Criterion
  ->
Test
  ->
Test Result
  ->
Release Evidence

Do not require every low-level unit test to map directly to a requirement.

Traceability matters most for meaningful behavior and release claims.

Replace this comment with the team's actual traceability approach.
-->

## Risk-Based Testing

<!--
TEAM CONTENT REQUIRED

Not every part of the system deserves equal testing depth.

Use risk to guide verification effort.

Consider areas with:

- high impact if incorrect;
- complex logic;
- security significance;
- data integrity consequences;
- external dependencies;
- repeated defect history;
- difficult recovery;
- architectural uncertainty.

Reference:

/docs/planning/risk-register.md

EXAMPLE ONLY:

| Risk / Concern | Additional Testing Approach | Related Evidence |
|---|---|---|
| Unauthorized data access | Multi-user authorization tests and negative-path API verification | R-004, permission-boundaries.md |

DELETE the example and populate actual risk-based testing below.
-->

| Risk / Concern | Additional Testing Approach | Related Evidence |
|---|---|---|
|  |  |  |

## Positive and Negative Testing

<!--
TEAM CONTENT REQUIRED

Describe how the team will verify both:

POSITIVE PATHS
Expected valid behavior.

NEGATIVE PATHS
Invalid, unauthorized, missing, conflicting, or failed conditions.

Examples of negative conditions may include:

- missing required input;
- malformed data;
- unauthorized operation;
- duplicate request;
- unavailable dependency;
- unknown resource;
- invalid state transition.

Do not test negative conditions merely for volume.

Prioritize those that matter to requirements, security, integrity, and risk.

Replace this comment with the team's actual approach.
-->

## Automation Strategy

<!--
TEAM CONTENT REQUIRED

Explain what the team intends to automate and why.

Possible automated checks include:

- unit tests;
- integration tests;
- contract tests;
- regression tests;
- static checks;
- build verification;
- deployment checks.

Also identify what remains manual and why.

Do not claim "everything is automated" unless that is actually true.
-->

| Verification Area | Automated / Manual / Mixed | Reason |
|---|---|---|
|  |  |  |

## Regression Strategy

<!--
TEAM CONTENT REQUIRED

Describe how the team prevents previously fixed behavior from breaking again.

A practical rule may be:

"When a meaningful defect is fixed, add or update an automated test where
practical so the defect would be detected if it returned."

Reference:

/docs/quality/defect-log.md

Replace this comment with the team's actual regression approach.
-->

## Test Data Strategy

<!--
TEAM CONTENT REQUIRED

Describe how test data will be created and controlled.

Consider:

- synthetic data;
- test accounts;
- boundary values;
- invalid data;
- duplicate data;
- security-sensitive cases.

Reference:

/docs/security/data-handling-notes.md

Do not place real sensitive personal information into tests merely because it
is convenient.

Replace this comment with the team's actual test-data approach.
-->

## Environment Strategy

<!--
TEAM CONTENT REQUIRED

Identify where different kinds of tests run.

Examples might include:

- local developer environment;
- CI;
- test deployment;
- staging-like environment;
- deployed course environment.

Explain meaningful differences that could affect results.

Do not create fictional environments.
-->

| Environment | Testing Purpose | Important Differences / Limitations |
|---|---|---|
|  |  |  |

## AI-Assisted Testing

<!--
TEAM CONTENT REQUIRED WHEN AI IS USED TO ASSIST TESTING

AI may assist with:

- identifying edge cases;
- proposing test scenarios;
- reviewing test completeness;
- suggesting failure conditions;
- generating initial test code.

AI output is not verification by itself.

The team remains responsible for:

- deciding whether proposed tests are valid;
- understanding generated test code;
- verifying test expectations;
- ensuring tests actually exercise meaningful behavior.

Reference:

/docs/ai/ai-policy.md
/docs/ai/ai-use-log.md

Remove this section if AI-assisted testing is not used.
-->

## Test Evidence

<!--
TEAM CONTENT REQUIRED

Define what evidence the team preserves.

Possible evidence includes:

- CI run;
- test report;
- test-case result;
- runtime evidence;
- pull request;
- screenshot when appropriate;
- defect verification.

Do not store large amounts of redundant evidence without purpose.

The evidence should be reviewable enough to support important engineering claims.

Replace this comment with the team's actual evidence approach.
-->

## Known Testing Limitations

<!--
TEAM CONTENT REQUIRED

Record limitations honestly.

Examples ONLY:

- no sustained-load testing;
- one external integration verified manually;
- browser compatibility limited;
- recovery testing incomplete;
- performance baseline not yet established.

Reference:

/docs/release/known-limitations.md

when the limitation affects a release.
-->

| Limitation | Impact | Planned Improvement | Related Evidence |
|---|---|---|---|
|  |  |  |  |

<!--
FINAL STARTER KIT CHECK — DELETE BEFORE PHASE-GATE SUBMISSION

Before submission:

1. Define testing objectives that actually matter to the project.
2. Include only test levels and types the team genuinely uses.
3. Connect important verification to requirements and acceptance criteria.
4. Use risk to guide test depth.
5. Include meaningful negative-path testing.
6. Be explicit about what is automated versus manual.
7. Describe regression and test-data practices.
8. Identify real test environments.
9. State testing limitations honestly.
10. Remove ALL instructional HTML comments.

The completed strategy should explain WHY the team tests the way it does, not
serve as a generic catalog of testing terminology.
-->
