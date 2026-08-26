# Incident Response Notes

<!--
STARTER KIT GUIDANCE — DELETE BEFORE PHASE-GATE SUBMISSION

This file defines how your team intends to recognize, coordinate, investigate,
contain, recover from, and document meaningful operational incidents.

An incident is more than an ordinary defect.

For this project, an incident may involve a significant condition such as:

- system unavailability;
- major workflow failure;
- data integrity concern;
- security concern;
- failed deployment that affects users;
- serious dependency failure;
- repeated critical runtime errors.

Not every bug requires incident handling.

For a course project, the goal is NOT to reproduce a corporate incident
management organization.

The goal is to demonstrate disciplined engineering behavior when the running
system fails in a meaningful way.

IMPORTANT:

- Everything inside HTML comments is Starter Kit guidance.
- Remove instructional comments before the applicable phase-gate submission.
- Examples are guidance only.
- Replace generic roles and procedures with what your team will actually do.
-->

## Incident Definition

<!--
TEAM CONTENT REQUIRED

Define what your team considers an operational incident.

Distinguish incidents from:

- routine defects;
- failed tests during normal development;
- ordinary feature work;
- minor UI problems.

Replace this comment with the team's actual definition.
-->

## Severity / Priority

<!--
TEAM CONTENT REQUIRED

Use a simple classification appropriate for your project.

Do NOT create an enterprise-scale severity model unless it adds value.

EXAMPLE ONLY:

| Level | Description | Example |
|---|---|---|
| Critical | Core system unavailable, security concern, or meaningful data-integrity risk | Users cannot access the system |
| Significant | Important capability impaired but system remains partially usable | Workflow submission consistently fails |
| Minor | Limited operational defect with a practical workaround | Non-critical runtime warning |

Delete the example and define the classification your team will actually use.
-->

| Level | Description | Example / Trigger |
|---|---|---|
|  |  |  |

## Incident Roles

<!--
TEAM CONTENT REQUIRED

Identify who coordinates incident response.

You may reference specialized team roles from:

/docs/team/roles.md

Possible responsibilities include:

- Incident Coordinator
- Technical Investigation
- Evidence Capture
- Communication
- Recovery Verification

Do not assign elaborate incident roles that your team cannot realistically use.

EXAMPLE ONLY:

| Responsibility | Primary Role / Owner | Backup |
|---|---|---|
| Coordinate response | Operations & Evidence Lead | Team Lead |
| Technical investigation | Architecture & Development Lead | Quality & Review Lead |

Populate the actual table below.
-->

| Responsibility | Primary Role / Owner | Backup |
|---|---|---|
|  |  |  |

## Initial Response

<!--
TEAM CONTENT REQUIRED

Define the first actions after recognizing a meaningful incident.

A practical sequence may include:

1. confirm that the problem is real;
2. identify affected environment and behavior;
3. protect data and evidence;
4. stop unsafe or damaging activity when necessary;
5. identify an incident coordinator;
6. begin recording significant actions;
7. determine whether containment is required.

Adapt this process to your project.

Replace this comment with your team's actual response expectations.
-->

## Evidence Preservation

<!--
TEAM CONTENT REQUIRED

Identify evidence that should be preserved during an incident.

Examples may include:

- timestamps;
- logs;
- error messages;
- metric observations;
- deployment identifier;
- commit or release version;
- affected request IDs;
- screenshots;
- relevant issue or PR;
- reproduction steps.

Do not collect or expose secrets or unnecessary sensitive information.

Runtime evidence may be preserved in:

/docs/observability/runtime-evidence.md
-->

## Investigation

<!--
TEAM CONTENT REQUIRED

Describe how the team investigates the incident.

Useful questions include:

- What failed?
- When did it begin?
- What changed?
- Which components or dependencies are affected?
- Can the problem be reproduced?
- Is data integrity at risk?
- Is there a security concern?
- What evidence supports the current theory?

Do not jump directly from symptom to assumed cause.

Replace this comment with the actual investigation approach.
-->

## Containment

<!--
TEAM CONTENT REQUIRED WHEN RELEVANT

Containment attempts to limit additional harm before the permanent fix is
known.

Possible actions might include:

- disable an affected feature;
- stop a broken deployment;
- roll back;
- block an unsafe operation;
- temporarily isolate an external integration.

Do not create a containment step merely because this section exists.

If containment is unnecessary for the kinds of incidents your project can
experience, state that explicitly.
-->

## Recovery

<!--
TEAM CONTENT REQUIRED

Define how the team determines that the system is safe to return to normal
operation.

Recovery should include verification.

Reference the applicable procedures in:

/docs/operations/runbook.md

Possible recovery evidence may include:

- health checks;
- critical workflow verification;
- acceptance criteria;
- regression tests;
- dependency checks;
- runtime observations.

Do not declare recovery based only on "the application started."
-->

## Communication

<!--
TEAM CONTENT REQUIRED

Define who needs to know about a meaningful incident and when.

For a course project this may simply mean:

- team members;
- instructor when appropriate;
- affected stakeholder or reviewer if applicable.

Keep the process proportional.

Do not invent external communication requirements that do not apply.
-->

## Incident Record

<!--
TEAM CONTENT REQUIRED WHEN AN ACTUAL INCIDENT OCCURS

Use stable identifiers:

INC-###

Examples:

INC-001
INC-002

The table below should contain ACTUAL incidents only.

Do not create fake incidents to make the repository appear complete.

At project start, a blank table is correct.
-->

| Incident ID | Date / Time | Severity | Summary | Status | Evidence |
|---|---|---|---|---|---|
|  |  |  |  |  |  |

## Incident Timeline

<!--
USE WHEN AN ACTUAL INCIDENT REQUIRES A TIMELINE

Record meaningful events and actions.

Do not document every chat message or minor action.

EXAMPLE STRUCTURE ONLY:

| Time | Event / Observation | Action / Decision | Owner |
|---|---|---|---|
| 14:05 | Repeated request failures confirmed | Incident opened as INC-001 | Team Lead |
| 14:12 | Database dependency unavailable | Recovery procedure initiated | Operations Lead |

Do not retain fictional sample entries.

Create a timeline only when there is an actual incident worth preserving.
-->

## Escalation Conditions

<!--
TEAM CONTENT REQUIRED

Identify conditions requiring additional attention or instructor involvement.

Examples may include:

- suspected security issue;
- potential data loss or corruption;
- no safe recovery path;
- unresolved critical outage;
- incident affecting phase-gate evidence;
- issue beyond the team's authority or access.

Replace this comment with actual escalation expectations.
-->

## Post-Incident Review

<!--
TEAM CONTENT REQUIRED

Identify when an incident should receive a postmortem.

A postmortem is most useful when an incident:

- materially affected users or system operation;
- exposed an architectural weakness;
- exposed a process weakness;
- involved a security or data-integrity concern;
- required significant recovery work;
- is likely to recur without corrective action.

Use:

/docs/operations/postmortem-template.md

Do not require a postmortem for every minor defect.
-->

<!--
FINAL STARTER KIT CHECK — DELETE BEFORE PHASE-GATE SUBMISSION

Before submission:

1. Define what actually constitutes an incident for your project.
2. Replace blank planning rows with actual team decisions where required.
3. Keep the Incident Record blank unless real incidents occurred.
4. Do not fabricate timelines or operational failures.
5. Confirm response responsibilities agree with docs/team/roles.md.
6. Confirm recovery references agree with runbook.md.
7. Confirm runtime evidence references actual evidence.
8. Remove ALL instructional HTML comments.

The finished document should show how the team responds responsibly to
meaningful operational failure without creating unnecessary process overhead.
-->
