# Architecture Review

<!--
STARTER KIT GUIDANCE — DELETE BEFORE PHASE-GATE SUBMISSION

This file records a review of the project's current architecture.

An architecture review should evaluate whether the architecture is appropriate
for the requirements, constraints, risks, quality concerns, and evidence
currently available.

The goal is NOT to ask:

"Does the architecture diagram look complete?"

The goal is to ask questions such as:

- Does the architecture address important requirements?
- Are component responsibilities clear?
- Are important interfaces and dependencies understood?
- Are architectural assumptions visible?
- Are important failure and security boundaries explicit?
- Are significant architectural decisions justified?
- Are there contradictions among architecture artifacts?
- What risks or unresolved questions remain?
- What must change before the architecture can be considered ready?

Reference the authoritative architecture evidence in:

/docs/architecture/architecture.md
/docs/architecture/component-responsibilities.md
/docs/architecture/api-contracts.md
/docs/decisions/

IMPORTANT:

- Everything inside HTML comments is Starter Kit guidance.
- Remove ALL instructional comments before the applicable phase-gate submission.
- Examples inside comments are guidance only.
- Do not claim that an architecture was reviewed if the review did not occur.
-->

## Review Identification

**Review Date:**  
**Applicable Gate / Milestone:**  
**Architecture Baseline / Commit:**  
**Reviewer(s):**  

<!--
TEAM CONTENT REQUIRED

Identify exactly what architecture baseline was reviewed.

Where practical, reference:

- Git commit;
- branch;
- phase-gate baseline;
- architecture version.

Do not leave placeholder metadata in the completed review.
-->

## Review Scope

<!--
TEAM CONTENT REQUIRED

Describe what was included in this review.

Possible evidence may include:

- architecture.md;
- architecture diagram;
- component-responsibilities.md;
- api-contracts.md;
- ADRs;
- requirements;
- acceptance criteria;
- assumptions;
- risk register.

Also identify anything explicitly excluded.

Replace this comment with the actual review scope.
-->

## Architecture Summary

<!--
TEAM CONTENT REQUIRED

Briefly summarize the architecture being reviewed.

Do not reproduce architecture.md.

Capture only enough context for the review findings to make sense.

Replace this comment with the actual summary.
-->

## Review Criteria

<!--
TEAM CONTENT REQUIRED

Identify the criteria used to evaluate the architecture.

Use only criteria that matter to the project.

Possible areas include:

- requirements alignment;
- separation of responsibilities;
- interface clarity;
- data ownership;
- security;
- reliability;
- maintainability;
- testability;
- deployability;
- observability;
- failure handling;
- operational support;
- scalability;
- traceability.

EXAMPLE ONLY:

| Review Area | Review Question | Related Evidence |
|---|---|---|
| Requirements alignment | Does the architecture provide a credible path to satisfy the current requirements? | requirements.md, architecture.md |
| Responsibility boundaries | Are important component responsibilities and non-responsibilities explicit? | component-responsibilities.md |

Delete the example and populate the actual table below.
-->

| Review Area | Review Question | Related Evidence |
|---|---|---|
|  |  |  |

## Findings

<!--
TEAM CONTENT REQUIRED

Record actual review findings.

Use stable identifiers:

ARF-###

Examples:

ARF-001
ARF-002

Finding Type may include:

- Strength
- Concern
- Gap
- Risk
- Question
- Required Change

Severity / Importance should use a simple team-defined scale when useful.

Suggested values:

- High
- Medium
- Low

Do not manufacture findings merely to populate the review.

EXAMPLE ONLY:

| ID | Type | Finding | Importance | Evidence | Required Action |
|---|---|---|---|---|---|
| ARF-001 | Concern | Authorization responsibility is described in architecture.md but not explicitly assigned in component-responsibilities.md | Medium | Architecture / component responsibility comparison | Clarify authoritative authorization boundary |

DELETE the example and populate actual findings below.
-->

| ID | Type | Finding | Importance | Evidence | Required Action |
|---|---|---|---|---|---|
|  |  |  |  |  |  |

## Requirements Alignment

<!--
TEAM CONTENT REQUIRED

Evaluate whether important requirements have a plausible architectural
realization.

Do not attempt to duplicate the complete traceability matrix.

Focus on architectural relationships significant enough to review.

EXAMPLE ONLY:

| Requirement / Concern | Architectural Response | Review Result | Gap / Action |
|---|---|---|---|
| REQ-001 | Web Client -> Application Service -> Persistence Layer | Adequate | None |

Populate actual evidence below.
-->

| Requirement / Concern | Architectural Response | Review Result | Gap / Action |
|---|---|---|---|
|  |  |  |  |

## Component and Responsibility Review

<!--
TEAM CONTENT REQUIRED

Review whether component boundaries are clear enough to prevent:

- duplicated responsibility;
- missing responsibility;
- ambiguous ownership;
- security responsibility leakage;
- architectural coupling that contradicts the intended design.

Reference:

/docs/architecture/component-responsibilities.md

Populate findings only where useful.
-->

| Component / Boundary | Review Result | Concern / Strength | Action |
|---|---|---|---|
|  |  |  |  |

## Interface and Dependency Review

<!--
TEAM CONTENT REQUIRED

Review important interfaces and dependencies.

Consider:

- consumer/provider clarity;
- input/output expectations;
- failure behavior;
- security expectations;
- external dependencies;
- compatibility concerns.

Reference:

/docs/architecture/api-contracts.md
-->

| Interface / Dependency | Review Result | Concern / Strength | Action |
|---|---|---|---|
|  |  |  |  |

## Quality Attribute Review

<!--
TEAM CONTENT REQUIRED

Evaluate quality concerns that actually matter to the architecture.

Examples may include:

- security;
- maintainability;
- reliability;
- testability;
- performance;
- deployability;
- recoverability;
- observability.

Do not include a quality merely because it appears in this comment.

EXAMPLE ONLY:

| Quality Concern | Current Architectural Support | Evidence | Remaining Concern |
|---|---|---|---|
| Testability | Business logic separated from presentation boundary | architecture.md, tests | Integration boundary still needs explicit contract tests |

Populate actual review evidence below.
-->

| Quality Concern | Current Architectural Support | Evidence | Remaining Concern |
|---|---|---|---|
|  |  |  |  |

## Architecture Risks and Open Questions

<!--
TEAM CONTENT REQUIRED

Reference rather than duplicate authoritative risks and open questions.

Relevant sources:

/docs/planning/risk-register.md
/docs/requirements/assumptions-open-questions.md

Capture only those that materially affect architecture readiness.
-->

| Risk / Question | Architectural Impact | Required Resolution / Monitoring |
|---|---|---|
|  |  |  |

## Decision Record Review

<!--
TEAM CONTENT REQUIRED

Review whether significant architectural choices have appropriate decision
evidence.

Reference ADRs from:

/docs/decisions/

Questions to consider:

- Was a meaningful choice made?
- Were alternatives considered?
- Are tradeoffs visible?
- Does the current architecture agree with the ADR?
- Has evidence changed enough to revisit the decision?

Populate actual evidence below.
-->

| ADR / Decision | Review Result | Current? | Revisit Needed? | Notes |
|---|---|---|---|---|
|  |  |  |  |  |

## Required Actions

<!--
TEAM CONTENT REQUIRED

Convert review findings requiring work into concrete actions.

Use action IDs when useful:

ARA-###

Examples:

ARA-001
ARA-002

Actions should have:

- clear outcome;
- owner;
- target;
- evidence of completion.

EXAMPLE ONLY:

| Action ID | Required Action | Driver | Owner | Target | Status |
|---|---|---|---|---|---|
| ARA-001 | Clarify authorization ownership in component-responsibilities.md | ARF-001 | Architecture & Development Lead | Before A3 review | Planned |

DELETE the example and populate actual actions below.
-->

| Action ID | Required Action | Driver | Owner | Target | Status |
|---|---|---|---|---|---|
|  |  |  |  |  |  |

## Review Conclusion

<!--
TEAM CONTENT REQUIRED

State the review conclusion based on the evidence.

Suggested outcomes:

- Ready
- Ready with Minor Actions
- Conditionally Ready
- Not Ready

Define the conclusion in terms of the architecture baseline reviewed.

Do not mark architecture Ready merely because the document is complete.

The conclusion should reflect whether significant architecture risks, gaps,
contradictions, or unresolved decisions remain.

Replace this comment with the actual conclusion and rationale.
-->

**Review Outcome:**  

## Follow-Up

<!--
TEAM CONTENT REQUIRED WHEN REVIEW ACTIONS REMAIN

State when or how open architecture-review actions will be checked.

If no follow-up is required, state that explicitly.
-->

<!--
FINAL STARTER KIT CHECK — DELETE BEFORE PHASE-GATE SUBMISSION

Before submission:

1. Complete review identification.
2. Confirm the architecture baseline actually reviewed.
3. Base findings on real engineering evidence.
4. Do not invent strengths or concerns.
5. Confirm component and interface names agree with architecture artifacts.
6. Reference risks, assumptions, and ADRs rather than duplicating them.
7. Convert meaningful findings into concrete actions.
8. Base the review outcome on evidence, not document completeness.
9. Remove unused sections.
10. Remove ALL instructional HTML comments.

The completed review should demonstrate critical evaluation of the architecture,
not merely approval of the team's own design.
-->
