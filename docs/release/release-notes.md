# Release Notes

<!--
STARTER KIT GUIDANCE — DELETE BEFORE PHASE-GATE SUBMISSION

This file describes the release being presented or delivered.

Release notes should tell a reviewer:

- what release this is;
- what capabilities are included;
- what meaningful changes were made;
- what was verified;
- what defects were resolved;
- what remains limited or incomplete; and
- where supporting engineering evidence can be found.

Release notes are NOT a complete commit history.

Focus on changes and capabilities that matter to users, reviewers, operators,
or downstream engineering work.

IMPORTANT:

- Everything inside HTML comments is Starter Kit guidance.
- Remove ALL instructional comments before the applicable phase-gate submission.
- Examples inside comments are guidance only.
- Do not claim features, fixes, verification, or deployment results that do
  not actually exist.
-->

## Release Identification

**Release / Version:**  
**Release Date:**  
**Release Gate / Milestone:**  
**Git Tag / Commit:**  
**Deployment / Environment:**  

<!--
TEAM CONTENT REQUIRED

Identify the actual release.

Use the Git tag, commit, deployment, or other repository-visible identifier
that defines exactly what code and evidence this release represents.

Do not leave placeholder metadata in the completed artifact.

If a field does not apply, remove it rather than leaving it blank.
-->

## Release Summary

<!--
TEAM CONTENT REQUIRED

Provide a short summary of the release.

Explain:

- the primary purpose of this release;
- the most important capabilities now available; and
- the overall maturity or readiness represented by the release.

Keep this concise.

Do not repeat the entire scope or requirements document.

Replace this comment with the team's actual release summary.
-->

## Included Capabilities

<!--
TEAM CONTENT REQUIRED

Identify meaningful capabilities included in this release.

Reference related requirements where useful.

Do not list every small code change.

EXAMPLE ONLY:

| Capability | Related Requirements | Release Status |
|---|---|---|
| Authenticated workflow submission | REQ-001, REQ-003 | Included and verified |

Delete the example and populate the actual table below.
-->

| Capability | Related Requirements | Release Status |
|---|---|---|
|  |  |  |

## Significant Changes

<!--
TEAM CONTENT REQUIRED

Summarize meaningful changes since the previous release or baseline.

Possible categories include:

- new capability;
- changed behavior;
- architectural change;
- interface change;
- security improvement;
- reliability improvement;
- operational improvement;
- documentation or evidence improvement.

Do not reproduce the Git commit log.

EXAMPLE ONLY:

| Area | Change | Why It Matters | Related Evidence |
|---|---|---|---|
| Workflow validation | Added server-side required-field validation | Prevents invalid workflow records from being created | REQ-004, AC-REQ-004-02, PR #21 |

Populate actual changes below.
-->

| Area | Change | Why It Matters | Related Evidence |
|---|---|---|---|
|  |  |  |  |

## Verification Summary

<!--
TEAM CONTENT REQUIRED

Summarize the evidence supporting this release.

Do not copy the entire test plan or traceability matrix.

Reference authoritative verification evidence.

Consider:

- automated tests;
- acceptance verification;
- integration tests;
- runtime evidence;
- defect verification;
- deployment checks;
- observability evidence.

Do not claim "all tests passed" unless the supporting evidence exists.

EXAMPLE ONLY:

| Verification Area | Result | Evidence |
|---|---|---|
| Workflow submission acceptance criteria | Passed | AC-REQ-001-01, AC-REQ-001-02, test report |

Populate actual evidence below.
-->

| Verification Area | Result | Evidence |
|---|---|---|
|  |  |  |

## Defects Resolved

<!--
TEAM CONTENT REQUIRED WHEN DEFECTS WERE RESOLVED

Reference actual defects from:

/docs/quality/defect-log.md

Do not invent defects merely to populate release notes.

If no tracked defects were resolved in this release, state that in the finished
artifact or remove this section.
-->

| Defect ID | Summary | Resolution Evidence |
|---|---|---|
|  |  |  |

## Known Limitations

<!--
TEAM CONTENT REQUIRED

Summarize only the most important limitations affecting this release.

The authoritative detailed record is:

/docs/release/known-limitations.md

Do not duplicate the entire limitations file.

Reference limitation IDs where possible.
-->

| Limitation ID | Summary | Impact |
|---|---|---|
|  |  |  |

## Deployment / Operational Notes

<!--
TEAM CONTENT REQUIRED WHEN THE RELEASE IS DEPLOYED OR OPERATED

Document release-specific operational information that a reviewer or operator
needs to know.

Examples might include:

- deployment completed successfully;
- configuration change required;
- database migration performed;
- service restart required;
- first-run behavior;
- environment-specific limitation.

Do not duplicate the complete runbook.

Reference:

/docs/operations/runbook.md

Remove this section if there is no release-specific operational information.
-->

## Compatibility / Migration Notes

<!--
TEAM CONTENT REQUIRED ONLY WHEN RELEVANT

Document any change that affects:

- existing data;
- API consumers;
- configuration;
- deployment;
- external integrations;
- previously supported behavior.

If no compatibility or migration concern exists, remove this section.
-->

## Evidence References

<!--
TEAM CONTENT REQUIRED

Provide concise references to the most important release evidence.

Possible references include:

- requirements;
- acceptance criteria;
- traceability-summary.md;
- test evidence;
- runtime evidence;
- defect log;
- ADRs;
- pull requests;
- release tag;
- deployment evidence.

Do not create a giant index of the repository.

Reference evidence most useful for reviewing this release.
-->

| Evidence | Location / Reference | Purpose |
|---|---|---|
|  |  |  |

<!--
FINAL STARTER KIT CHECK — DELETE BEFORE PHASE-GATE SUBMISSION

Before submission:

1. Complete the actual release identification.
2. Confirm the Git tag / commit identifies the release being described.
3. Include only capabilities actually present in the release.
4. Confirm verification statements point to real evidence.
5. Confirm resolved defects exist in defect-log.md.
6. Confirm limitations agree with known-limitations.md.
7. Remove unsupported claims about readiness or quality.
8. Remove sections that genuinely do not apply.
9. Remove ALL instructional HTML comments.

The completed release notes should accurately describe what was delivered,
what changed, what was verified, and what remains limited.
-->
