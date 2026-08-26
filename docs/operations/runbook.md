# Operations Runbook

<!--
STARTER KIT GUIDANCE — DELETE BEFORE PHASE-GATE SUBMISSION

This file documents how your team operates, verifies, troubleshoots, and
recovers the running system.

A runbook should help another engineer answer questions such as:

- How do I know the system is healthy?
- How is the system started or deployed?
- What dependencies must be available?
- What routine checks should be performed?
- What should I inspect when something fails?
- How can the system be safely restarted or recovered?
- Where do I find logs, metrics, or runtime evidence?

For a course project, this does NOT need to become an enterprise operations
manual.

Document procedures that are real and useful for your system.

IMPORTANT:

- Everything inside HTML comments like this is Starter Kit guidance.
- Remove all instructional comments before the applicable phase-gate submission.
- Examples inside comments are guidance only.
- Do not document commands, URLs, credentials, procedures, or capabilities
  that your system does not actually use.
- Never place passwords, tokens, private keys, or other secrets in this file.
-->

## System Overview

<!--
TEAM CONTENT REQUIRED

Provide a concise operational description of the system.

Include information useful to someone who must operate or troubleshoot it,
such as:

- major runtime components;
- deployment environment;
- important external dependencies;
- authoritative data store;
- operational entry points.

Do not repeat the full architecture document.

Replace this comment with your team's actual operational overview.
-->

## Environments

<!--
TEAM CONTENT REQUIRED

Document the environments that actually exist.

Examples might include:

- local development;
- CI;
- test;
- staging;
- production or course-hosted deployment.

Do not list environments your team does not use.

EXAMPLE ONLY:

| Environment | Purpose | Location / Access | Important Notes |
|---|---|---|---|
| Test | Team integration and runtime verification | Deployment URL or platform reference | Uses test data only |

Populate the table below with actual environments.
-->

| Environment | Purpose | Location / Access | Important Notes |
|---|---|---|---|
|  |  |  |  |

## Dependencies

<!--
TEAM CONTENT REQUIRED

Identify dependencies required for normal operation.

Examples may include:

- database;
- identity provider;
- external API;
- message service;
- storage service;
- configuration source.

Record only dependencies that actually matter operationally.

Do not place credentials or secrets here.

EXAMPLE ONLY:

| Dependency | Purpose | How to Verify | Failure Impact |
|---|---|---|---|
| Database | Persistent workflow state | Application health check / connection verification | Core workflow operations unavailable |

Populate the actual table below.
-->

| Dependency | Purpose | How to Verify | Failure Impact |
|---|---|---|---|
|  |  |  |  |

## Configuration

<!--
TEAM CONTENT REQUIRED

Identify important configuration required for operation.

Do NOT include secret values.

Instead, document:

- configuration variable name;
- purpose;
- where the value is managed;
- whether it is required;
- safe example values when appropriate.

EXAMPLE ONLY:

| Configuration | Purpose | Required | Managed In |
|---|---|---|---|
| APP_ENV | Identifies runtime environment | Yes | Deployment configuration |

Populate the actual table below.
-->

| Configuration | Purpose | Required | Managed In |
|---|---|---|---|
|  |  |  |  |

## Start / Deploy Procedure

<!--
TEAM CONTENT REQUIRED

Document the actual procedure used to make the system available.

This may be:

- local startup commands;
- CI/CD deployment;
- platform deployment;
- container startup;
- another actual process.

Write the procedure so another team member can follow it.

Do not invent manual commands if deployment is automated.

If deployment is handled by CI/CD, describe:

1. what triggers deployment;
2. where deployment status is visible;
3. how success is verified; and
4. what to do if deployment fails.

Replace this comment with the actual procedure.
-->

## Post-Deployment Verification

<!--
TEAM CONTENT REQUIRED

Define the minimum checks used to determine whether a deployment or startup
was successful.

Consider:

- health check;
- application access;
- critical workflow;
- database connectivity;
- authentication;
- important dependency;
- logs or metrics.

EXAMPLE ONLY:

| Check | Expected Result | Evidence / Location |
|---|---|---|
| Application health | Healthy response | Health endpoint |
| Basic workflow | Test request completes successfully | Runtime evidence entry |

Populate the actual table below.
-->

| Check | Expected Result | Evidence / Location |
|---|---|---|
|  |  |  |

## Routine Operational Checks

<!--
TEAM CONTENT REQUIRED

Identify checks that are useful during normal operation.

Not every project requires recurring manual checks.

Examples might include:

- application availability;
- failed requests;
- dependency health;
- recent deployment status;
- error logs;
- relevant runtime metrics.

Do not create unnecessary operational busywork.

Populate only checks that actually help your team understand system health.
-->

| Check | How to Perform | Normal Result | Action if Abnormal |
|---|---|---|---|
|  |  |  |  |

## Troubleshooting

<!--
TEAM CONTENT REQUIRED

Document common or important failure symptoms and the first useful checks.

Do not attempt to document every possible defect.

Focus on operational problems another team member could realistically
encounter.

EXAMPLE ONLY:

| Symptom | Likely Areas to Check | Evidence to Inspect | Initial Action |
|---|---|---|---|
| Application cannot persist requests | Database connectivity, configuration | Health check, application logs | Verify dependency before restarting application |

Populate the actual table below.
-->

| Symptom | Likely Areas to Check | Evidence to Inspect | Initial Action |
|---|---|---|---|
|  |  |  |  |

## Logs, Metrics, and Runtime Evidence

<!--
TEAM CONTENT REQUIRED

Identify where operational evidence can be found.

Reference:

/docs/observability/observability-plan.md
/docs/observability/metrics-notes.md
/docs/observability/runtime-evidence.md

Do not duplicate those artifacts here.

The purpose of this section is to tell an operator WHERE to look.

EXAMPLE ONLY:

| Evidence Type | Location / Source | Used For |
|---|---|---|
| Application logs | Deployment platform logging view | Investigating runtime errors |
| Runtime evidence | `/docs/observability/runtime-evidence.md` | Preserved verification results |

Populate the actual table below.
-->

| Evidence Type | Location / Source | Used For |
|---|---|---|
|  |  |  |

## Restart and Recovery

<!--
TEAM CONTENT REQUIRED WHEN RESTART OR RECOVERY PROCEDURES EXIST

Document safe recovery actions.

Examples may include:

- application restart;
- redeployment;
- restoring a failed dependency;
- rollback;
- data recovery;
- clearing transient state.

Distinguish between:

- a safe operational action; and
- an action that risks data loss or requires special approval.

Never recommend destructive recovery merely because it is easy.

EXAMPLE ONLY:

| Situation | Recovery Action | Verification | Risk / Caution |
|---|---|---|---|
| Application instance unhealthy | Restart or redeploy application | Health and basic workflow checks | Confirm persistent data is external to the instance |

Populate the actual table below where relevant.
-->

| Situation | Recovery Action | Verification | Risk / Caution |
|---|---|---|---|
|  |  |  |  |

## Rollback

<!--
TEAM CONTENT REQUIRED IF ROLLBACK IS POSSIBLE

Explain how the team returns to a previous known-good version when a deployment
introduces a serious problem.

Document the actual mechanism used by your project.

If no practical rollback mechanism currently exists, state that explicitly
and identify the operational consequence.

Do not pretend rollback capability exists if it has not been implemented or
verified.
-->

## Data Backup and Recovery

<!--
TEAM CONTENT REQUIRED WHEN THE SYSTEM PERSISTS IMPORTANT DATA

Document what data requires protection and what recovery capability actually
exists.

Consider:

- what is backed up;
- how backups occur;
- retention;
- who or what performs the backup;
- how recovery would be performed;
- whether recovery has been tested.

If the project uses disposable test data and no backup is required, state that
explicitly.

Do not claim recovery has been tested unless actual evidence exists.
-->

| Data / State | Protection Method | Recovery Method | Verification Status |
|---|---|---|---|
|  |  |  |  |

## Incident Escalation

<!--
TEAM CONTENT REQUIRED

Describe when an operational problem should stop being treated as routine
troubleshooting and become an incident.

Reference:

/docs/operations/incident-response-notes.md

Possible escalation triggers might include:

- system unavailable;
- data integrity concern;
- security concern;
- repeated critical failure;
- failed deployment with no safe recovery;
- issue affecting an important acceptance criterion.

Define triggers appropriate to your actual project.
-->

## Known Operational Limitations

<!--
TEAM CONTENT REQUIRED

Record limitations honestly.

Examples ONLY:

- no automated rollback;
- recovery has not yet been tested;
- monitoring is limited to platform logs;
- only one deployment environment exists;
- external dependency outage cannot be mitigated.

Use this section to make operational uncertainty visible rather than hiding it.
-->

| Limitation | Operational Impact | Planned Improvement | Target Gate / Milestone |
|---|---|---|---|
|  |  |  |  |

<!--
FINAL STARTER KIT CHECK — DELETE BEFORE PHASE-GATE SUBMISSION

Before submission:

1. Replace all blank scaffold rows with actual project information or remove
   unnecessary rows.
2. Confirm every procedure reflects the system the team actually operates.
3. Remove sample or hypothetical commands and procedures.
4. Verify links to observability and incident-response evidence.
5. Confirm no secrets or protected credentials appear in the file.
6. Identify unimplemented operational capabilities honestly.
7. Remove ALL instructional HTML comments.

A reviewer or teammate should be able to use the finished runbook to operate
and troubleshoot the system without guessing how it works.
-->
