# AI-Assisted Code Review Example

<!--
STARTER KIT GUIDANCE — DELETE BEFORE PHASE-GATE SUBMISSION IF THIS FILE IS
USED AS AN ACTUAL REVIEW RECORD

This file demonstrates how AI may assist code review while preserving human
engineering responsibility.

AI may help identify:

- possible defects;
- missing edge cases;
- security concerns;
- test gaps;
- maintainability concerns;
- contract inconsistencies;
- alternative implementations.

AI output is NOT itself an approval.

The human reviewer remains responsible for:

- understanding the change;
- evaluating AI suggestions;
- rejecting incorrect or irrelevant findings;
- independently verifying important claims;
- deciding whether required changes exist;
- making the final review decision.

This review should be consistent with:

/docs/ai/ai-policy.md
/docs/ai/ai-use-log.md
/docs/ai/ai-verification-notes.md

IMPORTANT:

- Everything inside HTML comments is Starter Kit guidance.
- If this file is copied for an actual review, remove instructional comments.
- Do not fabricate AI findings, human verification, or review outcomes.
-->

## Review Identification

**Human Reviewer:**  
**Date:**  
**Pull Request / Change:**  
**Commit / Baseline Reviewed:**  
**AI Tool:**  
**AI Model / Version (if known):**  

<!--
TEAM CONTENT REQUIRED

Identify both:

1. the exact engineering change reviewed; and
2. the AI tool used to assist the review.

Do not invent a model/version when it is unknown.
-->

## Review Purpose

<!--
TEAM CONTENT REQUIRED

State why AI assistance was used.

Examples might include:

- second-pass defect identification;
- security-focused review;
- edge-case analysis;
- test-gap analysis;
- maintainability review.

Do not use vague statements such as:

"AI reviewed the code."

Replace this comment with the actual purpose.
-->

## Related Engineering Evidence

<!--
TEAM CONTENT REQUIRED WHEN APPLICABLE

Reference relevant:

- requirements;
- acceptance criteria;
- API contracts;
- ADRs;
- defects;
- issues;
- tasks.

Populate only evidence that actually matters to the change.
-->

| Evidence | Reference | Why It Matters |
|---|---|---|
|  |  |  |

## AI Review Scope

<!--
TEAM CONTENT REQUIRED

Describe what evidence the AI was given or what part of the change it was
asked to review.

Examples:

- changed files only;
- pull-request diff;
- implementation plus acceptance criteria;
- API implementation plus API contract;
- test suite and changed code.

This helps reviewers understand what the AI could and could not reasonably
evaluate.

Do not expose secrets or protected information in prompts.
-->

## AI Findings

<!--
TEAM CONTENT REQUIRED

Record only AI findings significant enough to evaluate.

Do NOT copy an entire AI conversation.

Use stable identifiers when useful:

AIR-###

Examples:

AIR-001
AIR-002

Human Assessment should state whether the human reviewer considers the AI
finding:

- Valid
- Partially Valid
- Invalid
- Needs Investigation

EXAMPLE ONLY:

| ID | AI Finding | Human Assessment | Verification Performed | Result / Action |
|---|---|---|---|---|
| AIR-001 | API may permit unauthorized request lookup when request IDs are guessed | Needs Investigation | Compared implementation with API-002 and executed unauthorized-access test | Valid; defect opened as DEF-014 |

DELETE the example and populate actual findings below.
-->

| ID | AI Finding | Human Assessment | Verification Performed | Result / Action |
|---|---|---|---|---|
|  |  |  |  |  |

## Rejected AI Findings

<!--
TEAM CONTENT REQUIRED WHEN AI FINDINGS ARE REJECTED

Rejected AI findings are useful evidence of human engineering judgment.

Do not omit a significant AI finding merely because it was incorrect.

Explain WHY it was rejected.

EXAMPLE ONLY:

| Finding ID | AI Claim | Why Rejected | Evidence |
|---|---|---|---|
| AIR-003 | Transaction can commit partial state | Code path executes inside one database transaction | Persistence implementation and integration test |

Populate actual rejected findings below.

Remove this section if no significant AI findings were rejected.
-->

| Finding ID | AI Claim | Why Rejected | Evidence |
|---|---|---|---|
|  |  |  |  |

## Human-Only Findings

<!--
TEAM CONTENT REQUIRED WHEN THE HUMAN REVIEW IDENTIFIES SOMETHING AI MISSED

This section is important because AI-assisted review should not imply that AI
is the complete reviewer.

Record meaningful findings identified independently by the human reviewer.

EXAMPLE ONLY:

| ID | Human Finding | AI Identified It? | Evidence / Action |
|---|---|---|---|
| HCR-001 | New field is not documented in API-003 | No | API contract update required |

Populate actual findings below.

Remove this section if none occurred.
-->

| ID | Human Finding | AI Identified It? | Evidence / Action |
|---|---|---|---|
|  |  |  |  |

## Verification of Important AI Claims

<!--
TEAM CONTENT REQUIRED

AI claims with meaningful engineering consequence should be independently
verified.

Verification may include:

- code inspection;
- automated test;
- integration test;
- comparison with requirement;
- comparison with API contract;
- authoritative technical documentation;
- runtime observation;
- security analysis.

Do NOT treat:

"The AI said its earlier finding was correct"

as independent verification.

Reference:

/docs/ai/ai-verification-notes.md

when more detailed evidence is warranted.
-->

| AI Finding | Verification Method | Evidence | Conclusion |
|---|---|---|---|
|  |  |  |  |

## Test Review

<!--
TEAM CONTENT REQUIRED

Review whether the AI identified meaningful test gaps and whether those claims
were correct.

Also perform human judgment independently.

Do not add tests simply because AI suggested them.

A test should protect meaningful behavior or risk.
-->

| Behavior / Risk | Existing Evidence | AI Recommendation | Human Decision / Action |
|---|---|---|---|
|  |  |  |  |

## Architecture / Contract Review

<!--
TEAM CONTENT REQUIRED WHEN RELEVANT

Compare significant AI findings against:

/docs/architecture/architecture.md
/docs/architecture/component-responsibilities.md
/docs/architecture/api-contracts.md

AI may identify a contradiction, but the team must determine whether:

- the code is wrong;
- the architecture evidence is stale;
- the contract needs to change;
- the AI interpretation is incorrect.

Remove this section when it genuinely does not apply.
-->

## AI Use Log Reference

<!--
TEAM CONTENT REQUIRED

Significant AI-assisted review should normally be represented in:

/docs/ai/ai-use-log.md

Reference the corresponding entry.

Do not duplicate the entire AI Use Log here.
-->

**AI Use Log Reference:**  

## Human Review Decision

<!--
TEAM CONTENT REQUIRED

The final review decision belongs to the HUMAN reviewer.

Suggested outcomes:

Approve
Approve with Non-Blocking Suggestions
Changes Requested

Do not write:

"AI approved the pull request."

AI may provide input.

A human makes the engineering review decision.
-->

**Decision:**  

**Human Rationale:**  

## Follow-Up

<!--
TEAM CONTENT REQUIRED WHEN ACTIONS REMAIN

Record how significant AI or human findings were resolved.

EXAMPLE ONLY:

| Finding ID | Action | Resolution Evidence | Human Verification |
|---|---|---|---|
| AIR-001 | Added authorization check and regression test | PR #27 | Verified by Taylor Nguyen |

Populate actual evidence below.

Remove this section if no follow-up was needed.
-->

| Finding ID | Action | Resolution Evidence | Human Verification |
|---|---|---|---|
|  |  |  |  |

## Review Reflection

<!--
OPTIONAL TEAM CONTENT

A useful AI-assisted review may provide evidence about the strengths and
limitations of the AI reviewer itself.

Examples:

- AI identified an edge case the team missed;
- AI produced several plausible but incorrect findings;
- AI was useful only after receiving the API contract;
- AI focused on syntax and missed architectural inconsistency;
- human review found a critical issue AI did not identify.

Do not praise or criticize AI generically.

Base reflection on actual evidence from this review.

Remove this section if it adds no useful engineering evidence.
-->

<!--
FINAL STARTER KIT CHECK — DELETE FROM AN ACTUAL REVIEW

Before finalizing an AI-assisted code-review record:

1. Identify the exact code baseline reviewed.
2. Identify the AI tool used.
3. State the AI review scope.
4. Preserve only significant AI findings.
5. Human-assess every retained AI finding.
6. Independently verify important AI claims.
7. Record significant rejected AI findings.
8. Record meaningful human-only findings when present.
9. Reference the AI Use Log.
10. Ensure the final review decision is explicitly human.
11. Remove ALL instructional HTML comments.

The completed review should demonstrate that AI assisted engineering judgment;
it did not replace it.
-->
