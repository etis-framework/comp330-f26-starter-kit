# Defect Review

<!--
STARTER KIT GUIDANCE — DELETE BEFORE PHASE-GATE SUBMISSION

This file is used to periodically review the team's accumulated defect evidence
for patterns, recurring causes, quality weaknesses, and engineering
improvements.

This is different from:

/docs/quality/defect-log.md

The defect log records INDIVIDUAL defects.

The defect review asks what the COLLECTION of defects tells the team about the
system and its engineering process.

A defect review may reveal:

- recurring failure categories;
- weak requirements;
- missing acceptance criteria;
- architecture problems;
- interface-contract problems;
- repeated implementation mistakes;
- inadequate review;
- test gaps;
- deployment weaknesses;
- observability gaps;
- areas of growing technical debt.

Do NOT invent defects or trends merely to complete this artifact.

If the project has too few defects to support meaningful analysis, state that
fact rather than manufacturing conclusions.

IMPORTANT:

- Everything inside HTML comments is Starter Kit guidance.
- Remove all instructional comments before the applicable phase-gate submission.
- Examples inside comments are guidance only.
-->

## Review Scope

<!--
TEAM CONTENT REQUIRED

State what defect evidence this review covers.

Examples:

- defects since the previous phase gate;
- defects discovered during a release cycle;
- all open and closed defects through a given date.

Identify:

- review date;
- applicable phase gate or period;
- defects included;
- defects excluded, if any.

Replace this comment with the actual review scope.
-->

**Review Date:**  
**Review Period / Gate:**  
**Defects Reviewed:**  

## Defect Summary

<!--
TEAM CONTENT REQUIRED

Summarize the defect population being reviewed.

Use actual counts from defect-log.md.

Do not create counts that cannot be reconciled with the authoritative defect
log.

EXAMPLE ONLY:

| Measure | Count |
|---|---:|
| Total defects reviewed | 8 |
| Open | 2 |
| Closed | 5 |
| Deferred | 1 |
| Critical / High severity | 1 |

Populate the actual table below.
-->

| Measure | Count |
|---|---:|
| Total defects reviewed |  |
| Open |  |
| Closed |  |
| Deferred |  |
| Critical / High severity |  |

## Defect Distribution

<!--
TEAM CONTENT REQUIRED WHEN ENOUGH DEFECTS EXIST TO SUPPORT ANALYSIS

Group defects in ways that help reveal engineering patterns.

Possible categories include:

- requirements;
- architecture;
- implementation;
- interface / integration;
- validation;
- security;
- test;
- deployment;
- operations;
- documentation.

Do not force every project to use these exact categories.

Use categories meaningful to your actual defect evidence.

EXAMPLE ONLY:

| Category | Defect IDs | Count | Observation |
|---|---|---:|---|
| Input validation | DEF-001, DEF-004 | 2 | Similar boundary conditions were missed in two workflows |

Populate the actual table below, or remove the section if the defect population
is too small for meaningful categorization.
-->

| Category | Defect IDs | Count | Observation |
|---|---|---:|---|
|  |  |  |  |

## Recurring Patterns

<!--
TEAM CONTENT REQUIRED WHEN EVIDENCE SUPPORTS A PATTERN

Identify recurring patterns across multiple defects.

A pattern should be supported by evidence.

Examples ONLY:

- multiple defects involve missing negative-path validation;
- defects repeatedly occur at the same component boundary;
- several defects trace back to ambiguous acceptance criteria;
- integration defects appear because API assumptions were not documented;
- defects are being discovered late because review occurs only after merge.

Do not claim a pattern based on a single defect unless there is other supporting
evidence.

If no meaningful pattern exists yet, state that explicitly in the finished
artifact.
-->

| Pattern | Supporting Defects / Evidence | Engineering Significance |
|---|---|---|
|  |  |  |

## Contributing Factors

<!--
TEAM CONTENT REQUIRED

Look beyond the immediate code-level cause.

Consider whether defects were enabled or made harder to detect by:

- unclear requirements;
- weak acceptance criteria;
- incorrect assumptions;
- architecture boundaries;
- incomplete API contracts;
- missing review;
- inadequate testing;
- poor test data;
- configuration differences;
- observability limitations;
- schedule pressure;
- insufficient knowledge sharing.

Do not assign blame to individuals.

Focus on system and process conditions that the team can improve.
-->

| Contributing Factor | Supporting Evidence | Effect |
|---|---|---|
|  |  |  |

## Defect Escape Analysis

<!--
TEAM CONTENT REQUIRED WHEN RELEVANT

A defect "escapes" when it is discovered later than the engineering activity
that ideally should have detected it.

Examples:

- implementation defect should have been found by unit testing but was found
  during integration;
- contract mismatch should have been found during design review but was found
  after deployment;
- requirement ambiguity was discovered only during acceptance verification.

This is NOT about blaming the person who created the defect.

The engineering question is:

"Where could we have detected this earlier?"

EXAMPLE ONLY:

| Defect ID | Detected At | Earlier Detection Opportunity | Improvement |
|---|---|---|---|
| DEF-003 | Integration test | API contract review | Add explicit failure response to API contract |

Populate actual escapes below where useful.

If no useful escape analysis exists, remove this section.
-->

| Defect ID | Detected At | Earlier Detection Opportunity | Improvement |
|---|---|---|---|
|  |  |  |  |

## Quality Strengths

<!--
TEAM CONTENT REQUIRED

Defect review should not look only for weaknesses.

Identify evidence of practices that are working.

Examples ONLY:

- peer review found defects before merge;
- negative-path acceptance criteria exposed important failures;
- automated regression tests prevented recurrence;
- architecture boundaries limited defect impact;
- observability reduced investigation time.

Use actual evidence.
-->

| Strength | Supporting Evidence | Why It Matters |
|---|---|---|
|  |  |  |

## Improvement Actions

<!--
TEAM CONTENT REQUIRED

Turn meaningful defect-review findings into concrete engineering actions.

Avoid vague actions such as:

- "test more";
- "be more careful";
- "write better code."

Prefer actions such as:

- add negative-path acceptance criteria for all state-changing operations;
- introduce contract tests for API-003;
- require peer review of persistence changes;
- add regression test for DEF-007;
- clarify REQ-012;
- revise ADR-004 based on repeated failure evidence.

Use stable action IDs when useful:

QA-###

Examples:

QA-001
QA-002

EXAMPLE ONLY:

| Action ID | Improvement | Evidence / Driver | Owner | Target | Status |
|---|---|---|---|---|---|
| QA-001 | Add negative-path review to acceptance-criteria preparation | DEF-001, DEF-004 | Quality & Review Lead | A4 | Planned |

DELETE the example and populate actual actions below.
-->

| Action ID | Improvement | Evidence / Driver | Owner | Target | Status |
|---|---|---|---|---|---|
|  |  |  |  |  |  |

## Engineering Evidence to Update

<!--
TEAM CONTENT REQUIRED

Defect patterns may require changes beyond implementation.

Review whether findings require updates to:

- requirements;
- acceptance criteria;
- assumptions;
- risk register;
- architecture;
- component responsibilities;
- API contracts;
- ADRs;
- tests;
- task plan;
- observability;
- runbook;
- other engineering evidence.

Populate only artifacts actually affected.
-->

| Finding / Defect | Artifact / Evidence | Required Update | Owner | Status |
|---|---|---|---|---|
|  |  |  |  |  |

## Previous Review Actions

<!--
TEAM CONTENT REQUIRED AFTER THE FIRST DEFECT REVIEW

If prior reviews created quality-improvement actions, evaluate whether those
actions were completed and whether they helped.

Do not simply carry improvement actions forward indefinitely without checking
their effect.

At the first review, this section may be removed.
-->

| Action ID | Previous Action | Status | Evidence of Effectiveness | Follow-Up |
|---|---|---|---|---|
|  |  |  |  |  |

## Review Conclusion

<!--
TEAM CONTENT REQUIRED

Summarize what the defect evidence currently says about project quality.

A useful conclusion may address:

- whether defects are concentrated in a particular area;
- whether detection is occurring early or late;
- whether severity is changing;
- whether previous improvements are working;
- what quality concern deserves the most attention next.

Do not write "quality is good" without supporting evidence.

If too little evidence exists for a meaningful conclusion, state that
explicitly.
-->

<!--
FINAL STARTER KIT CHECK — DELETE BEFORE PHASE-GATE SUBMISSION

Before submission:

1. Confirm all counts reconcile with defect-log.md.
2. Base patterns on actual defects rather than hypothetical concerns.
3. Avoid assigning blame to individuals.
4. Distinguish immediate defect causes from deeper contributing factors.
5. Identify earlier detection opportunities where useful.
6. Convert meaningful findings into concrete improvement actions.
7. Update related engineering evidence when defect analysis exposes a weakness.
8. Evaluate previous quality actions when prior review evidence exists.
9. State explicitly when insufficient defect evidence exists for a conclusion.
10. Remove ALL instructional HTML comments.

The completed defect review should demonstrate that the team learns from
defects rather than merely fixing them one at a time.
-->
