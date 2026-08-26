# Release Traceability Summary

<!--
STARTER KIT GUIDANCE — DELETE BEFORE PHASE-GATE SUBMISSION

This file provides a RELEASE-LEVEL summary of engineering traceability.

It does NOT replace the project's broader traceability artifact:

/docs/planning/traceability.md

The planning traceability file evolves throughout the lifecycle.

This release traceability summary answers a narrower question:

"For the capabilities represented in this release, can we trace important
requirements through design / architecture, implementation, and verification?"

The summary should help a phase-gate reviewer quickly identify:

- what requirements are represented in the release;
- how they connect to acceptance criteria;
- where they are implemented;
- how they were verified;
- what evidence remains incomplete;
- what limitations affect release claims.

Do not manufacture links to make the release appear complete.

A visible traceability gap is stronger engineering evidence than a fictional
verification reference.

IMPORTANT:

- Everything inside HTML comments is Starter Kit guidance.
- Remove ALL instructional comments before the applicable phase-gate submission.
- Examples are guidance only.
-->

## Release Identification

**Release / Version:**  
**Git Tag / Commit:**  
**Release Gate / Milestone:**  

<!--
TEAM CONTENT REQUIRED

Identify the exact release represented by this traceability summary.

Use the same release identification as:

/docs/release/release-notes.md
-->

## Requirements Coverage

<!--
TEAM CONTENT REQUIRED

Include requirements relevant to this release.

Do not necessarily include requirements explicitly deferred outside the current
release unless showing that deferred status is useful.

COLUMN GUIDANCE

Requirement
Requirement ID from requirements.md.

Acceptance Criteria
Applicable AC IDs.

Architecture / Design
Relevant component, API contract, ADR, or other design evidence.

Implementation
Repository path, module, PR, commit, or other implementation evidence.

Verification
Test, runtime evidence, review, or other verification evidence.

Release Status
Suggested values:
- Verified
- Implemented / Not Yet Verified
- Partial
- Deferred
- Not Included

Limitation / Gap
Reference LIM-### or another explicit gap when applicable.

EXAMPLE ONLY:

| Requirement | Acceptance Criteria | Architecture / Design | Implementation | Verification | Release Status | Limitation / Gap |
|---|---|---|---|---|---|---|
| REQ-001 | AC-REQ-001-01, AC-REQ-001-02 | API-001, Application Service | `src/workflow/` | Integration verification | Verified | None |

DELETE the example and populate the actual table below.
-->

| Requirement | Acceptance Criteria | Architecture / Design | Implementation | Verification | Release Status | Limitation / Gap |
|---|---|---|---|---|---|---|
|  |  |  |  |  |  |  |

## Acceptance-Criteria Coverage

<!--
TEAM CONTENT REQUIRED WHEN ADDITIONAL ACCEPTANCE-CRITERIA DETAIL IS USEFUL

Use this section when a single requirement has several criteria with different
verification outcomes.

Do not duplicate the Requirements Coverage table unnecessarily.

EXAMPLE ONLY:

| Acceptance Criterion | Verification Evidence | Result | Notes |
|---|---|---|---|
| AC-REQ-003-01 | `tests/integration/test_status.py` | Passed | Automated |
| AC-REQ-003-02 | RUN-012 | Partial | External dependency unavailable for one scenario |

Populate actual evidence when useful.

Remove this section if the Requirements Coverage table is sufficient.
-->

| Acceptance Criterion | Verification Evidence | Result | Notes |
|---|---|---|---|
|  |  |  |  |

## Architectural Decision Coverage

<!--
TEAM CONTENT REQUIRED FOR SIGNIFICANT DECISIONS AFFECTING THE RELEASE

Reference ADRs that materially shaped what was delivered.

The goal is to show that major release behavior can be traced back to explicit
engineering decisions where appropriate.

EXAMPLE ONLY:

| Decision | Release Impact | Implementation / Contract Evidence | Verification |
|---|---|---|---|
| ADR-003 | Defines persistence boundary used in release | Persistence Layer, API-004 | Integration tests |

Populate actual decisions below.

Remove this section if no ADR materially affects the release.
-->

| Decision | Release Impact | Implementation / Contract Evidence | Verification |
|---|---|---|---|
|  |  |  |  |

## Defect Traceability

<!--
TEAM CONTENT REQUIRED WHEN DEFECTS MATERIALLY AFFECT RELEASE EVIDENCE

Show important defects that:

- were fixed for the release;
- remain unresolved;
- exposed a requirement or verification gap.

Reference:

/docs/quality/defect-log.md

Do not list every trivial defect.
-->

| Defect ID | Related Requirement / Criterion | Release Disposition | Verification / Limitation |
|---|---|---|---|
|  |  |  |  |

## Traceability Gaps

<!--
TEAM CONTENT REQUIRED

Identify gaps that remain at release time.

Examples ONLY:

- requirement implemented but not independently verified;
- acceptance criterion has no runtime evidence;
- implementation exists but architecture reference is stale;
- requirement is only partially covered;
- external dependency prevented verification.

Do not hide gaps.

Reference:

/docs/release/known-limitations.md

where a gap materially limits the release.
-->

| Gap | Affected Evidence | Release Impact | Owner / Follow-Up | Related Limitation |
|---|---|---|---|---|
|  |  |  |  |  |

## Release Evidence Summary

<!--
TEAM CONTENT REQUIRED

Summarize the release's traceability position.

A useful conclusion might state:

- how many release requirements are verified;
- which are partial or deferred;
- whether significant gaps remain;
- whether limitations constrain release claims.

Do not reduce this to a percentage unless the percentage actually provides
useful information.

Do not claim "100% traceability" merely because every table cell contains text.

Traceability quality depends on meaningful, valid relationships.
-->

## Review Confirmation

<!--
TEAM CONTENT REQUIRED

Record who reviewed this release traceability summary and when.

The review should confirm that references point to actual evidence.

This does NOT require every team member to sign unless your team process says
otherwise.
-->

| Reviewer | Date | Review Result / Notes |
|---|---|---|
|  |  |  |

<!--
FINAL STARTER KIT CHECK — DELETE BEFORE PHASE-GATE SUBMISSION

Before submission:

1. Confirm release identification agrees with release-notes.md.
2. Include only actual release requirements.
3. Confirm acceptance-criteria IDs exist.
4. Confirm architecture and ADR references are valid.
5. Confirm implementation references point to actual code or repository evidence.
6. Confirm verification references represent work that actually occurred.
7. Identify partial or missing evidence explicitly.
8. Confirm limitations agree with known-limitations.md.
9. Confirm defects agree with defect-log.md.
10. Remove ALL instructional HTML comments.

The completed summary should allow a reviewer to move from release requirement
to engineering solution to verification evidence without reconstructing the
entire project history.
-->
