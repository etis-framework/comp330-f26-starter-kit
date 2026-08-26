# Release Readiness Review

<!--
STARTER KIT GUIDANCE — DELETE BEFORE PHASE-GATE SUBMISSION

This file records the team's review of whether a specific release is ready for
the intended phase gate, demonstration, deployment, or delivery.

A release-readiness review should answer:

"Based on the available engineering evidence, are we ready to release this
specific baseline?"

This is NOT merely a checklist asking whether files exist.

Readiness should consider:

- scope;
- requirements;
- acceptance criteria;
- traceability;
- verification;
- defects;
- known limitations;
- architecture;
- operations;
- observability;
- deployment readiness;
- unresolved risks;
- release identification.

Reference authoritative release evidence in:

/docs/release/
/docs/quality/
/docs/operations/
/docs/observability/
/docs/planning/traceability.md

IMPORTANT:

- Everything inside HTML comments is Starter Kit guidance.
- Remove ALL instructional comments before the applicable phase-gate submission.
- Do not declare readiness without supporting evidence.
-->

## Review Identification

**Review Date:**  
**Release / Version:**  
**Git Tag / Commit:**  
**Target Gate / Milestone:**  
**Deployment / Environment:**  
**Reviewer(s):**  

<!--
TEAM CONTENT REQUIRED

Identify the exact release baseline being reviewed.

The release identification should agree with:

/docs/release/release-notes.md
/docs/release/traceability-summary.md

Do not review an ambiguous or moving code baseline.
-->

## Intended Release Outcome

<!--
TEAM CONTENT REQUIRED

State what this release is expected to accomplish.

Keep this concise.

Reference the current scope and release notes rather than duplicating them.

Replace this comment with the actual release objective.
-->

## Readiness Summary

<!--
TEAM CONTENT REQUIRED

Provide a concise status summary.

Do NOT complete this section until the detailed review below has been performed.

Suggested final outcomes:

- Ready
- Ready with Accepted Limitations
- Conditionally Ready
- Not Ready

Replace this comment with the actual evidence-based summary.
-->

**Readiness Outcome:**  

## Scope Readiness

<!--
TEAM CONTENT REQUIRED

Review whether the release matches the intended delivery scope.

Reference:

/docs/planning/scope.md
/docs/release/release-notes.md

Questions include:

- Are committed release capabilities present?
- Are deferred items explicitly identified?
- Has scope changed without being documented?
- Are out-of-scope expectations being represented accurately?

Populate actual evidence below.
-->

| Review Item | Evidence | Result | Gap / Action |
|---|---|---|---|
| Release scope matches current baseline |  |  |  |
| Deferred capabilities are identified |  |  |  |
| Release notes accurately describe delivered scope |  |  |  |

## Requirements and Traceability Readiness

<!--
TEAM CONTENT REQUIRED

Review:

/docs/release/traceability-summary.md
/docs/planning/traceability.md

Confirm that important release requirements connect to:

- acceptance criteria;
- architecture / design;
- implementation;
- verification.

A gap does not automatically mean the release must fail, but it must be visible
and evaluated.
-->

| Review Item | Evidence | Result | Gap / Action |
|---|---|---|---|
| Release requirements identified |  |  |  |
| Acceptance criteria linked |  |  |  |
| Implementation traceability present |  |  |  |
| Verification traceability present |  |  |  |
| Remaining traceability gaps understood |  |  |  |

## Verification Readiness

<!--
TEAM CONTENT REQUIRED

Review actual verification evidence.

Consider:

- automated tests;
- integration tests;
- acceptance criteria;
- runtime evidence;
- regression tests;
- manual verification where appropriate.

Do not claim "testing complete" because tests exist.

Ask whether important release behavior has actually been exercised and whether
results support the release claim.
-->

| Verification Area | Evidence | Result | Remaining Concern |
|---|---|---|---|
|  |  |  |  |

## Defect Readiness

<!--
TEAM CONTENT REQUIRED

Reference:

/docs/quality/defect-log.md
/docs/quality/defect-review.md

Review:

- open defects;
- severity;
- unresolved high-impact defects;
- deferred defects;
- regression verification;
- recurring quality patterns.

Do not require zero defects automatically.

The engineering question is whether remaining defects are understood and
acceptable for this release.
-->

| Defect / Concern | Severity / Impact | Disposition | Release Decision |
|---|---|---|---|
|  |  |  |  |

## Known Limitations

<!--
TEAM CONTENT REQUIRED

Reference:

/docs/release/known-limitations.md

Confirm:

- important limitations are visible;
- limitations are accurately described;
- workarounds are real;
- verification gaps are represented;
- the release claim does not contradict known limitations.
-->

| Limitation ID | Impact on Release | Accepted? | Rationale / Action |
|---|---|---|---|
|  |  |  |  |

## Architecture Readiness

<!--
TEAM CONTENT REQUIRED

Reference:

/docs/review/architecture-review.md

Confirm whether architecture issues materially affect release readiness.

Do not repeat the complete architecture review.
-->

| Architecture Concern | Evidence | Release Impact | Action |
|---|---|---|---|
|  |  |  |  |

## Operational Readiness

<!--
TEAM CONTENT REQUIRED

Reference:

/docs/operations/runbook.md
/docs/operations/incident-response-notes.md

Consider:

- deployment procedure;
- configuration;
- dependencies;
- startup;
- recovery;
- rollback where relevant;
- known operational limitations.

Do not claim operational readiness for procedures that have never been tested
when testing would be important.
-->

| Operational Area | Evidence | Result | Gap / Action |
|---|---|---|---|
| Deployment / startup |  |  |  |
| Post-deployment verification |  |  |  |
| Dependencies |  |  |  |
| Recovery / rollback |  |  |  |

## Observability Readiness

<!--
TEAM CONTENT REQUIRED

Reference:

/docs/observability/observability-plan.md
/docs/observability/metrics-notes.md
/docs/observability/runtime-evidence.md

Ask whether the team has enough runtime visibility to detect and investigate
important release failures.

Enterprise monitoring is not required.

Appropriate visibility for the actual system is.
-->

| Observability Area | Evidence | Result | Gap / Action |
|---|---|---|---|
|  |  |  |  |

## Risk Review

<!--
TEAM CONTENT REQUIRED

Reference:

/docs/planning/risk-register.md

Identify active risks that materially affect release readiness.

Do not recreate the full risk register.
-->

| Risk ID | Release Exposure | Mitigation / Response | Accepted for Release? |
|---|---|---|---|
|  |  |  |  |

## Demonstration Readiness

<!--
TEAM CONTENT REQUIRED WHEN A RELEASE DEMONSTRATION IS PART OF THE GATE

Reference:

/docs/release/demo-script.md

Consider:

- demo baseline matches release baseline;
- required environment available;
- scenarios verified;
- negative-path behavior represented where appropriate;
- limitations acknowledged;
- fallback evidence available.

Remove this section if no demonstration is relevant.
-->

| Review Item | Evidence | Result | Gap / Action |
|---|---|---|---|
|  |  |  |  |

## Blocking Issues

<!--
TEAM CONTENT REQUIRED

List only issues that prevent readiness.

A blank table means no blocking issue has been identified.

Do not put minor follow-up work here.

Use stable IDs if useful:

RRB-###

EXAMPLE ONLY:

| ID | Blocking Issue | Evidence | Owner | Required Resolution |
|---|---|---|---|---|
| RRB-001 | Critical acceptance criterion has no verification evidence | AC-REQ-008-02 | Quality & Review Lead | Execute and document verification |

DELETE the example and populate actual blockers below.
-->

| ID | Blocking Issue | Evidence | Owner | Required Resolution |
|---|---|---|---|---|
|  |  |  |  |  |

## Non-Blocking Follow-Up

<!--
TEAM CONTENT REQUIRED WHEN RELEASE CAN PROCEED WITH OPEN WORK

Record work that should continue but does not prevent the current release.

Do not hide material limitations here merely to obtain a Ready decision.
-->

| Follow-Up | Owner | Target | Related Evidence |
|---|---|---|---|
|  |  |  |  |

## Final Readiness Decision

<!--
TEAM CONTENT REQUIRED

Choose one:

Ready
- Evidence supports the intended release with no material unresolved blocker.

Ready with Accepted Limitations
- Release can proceed and known limitations are explicitly understood and accepted.

Conditionally Ready
- Release may proceed only after specified conditions are satisfied.

Not Ready
- One or more material blockers prevent the intended release.

State the decision and WHY.

Do not select Ready simply because the phase-gate date has arrived.
-->

**Decision:**  

**Rationale:**  

## Required Conditions / Approvals

<!--
TEAM CONTENT REQUIRED ONLY WHEN APPLICABLE

If the decision is Conditionally Ready, identify the conditions that must be
satisfied.

If no conditions apply, remove this section.
-->

| Condition | Owner | Evidence Required | Status |
|---|---|---|---|
|  |  |  |  |

<!--
FINAL STARTER KIT CHECK — DELETE BEFORE PHASE-GATE SUBMISSION

Before submission:

1. Confirm the reviewed Git tag / commit is the actual release baseline.
2. Confirm release-notes.md identifies the same baseline.
3. Base readiness on evidence, not artifact existence.
4. Review open defects and known limitations honestly.
5. Confirm verification claims point to actual evidence.
6. Confirm operational and observability readiness are proportional to the system.
7. Review release risks.
8. Identify real blockers explicitly.
9. State the final readiness decision and rationale.
10. Remove ALL instructional HTML comments.

The completed review should answer one question clearly:

"Does the available engineering evidence support releasing this exact baseline?"
-->
