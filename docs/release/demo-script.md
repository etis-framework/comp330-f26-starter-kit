# Release Demonstration Script

<!--
STARTER KIT GUIDANCE — DELETE BEFORE PHASE-GATE SUBMISSION

This file defines how the team will demonstrate the release.

A good engineering demonstration is NOT simply a tour of screens.

The demonstration should show meaningful system behavior and connect that
behavior to engineering evidence.

A reviewer should be able to see:

- what capability is being demonstrated;
- why it matters;
- what requirement or acceptance criterion it supports;
- what the expected result is;
- what evidence demonstrates that the behavior is real;
- relevant failure or negative-path behavior where appropriate;
- known limitations that should not be hidden.

The demo should be repeatable.

Do NOT script behavior that does not actually work.

Do NOT hide known failures by avoiding them without acknowledging the
limitation.

IMPORTANT:

- Everything inside HTML comments is Starter Kit guidance.
- Remove ALL instructional comments before the applicable phase-gate submission.
- Examples are guidance only.
-->

## Demonstration Identification

**Release / Version:**  
**Git Tag / Commit:**  
**Demo Environment:**  
**Demo Date:**  
**Presenter(s):**  

<!--
TEAM CONTENT REQUIRED

Use the same release identification as:

/docs/release/release-notes.md

Identify the actual environment being demonstrated.

Do not leave placeholder metadata in the completed artifact.
-->

## Demonstration Objective

<!--
TEAM CONTENT REQUIRED

In a short paragraph, explain what this demonstration is intended to prove or
show.

Do not write only:

"Demonstrate the application."

Instead identify the meaningful release behavior being demonstrated.

Replace this comment with the team's actual objective.
-->

## Pre-Demo Checks

<!--
TEAM CONTENT REQUIRED

Identify checks needed before the demonstration begins.

Examples may include:

- correct release deployed;
- health check passes;
- required dependencies available;
- demo accounts available;
- test data prepared;
- browser/session reset;
- relevant evidence accessible.

Do not include unnecessary ceremony.

EXAMPLE ONLY:

| Check | Expected Result | Action if Not Ready |
|---|---|---|
| Release identity | Deployment matches expected Git tag | Stop and correct deployment before demo |

Populate actual checks below.
-->

| Check | Expected Result | Action if Not Ready |
|---|---|---|
|  |  |  |

## Demo Scenario 1 — Title

<!--
TEAM CONTENT REQUIRED

Rename this section for an actual release capability.

Use additional Demo Scenario sections as needed.

Each scenario should demonstrate a meaningful engineering behavior.

Suggested content:

**Purpose**
Why is this scenario worth showing?

**Related Requirements**
Which requirement IDs apply?

**Related Acceptance Criteria**
Which acceptance criteria apply?

**Starting State**
What must be true before the scenario begins?

**Steps**
What will the presenter do?

**Expected Result**
What should the system visibly do?

**Evidence**
What repository, test, runtime, or traceability evidence supports the claim?

**Known Limitations**
What should the reviewer know about behavior that is intentionally limited?

Delete this instructional comment and complete the scenario.
-->

### Purpose

### Related Requirements

### Related Acceptance Criteria

### Starting State

### Steps

1. 
2. 
3. 

### Expected Result

### Evidence

### Known Limitations

## Demo Scenario 2 — Title

<!--
OPTIONAL TEAM CONTENT

Copy the Scenario 1 structure for another meaningful capability.

Do not create scenarios merely to make the demo longer.

Delete this section if only one scenario is appropriate.
-->

### Purpose

### Related Requirements

### Related Acceptance Criteria

### Starting State

### Steps

1. 
2. 
3. 

### Expected Result

### Evidence

### Known Limitations

## Negative / Failure Scenario

<!--
TEAM CONTENT REQUIRED WHEN A MEANINGFUL FAILURE PATH SHOULD BE DEMONSTRATED

A strong engineering demo often includes at least one important negative or
failure behavior.

Examples ONLY:

- invalid input rejected;
- unauthorized operation denied;
- missing resource handled correctly;
- duplicate request prevented;
- dependency failure surfaced safely.

Do not manufacture a failure scenario that does not matter to the system.

The purpose is to demonstrate that correctness includes handling invalid or
unsafe conditions, not only the happy path.

Remove this section if there is genuinely no meaningful negative scenario.
-->

### Purpose

### Related Requirement / Criterion

### Starting State

### Steps

1. 
2. 

### Expected Result

### Evidence

## Architecture / Engineering Evidence Callout

<!--
TEAM CONTENT REQUIRED

During or after the behavior demonstration, identify a small number of
engineering artifacts that help explain WHY the system works the way it does.

Possible evidence:

- architecture diagram;
- API contract;
- ADR;
- traceability summary;
- automated test;
- observability evidence.

Do not turn the demo into a documentation reading session.

Choose only evidence that materially helps the reviewer understand the
engineering behind the demonstrated behavior.
-->

| Evidence | What It Demonstrates | When to Show |
|---|---|---|
|  |  |  |

## Known Limitations to Acknowledge

<!--
TEAM CONTENT REQUIRED

Reference relevant limitations from:

/docs/release/known-limitations.md

Do not hide an important limitation simply because it makes the demonstration
less polished.

The goal is accurate engineering communication.

EXAMPLE ONLY:

| Limitation ID | What to State During Demo |
|---|---|
| LIM-002 | Automated recovery has not yet been implemented; recovery remains manual |

Populate actual limitations below or remove this section if none materially
affect the demonstration.
-->

| Limitation ID | What to State During Demo |
|---|---|
|  |  |

## Demo Evidence / Results

<!--
TEAM CONTENT REQUIRED AFTER THE DEMONSTRATION WHEN USEFUL

Record whether the planned demonstration actually worked.

This can provide useful release evidence.

Do not mark a scenario successful before the demonstration occurs.

EXAMPLE ONLY:

| Scenario | Result | Evidence / Observation | Follow-Up |
|---|---|---|---|
| Workflow submission | Passed | Expected status displayed; RUN-021 | None |

Populate actual results after execution if your team uses this section.
-->

| Scenario | Result | Evidence / Observation | Follow-Up |
|---|---|---|---|
|  |  |  |  |

## Recovery / Backup Demo Plan

<!--
TEAM CONTENT REQUIRED

A live demonstration can fail for reasons unrelated to the software:

- network outage;
- external service unavailable;
- deployment unavailable;
- presentation environment problem.

Identify a reasonable fallback that still preserves engineering integrity.

Examples might include:

- verified local environment;
- previously captured runtime evidence;
- test result;
- repository-visible evidence.

A fallback should NOT pretend that live behavior occurred when it did not.

If the live system fails, state that accurately and use preserved evidence only
to show what had previously been verified.

Replace this comment with the team's actual fallback approach.
-->

<!--
FINAL STARTER KIT CHECK — DELETE BEFORE PHASE-GATE SUBMISSION

Before the demonstration:

1. Confirm release identification matches release-notes.md.
2. Confirm the demo environment contains the intended release.
3. Replace generic scenario titles with actual capabilities.
4. Remove unused scenario sections.
5. Confirm requirements and acceptance criteria exist.
6. Confirm every expected result has actually been verified.
7. Include meaningful negative-path behavior where appropriate.
8. Acknowledge known limitations honestly.
9. Confirm the fallback plan does not misrepresent prerecorded evidence as live behavior.
10. Remove ALL instructional HTML comments.

The completed demo script should guide a concise, repeatable engineering
demonstration of what the release actually does and what evidence supports it.
-->
