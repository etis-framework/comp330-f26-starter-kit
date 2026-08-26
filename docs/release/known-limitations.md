# Known Limitations

<!--
STARTER KIT GUIDANCE — DELETE BEFORE PHASE-GATE SUBMISSION

This file records limitations the team KNOWS exist in the current release.

A known limitation is not necessarily a defect.

Examples may include:

- intentionally deferred functionality;
- supported behavior with a known restriction;
- operational constraint;
- scale limitation;
- unsupported scenario;
- incomplete recovery capability;
- environment limitation;
- dependency limitation;
- known defect that remains unresolved.

The purpose is to make limitations explicit so reviewers and users do not need
to discover them by accident.

Do NOT hide limitations merely because they make the release appear less
complete.

Do NOT invent limitations to populate this file.

IMPORTANT:

- Everything inside HTML comments is Starter Kit guidance.
- Remove ALL instructional comments before the applicable phase-gate submission.
- Examples are guidance only.
-->

## Current Limitations

<!--
TEAM CONTENT REQUIRED

Use stable identifiers:

LIM-###

Examples:

LIM-001
LIM-002

COLUMN GUIDANCE

Limitation
State clearly what the system currently cannot do or what restriction exists.

Impact
Explain the practical consequence.

Affected Area
Examples:
- requirement;
- capability;
- architecture;
- API;
- deployment;
- operations;
- performance;
- security.

Workaround
Describe a real workaround if one exists.

Disposition
State what the team intends to do.

Suggested values:
- Planned Fix
- Planned Improvement
- Deferred
- Accepted
- External Constraint
- Under Investigation

Related Evidence
Reference defects, requirements, risks, issues, tasks, or decisions.

EXAMPLE ONLY:

| ID | Limitation | Impact | Affected Area | Workaround | Disposition | Related Evidence |
|---|---|---|---|---|---|---|
| LIM-001 | Workflow history is not retained beyond the current deployment database | Historical review depends on current environment persistence | Operations | None | Planned Improvement | R-004 |

DELETE the example and populate the actual table below.
-->

| ID | Limitation | Impact | Affected Area | Workaround | Disposition | Related Evidence |
|---|---|---|---|---|---|---|
|  |  |  |  |  |  |  |

## Deferred Capabilities

<!--
TEAM CONTENT REQUIRED WHEN CAPABILITIES WERE INTENTIONALLY DEFERRED

A deferred capability is something the team intentionally decided not to
include in the current release.

Reference:

/docs/planning/scope.md

Do not create a second scope document.

Use this section only to identify deferred work relevant to understanding the
current release.

EXAMPLE ONLY:

| Capability | Reason Deferred | Impact on Current Release | Future Reference |
|---|---|---|---|
| Administrative reporting dashboard | Lower priority than core workflow verification | No administrative analytics in current release | SCP-007 |

Populate actual deferred capabilities below.

Remove this section if none exist.
-->

| Capability | Reason Deferred | Impact on Current Release | Future Reference |
|---|---|---|---|
|  |  |  |  |

## Unresolved Defects Affecting the Release

<!--
TEAM CONTENT REQUIRED WHEN OPEN DEFECTS REMAIN

Reference actual defects from:

/docs/quality/defect-log.md

Do not copy every open defect.

Include defects relevant enough that someone evaluating or using the release
should know about them.

EXAMPLE ONLY:

| Defect ID | Impact | Severity | Current Disposition |
|---|---|---|---|
| DEF-012 | Error message does not identify which optional integration failed | Low | Deferred |

Populate actual defects below.

Remove this section if no unresolved defects materially affect the release.
-->

| Defect ID | Impact | Severity | Current Disposition |
|---|---|---|---|
|  |  |  |  |

## Operational Limitations

<!--
TEAM CONTENT REQUIRED WHEN OPERATIONAL CONSTRAINTS EXIST

Examples may include:

- manual deployment;
- no automated rollback;
- limited health checks;
- backup recovery not yet tested;
- dependence on an external service;
- no automated alerting.

Reference:

/docs/operations/runbook.md
/docs/observability/observability-plan.md

Do not duplicate those documents.

Populate only limitations relevant to this release.
-->

| Limitation | Operational Impact | Related Evidence |
|---|---|---|
|  |  |  |

## Verification Limitations

<!--
TEAM CONTENT REQUIRED WHEN IMPORTANT VERIFICATION GAPS REMAIN

A release may have known gaps in evidence.

Examples:

- performance not tested under sustained load;
- recovery behavior not yet verified;
- one external integration verified only manually;
- insufficient data to establish a runtime baseline.

A verification gap is useful evidence when stated honestly.

Reference relevant acceptance criteria, runtime evidence, or traceability gaps.

Populate actual limitations below.
-->

| Limitation / Gap | What Has Been Verified | What Has Not Been Verified | Related Evidence |
|---|---|---|---|
|  |  |  |  |

## Limitation Changes

<!--
TEAM CONTENT REQUIRED WHEN A LIMITATION CHANGES MATERIALLY

Preserve useful history when a limitation is:

- resolved;
- reduced;
- expanded;
- accepted;
- deferred differently.

Do not silently delete a limitation that materially affected a prior release.

A blank table is intentional at project start.
-->

| Date / Release | Limitation ID | Change | Reason | Evidence |
|---|---|---|---|---|
|  |  |  |  |  |

## No Known Limitation Claims

<!--
STARTER KIT GUIDANCE — DELETE BEFORE PHASE-GATE SUBMISSION

Be cautious about writing:

"No known limitations."

That statement should mean the team has genuinely reviewed:

- scope;
- defects;
- verification gaps;
- operational constraints;
- risks;
- external dependencies.

It should not mean:

"We did not think about limitations."

If no material limitation is currently known, state that conclusion explicitly
in the finished artifact and identify the review basis when useful.
-->

<!--
FINAL STARTER KIT CHECK — DELETE BEFORE PHASE-GATE SUBMISSION

Before submission:

1. Record only actual known limitations.
2. Do not hide unresolved defects or verification gaps.
3. Distinguish limitations from defects and deferred scope.
4. Confirm limitation IDs are unique.
5. Confirm defect references exist in defect-log.md.
6. Confirm deferred capability references agree with scope.md.
7. Identify real workarounds only when they actually exist.
8. Preserve material limitation history when useful.
9. Remove unnecessary sections.
10. Remove ALL instructional HTML comments.

The completed file should clearly communicate what the current release cannot
yet do, cannot guarantee, or intentionally does not support.
-->
