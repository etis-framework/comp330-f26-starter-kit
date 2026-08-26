# CI Evidence

<!--
STARTER KIT GUIDANCE — DELETE BEFORE PHASE-GATE SUBMISSION

This file records evidence produced by Continuous Integration (CI).

CI is useful because it provides repeatable, repository-connected evidence that
important automated checks executed against a specific code baseline.

CI evidence may include:

- build result;
- automated test result;
- static analysis;
- formatting or linting checks;
- security scanning where actually used;
- packaging;
- deployment validation.

A green CI result does NOT automatically mean:

- all requirements are satisfied;
- all acceptance criteria are verified;
- the release is ready;
- the system has no defects.

CI proves only what its configured checks actually evaluate.

This file should make that boundary clear.

IMPORTANT:

- Everything inside HTML comments is Starter Kit guidance.
- Remove ALL instructional comments before the applicable phase-gate submission.
- Examples are guidance only.
- Do not fabricate CI runs or claim checks exist when they do not.
-->

## CI System

<!--
TEAM CONTENT REQUIRED

Describe the actual CI system used.

Examples might include:

- GitHub Actions;
- GitLab CI;
- Azure Pipelines;
- another configured system.

Identify:

- workflow or pipeline name;
- trigger conditions;
- repository location;
- what checks it performs.

Replace this comment with the team's actual CI setup.
-->

**CI Platform:**  
**Workflow / Pipeline:**  
**Configuration Location:**  

## CI Checks

<!--
TEAM CONTENT REQUIRED

Document important checks actually performed by CI.

Do not list hypothetical checks.

EXAMPLE ONLY:

| Check | Purpose | Command / Mechanism | Required to Pass? |
|---|---|---|---|
| Unit tests | Verify isolated application logic | pytest | Yes |
| Integration tests | Verify service and persistence interaction | pytest integration suite | Yes |

DELETE the example and populate actual CI checks below.
-->

| Check | Purpose | Command / Mechanism | Required to Pass? |
|---|---|---|---|
|  |  |  |  |

## Trigger Conditions

<!--
TEAM CONTENT REQUIRED

Explain when CI runs.

Examples:

- every pull request;
- push to main;
- manual workflow;
- release tag.

Explain why important checks run before or after merge.

Replace this comment with the team's actual trigger behavior.
-->

## CI Run Evidence

<!--
TEAM CONTENT REQUIRED

Record significant CI executions.

You do not need to record every development run.

Preserve runs meaningful to:

- phase-gate evidence;
- pull-request approval;
- release candidate;
- regression verification;
- deployment.

Use stable evidence IDs when useful:

CI-###

EXAMPLE ONLY:

| Evidence ID | Date | Commit / PR | Workflow | Result | Evidence Link / Reference | Purpose |
|---|---|---|---|---|---|---|
| CI-001 | YYYY-MM-DD | PR #21 | Build and Test | Passed | GitHub Actions run | Release candidate verification |

DELETE the example and populate actual CI runs below.
-->

| Evidence ID | Date | Commit / PR | Workflow | Result | Evidence Link / Reference | Purpose |
|---|---|---|---|---|---|---|
|  |  |  |  |  |  |  |

## Test Results

<!--
TEAM CONTENT REQUIRED WHEN CI EXECUTES TESTS

Summarize what tests actually ran.

Do not write only:

"CI passed."

Identify meaningful test categories and result counts where available.

EXAMPLE ONLY:

| CI Evidence ID | Test Type | Executed | Passed | Failed | Skipped | Notes |
|---|---|---:|---:|---:|---:|---|
| CI-001 | Unit | 42 | 42 | 0 | 0 | All unit tests passed |
| CI-001 | Integration | 12 | 12 | 0 | 0 | Test database used |

DELETE the example and populate actual evidence below.
-->

| CI Evidence ID | Test Type | Executed | Passed | Failed | Skipped | Notes |
|---|---|---:|---:|---:|---:|---|
|  |  |  |  |  |  |  |

## Failed CI Runs

<!--
TEAM CONTENT REQUIRED WHEN A SIGNIFICANT CI RUN FAILS

A failed CI run is useful engineering evidence.

Do not hide it.

Record:

- what failed;
- why;
- whether the failure identified a defect or environment problem;
- what action was taken;
- whether a later run confirmed resolution.

EXAMPLE ONLY:

| CI Evidence ID | Failure | Cause | Action | Resolution Evidence |
|---|---|---|---|---|
| CI-004 | Integration test failure | Persistence schema mismatch | Migration corrected | CI-005 |

DELETE the example and populate actual significant failures below.

A blank table is correct when no meaningful recorded failure exists.
-->

| CI Evidence ID | Failure | Cause | Action | Resolution Evidence |
|---|---|---|---|---|
|  |  |  |  |  |

## CI-to-Requirement Traceability

<!--
TEAM CONTENT REQUIRED WHEN CI PROVIDES REQUIREMENT OR ACCEPTANCE EVIDENCE

CI may execute tests that support acceptance criteria.

Reference:

/docs/testing/test-cases.md
/docs/planning/traceability.md

Do not claim that the entire CI pipeline verifies a requirement unless the
relationship is real.

EXAMPLE ONLY:

| CI Evidence ID | Test / Test Case | Related Requirement / Criterion | Result |
|---|---|---|---|
| CI-001 | TC-001 | REQ-001 / AC-REQ-001-01 | Passed |

DELETE the example and populate actual relationships below.
-->

| CI Evidence ID | Test / Test Case | Related Requirement / Criterion | Result |
|---|---|---|---|
|  |  |  |  |

## Branch / Merge Protection

<!--
TEAM CONTENT REQUIRED WHEN CI IS USED AS A MERGE CONTROL

Document whether CI is required before merge.

Possible controls include:

- required status checks;
- pull-request review;
- protected main branch;
- no direct pushes;
- test workflow required.

Do not claim repository protections that are not configured.

Replace this comment with actual repository behavior.
-->

## CI Limitations

<!--
TEAM CONTENT REQUIRED

CI has boundaries.

Examples ONLY:

- does not test external identity provider;
- does not test production configuration;
- does not exercise browser behavior;
- does not perform sustained-load testing;
- security scanning not configured;
- integration uses mock external dependency.

Do not imply CI provides broader assurance than it actually does.

Populate actual limitations below.
-->

| Limitation | Impact | Additional Verification |
|---|---|---|
|  |  |  |

## Release CI Evidence

<!--
TEAM CONTENT REQUIRED FOR RELEASE OR PHASE-GATE BASELINES

Identify the CI run supporting the actual release candidate.

Reference the same commit/tag used by:

/docs/release/release-notes.md
/docs/release/traceability-summary.md

Do not use a CI run from a different commit and present it as evidence for the
release baseline.
-->

**Release / Gate:**  
**Commit / Tag:**  
**CI Evidence ID:**  
**Result:**  

## CI Evidence Integrity

<!--
STARTER KIT GUIDANCE — DELETE BEFORE PHASE-GATE SUBMISSION

CI evidence is strongest when it is tied to the exact repository state being
reviewed.

A useful chain is:

Git Commit / PR
  ->
CI Workflow
  ->
Executed Tests / Checks
  ->
Results
  ->
Requirement / Acceptance Evidence
  ->
Release Baseline

Do not:

- claim a green run belongs to a different commit;
- omit skipped tests that matter;
- describe a failed check as passed;
- claim a CI check exists when it is not configured.
-->

<!--
FINAL STARTER KIT CHECK — DELETE BEFORE PHASE-GATE SUBMISSION

Before submission:

1. Identify the actual CI platform and configuration.
2. List only checks CI really performs.
3. Record meaningful CI runs tied to specific commits or PRs.
4. Preserve significant failed-run evidence and resolution.
5. Report test counts or categories when available.
6. Link CI tests to requirements only where the relationship is real.
7. Document branch or merge controls only if actually configured.
8. Identify CI limitations honestly.
9. Confirm release CI evidence matches the exact release baseline.
10. Remove ALL instructional HTML comments.

The completed artifact should show exactly what automated evidence CI produced
and, equally importantly, what that evidence does not prove.
-->
