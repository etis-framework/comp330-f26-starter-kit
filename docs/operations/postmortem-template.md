# Postmortem: Incident Title

<!--
STARTER KIT GUIDANCE

This file is a TEMPLATE.

Do NOT complete this file as though a fictional incident occurred.

When a meaningful real incident warrants a postmortem:

1. Copy this template.
2. Rename the copy using a descriptive incident identifier or title.

Example:

postmortem-INC-001-database-outage.md

3. Replace all placeholder headings and metadata with actual incident evidence.
4. Remove all instructional HTML comments from the completed postmortem.
5. Keep this original template available for future incidents unless your
   repository instructions specify otherwise.

A postmortem is intended to learn from an incident and improve the system or
engineering process.

It is NOT intended to assign blame to an individual.
-->

**Incident ID:** INC-###  
**Date:** YYYY-MM-DD  
**Postmortem Date:** YYYY-MM-DD  
**Status:** Draft  
**Owners:**  

<!--
REPLACE ALL METADATA ABOVE IN AN ACTUAL POSTMORTEM.

Incident ID:
Reference the corresponding actual incident from incident-response-notes.md.

Status examples:
- Draft
- Reviewed
- Final

Owners:
Identify the team members responsible for preparing or reviewing the record.

Do not leave placeholder values in a completed postmortem.
-->

## Executive Summary

<!--
TEAM CONTENT REQUIRED

Summarize the incident in a few sentences.

A reader should understand:

- what happened;
- what was affected;
- the operational consequence; and
- how the incident was resolved.

Avoid detailed root-cause analysis here.

Replace this comment with the actual summary.
-->

## Impact

<!--
TEAM CONTENT REQUIRED

Describe the actual consequence of the incident.

Consider where relevant:

- users affected;
- capabilities unavailable;
- incorrect behavior;
- data integrity;
- security;
- duration;
- operational workload;
- phase-gate or verification impact.

Do not exaggerate impact.

If an area was NOT affected, do not imply that it was.
-->

## Detection

<!--
TEAM CONTENT REQUIRED

Explain how the incident was first detected.

Examples may include:

- user report;
- failed acceptance test;
- health check;
- log review;
- metric;
- deployment verification;
- runtime observation.

Also identify whether the team believes detection should have occurred sooner.

Reference relevant observability evidence where useful.
-->

## Timeline

<!--
TEAM CONTENT REQUIRED

Record significant events in chronological order.

Do not include every minor action.

Use actual timestamps when available.

EXAMPLE STRUCTURE ONLY:

| Time | Event / Observation | Action / Decision |
|---|---|---|
| HH:MM | Incident detected | Response initiated |
| HH:MM | Cause narrowed to dependency failure | Recovery action selected |

Delete fictional examples and populate the blank table below.
-->

| Time | Event / Observation | Action / Decision |
|---|---|---|
|  |  |  |

## Technical Cause

<!--
TEAM CONTENT REQUIRED

Describe the technical condition that directly produced the incident.

Distinguish:

- observed symptom;
- direct technical cause;
- deeper contributing factors.

Do not claim a root cause that evidence does not support.

If the cause remains uncertain, say so explicitly.
-->

## Contributing Factors

<!--
TEAM CONTENT REQUIRED

Identify conditions that increased the likelihood, impact, or duration of the
incident.

Examples might include:

- unclear requirement;
- architectural weakness;
- missing validation;
- insufficient testing;
- missing monitoring;
- poor error handling;
- configuration mistake;
- dependency behavior;
- operational procedure gap;
- incorrect assumption.

Do not invent contributing factors to fill the section.

A contributing factor is not necessarily a person's mistake.
-->

## What Went Well

<!--
TEAM CONTENT REQUIRED

Identify parts of the system or response that helped limit the incident.

Examples might include:

- health check detected the failure;
- logs made diagnosis straightforward;
- rollback worked;
- team communication was effective;
- automated test reproduced the defect;
- backup or recovery procedure worked.

Use actual evidence.
-->

- 

<!--
REPLACE THE PLACEHOLDER BULLET ABOVE.
-->

## What Did Not Go Well

<!--
TEAM CONTENT REQUIRED

Identify system, evidence, process, or response weaknesses exposed by the
incident.

Focus on conditions the team can improve.

Avoid blame-oriented statements about individuals.
-->

- 

<!--
REPLACE THE PLACEHOLDER BULLET ABOVE.
-->

## Where We Got Lucky

<!--
OPTIONAL TEAM CONTENT

Sometimes an incident had limited impact because of circumstances the system
did not deliberately guarantee.

Examples:

- few users were active;
- the failure occurred before important data existed;
- a dependency recovered quickly;
- the defect did not reach another code path.

Recognizing luck helps prevent accidental success from being mistaken for
engineering control.

If this section does not apply, remove it.
-->

## Corrective Actions

<!--
TEAM CONTENT REQUIRED

Corrective actions should address the causes or weaknesses discovered during
the incident.

Use concrete, trackable actions.

Avoid vague actions such as:

"Be more careful."

Possible actions may involve:

- requirement clarification;
- architecture change;
- implementation fix;
- test addition;
- observability improvement;
- runbook update;
- deployment safeguard;
- operational procedure change.

Each action should have an owner and status.

EXAMPLE ONLY:

| Action ID | Corrective Action | Owner | Priority | Status | Related Evidence |
|---|---|---|---|---|---|
| ACT-001 | Add dependency-failure integration test | Quality & Review Lead | High | Planned | Issue #42 |

Delete the example and populate the actual table below.
-->

| Action ID | Corrective Action | Owner | Priority | Status | Related Evidence |
|---|---|---|---|---|---|
|  |  |  |  |  |  |

## Engineering Evidence to Update

<!--
TEAM CONTENT REQUIRED

An incident may invalidate or refine earlier engineering evidence.

Review whether the incident requires updates to:

- requirements;
- acceptance criteria;
- assumptions or open questions;
- risks;
- architecture;
- component responsibilities;
- API contracts;
- decision records;
- tests;
- observability plan;
- metrics;
- runbook;
- incident response procedures.

Do not assume that fixing the code alone is sufficient.

Populate the table with only artifacts actually affected.
-->

| Artifact / Evidence | Required Change | Owner | Status |
|---|---|---|---|
|  |  |  |  |

## Recurrence Prevention / Detection

<!--
TEAM CONTENT REQUIRED

Explain how the team intends to:

1. reduce the likelihood of recurrence; and/or
2. detect the condition more quickly if it happens again.

A good answer may involve several layers:

- prevention;
- test coverage;
- observability;
- operational procedure.

Do not claim the incident "can never happen again" unless evidence truly
supports that conclusion.
-->

## Lessons Learned

<!--
TEAM CONTENT REQUIRED

Capture the most important engineering lessons.

Focus on reusable learning rather than retelling the incident.

Examples of useful themes:

- an assumption should have been validated earlier;
- an interface contract was ambiguous;
- failure behavior was not designed explicitly;
- observability was insufficient;
- deployment verification missed a critical condition.

Replace this comment with actual lessons.
-->

## Evidence References

<!--
TEAM CONTENT REQUIRED

Reference relevant repository-visible evidence.

Examples may include:

- incident record;
- logs;
- runtime evidence;
- issues;
- pull requests;
- tests;
- requirement IDs;
- acceptance criteria;
- ADRs;
- runbook changes;
- observability evidence.

Do not include secrets or protected information.
-->

<!--
FINAL TEMPLATE CHECK — DELETE FROM COMPLETED POSTMORTEM

Before finalizing a copied postmortem:

1. Replace the title and all metadata.
2. Confirm the Incident ID references a real incident.
3. Complete the actual impact and timeline.
4. Distinguish symptoms, technical cause, and contributing factors.
5. Replace all placeholder bullets.
6. Record corrective actions with owners.
7. Identify engineering evidence that needs updating.
8. Link real supporting evidence.
9. Remove sections that genuinely do not apply.
10. Remove ALL instructional HTML comments.

The completed postmortem should be a factual, blameless engineering learning
record based on actual evidence.
-->
