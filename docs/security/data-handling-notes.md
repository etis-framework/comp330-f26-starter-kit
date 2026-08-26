# Data Handling Notes

<!--
STARTER KIT GUIDANCE — DELETE BEFORE PHASE-GATE SUBMISSION

This file documents how important project data is collected, created,
transmitted, stored, accessed, logged, retained, and removed.

The goal is NOT to create a legal or enterprise data-governance policy.

The goal is to make engineering decisions about data visible.

This artifact should help answer:

- What important data does the system handle?
- Where does the data come from?
- Is any of it sensitive?
- Where is it stored?
- Who can access it?
- Where does it travel?
- What must not appear in logs?
- How long is it retained?
- How is it deleted or disposed of?
- What assumptions or risks affect data handling?

Do not record actual passwords, tokens, private keys, or protected data in
this document.

IMPORTANT:

- Everything inside HTML comments is Starter Kit guidance.
- Remove ALL instructional comments before the applicable phase-gate submission.
- Examples are guidance only.
- Do not invent sensitive data categories that your system does not actually handle.
-->

## Data Overview

<!--
TEAM CONTENT REQUIRED

Briefly summarize the important categories of data handled by the system.

Keep this high-level.

Replace this comment with the team's actual data overview.
-->

## Data Inventory

<!--
TEAM CONTENT REQUIRED

Use stable identifiers where useful:

DATA-###

Examples:

DATA-001
DATA-002

COLUMN GUIDANCE

Data Category
Describe the type of data.

Source
Where it originates.

Sensitivity
Use a simple classification appropriate to your project.

Suggested values:

- Public
- Internal
- Sensitive
- Secret / Credential

Do not label ordinary data Sensitive without a reason.

Authoritative Owner
Which system or component is authoritative for the data.

Storage
Where the data is stored.

Retention
How long or under what condition it is kept.

Related Evidence
Reference requirements, architecture, risks, or permissions.

EXAMPLE ONLY:

| ID | Data Category | Source | Sensitivity | Authoritative Owner | Storage | Retention | Related Evidence |
|---|---|---|---|---|---|---|---|
| DATA-001 | Workflow request | Authenticated user | Internal | Application Service | Application database | Project-defined retention | REQ-001 |

DELETE the example and populate the actual table below.
-->

| ID | Data Category | Source | Sensitivity | Authoritative Owner | Storage | Retention | Related Evidence |
|---|---|---|---|---|---|---|---|
|  |  |  |  |  |  |  |  |

## Data Classification

<!--
TEAM CONTENT REQUIRED

Define what your sensitivity labels mean.

A lightweight classification is sufficient.

EXAMPLE ONLY:

Public
- Safe to expose publicly.

Internal
- Intended for project/application use but not inherently sensitive.

Sensitive
- Inappropriate for unrestricted disclosure and requiring deliberate handling.

Secret / Credential
- Passwords, private keys, tokens, or other values used to authenticate or
  authorize access.

Do not retain these definitions without team review.

Replace this comment with the classification actually used by the project.
-->

## Data Flow

<!--
TEAM CONTENT REQUIRED

Document important movement of data across architectural boundaries.

Do not list every method call.

Focus on data crossing:

- browser/application boundary;
- service boundary;
- database boundary;
- external-service boundary;
- trust boundary.

EXAMPLE ONLY:

| Data | Source | Destination | Purpose | Protection / Boundary |
|---|---|---|---|---|
| Workflow request | Web Client | Application Service | Submit workflow | Authenticated HTTPS request |

DELETE the example and populate actual data flows below.
-->

| Data | Source | Destination | Purpose | Protection / Boundary |
|---|---|---|---|---|
|  |  |  |  |  |

## Storage

<!--
TEAM CONTENT REQUIRED

Identify where important data is stored.

Consider:

- application database;
- local filesystem;
- cloud storage;
- browser storage;
- CI artifacts;
- logs;
- external service.

Questions include:

- Is the storage authoritative?
- Is data durable?
- Is encryption provided by the platform?
- Who can access it?
- Does the team actually need to store the data?

Do not claim encryption or security properties unless they are actually
provided or configured.
-->

| Data Category | Storage Location | Durable? | Access Boundary | Protection / Notes |
|---|---|---|---|---|
|  |  |  |  |  |

## Data Access

<!--
TEAM CONTENT REQUIRED

Reference:

/docs/security/permission-boundaries.md

Do not create a second permission matrix.

Summarize only data-access rules important enough to data handling.

EXAMPLE ONLY:

| Data Category | Authorized Access | Important Restriction | Permission Evidence |
|---|---|---|---|
| Workflow request | Request owner and authorized reviewer | Normal users cannot access another user's private request | permission-boundaries.md |

Populate actual relationships below.
-->

| Data Category | Authorized Access | Important Restriction | Permission Evidence |
|---|---|---|---|
|  |  |  |  |

## Sensitive Data Handling

<!--
TEAM CONTENT REQUIRED WHEN SENSITIVE DATA EXISTS

For each sensitive category, describe special handling requirements.

Consider:

- restricted access;
- storage;
- transmission;
- logging;
- retention;
- deletion;
- test data;
- screenshots or demo data.

Do not place real sensitive values in this file.

Populate only categories that genuinely require additional handling.
-->

| Data Category | Required Handling | Prohibited Handling | Evidence |
|---|---|---|---|
|  |  |  |  |

## Secrets and Credentials

<!--
TEAM CONTENT REQUIRED

Identify TYPES of secrets the project uses, not secret values.

Examples:

- database credential;
- API token;
- OAuth client secret;
- private key.

Document:

- where the secret is managed;
- who or what needs access;
- whether it is required in local, CI, or deployed environments.

Never place the actual secret value here.

EXAMPLE ONLY:

| Secret Type | Purpose | Managed In | Used By | Repository Exposure |
|---|---|---|---|---|
| Database credential | Application database access | Deployment secret configuration | Application Service | Must not be committed |

DELETE the example and populate actual secret types below.
-->

| Secret Type | Purpose | Managed In | Used By | Repository Exposure |
|---|---|---|---|---|
|  |  |  |  |  |

## Logging and Telemetry

<!--
TEAM CONTENT REQUIRED

Identify data that may appear in:

- application logs;
- metrics;
- traces;
- runtime evidence;
- screenshots.

Reference:

/docs/observability/

Important question:

"What information must NOT appear in logs or telemetry?"

EXAMPLE ONLY:

| Data / Field | May Be Logged? | Handling Rule | Reason |
|---|---|---|---|
| Authentication token | No | Never emit token value | Credential exposure risk |
| Request ID | Yes | Use for correlation | Needed for operational traceability |

DELETE the example and populate actual rules below.
-->

| Data / Field | May Be Logged? | Handling Rule | Reason |
|---|---|---|---|
|  |  |  |  |

## Test and Demo Data

<!--
TEAM CONTENT REQUIRED

Describe how test and demonstration data is handled.

Consider:

- synthetic data;
- real personal data;
- copied production data;
- screenshots;
- demo accounts.

Prefer synthetic or intentionally created test data unless a legitimate reason
requires otherwise.

Do not place sensitive real-world personal data into the repository merely
because it simplifies testing.

Replace this comment with the team's actual approach.
-->

## Retention

<!--
TEAM CONTENT REQUIRED

Document how long important data is retained or the condition under which it
is removed.

Retention may be defined by:

- project need;
- course lifecycle;
- operational requirement;
- external service behavior;
- platform lifecycle.

Do not invent a precise retention period without a basis.

If retention is currently unknown, reference an open question rather than
creating unsupported policy.
-->

| Data Category | Retention Rule | Basis | Disposal / Removal |
|---|---|---|---|
|  |  |  |  |

## Data Deletion / Disposal

<!--
TEAM CONTENT REQUIRED WHEN DATA CAN OR SHOULD BE REMOVED

Describe what deletion means.

Questions may include:

- Is data actually deleted or merely hidden?
- Are backups affected?
- Can the user initiate deletion?
- Does archiving replace deletion?
- Are test environments disposable?

Do not claim secure deletion guarantees that the platform does not actually
provide.

Replace this comment with actual project behavior.
-->

## External Data Handling

<!--
TEAM CONTENT REQUIRED WHEN EXTERNAL SERVICES RECEIVE OR RETURN DATA

Document important data sent to or received from external systems.

Examples might include:

- identity provider;
- third-party API;
- AI service;
- cloud service.

Questions include:

- What data leaves the application boundary?
- Why?
- Is sensitive data included?
- Who is authoritative for returned data?
- What happens when the external service is unavailable?

EXAMPLE ONLY:

| External Service | Data Sent | Data Received | Purpose | Important Constraint |
|---|---|---|---|---|
| Identity Provider | Authentication request | User identity claims | Authenticate user | Application does not store user password |

DELETE the example and populate actual external data flows below.
-->

| External Service | Data Sent | Data Received | Purpose | Important Constraint |
|---|---|---|---|---|
|  |  |  |  |  |

## AI Data Handling

<!--
TEAM CONTENT REQUIRED WHEN AI TOOLS ARE USED WITH PROJECT DATA

Reference:

/docs/ai/ai-policy.md

Consider what project information may or may not be provided to AI tools.

Do not provide AI systems with:

- passwords;
- access tokens;
- private keys;
- secrets;
- protected credentials.

Also consider whether user data, private project information, or sensitive
records are appropriate to provide.

Replace this comment with actual team policy or reference the authoritative
AI policy if it already fully addresses the issue.

Remove this section if AI data handling is not relevant.
-->

## Data Risks and Open Questions

<!--
TEAM CONTENT REQUIRED

Reference authoritative evidence from:

/docs/planning/risk-register.md
/docs/requirements/assumptions-open-questions.md

Do not duplicate those artifacts.

Include only risks or unknowns that materially affect data handling.
-->

| Risk / Question | Data Impact | Current Action / Needed Decision |
|---|---|---|
|  |  |  |

## Data Handling Verification

<!--
TEAM CONTENT REQUIRED

Identify actual evidence supporting important data-handling claims.

Possible evidence:

- permission tests;
- API tests;
- configuration inspection;
- secret scanning;
- log inspection;
- runtime evidence;
- code review.

Do not claim controls have been verified merely because they are documented.
-->

| Data Handling Concern | Verification | Result | Evidence |
|---|---|---|---|
|  |  |  |  |

## Known Data-Handling Limitations

<!--
TEAM CONTENT REQUIRED

Document limitations honestly.

Examples:

- retention policy not yet finalized;
- backup deletion behavior unknown;
- audit logging incomplete;
- external service behavior not fully verified.

Reference:

/docs/release/known-limitations.md

when the limitation affects the current release.
-->

| Limitation | Impact | Disposition | Related Evidence |
|---|---|---|---|
|  |  |  |  |

<!--
FINAL STARTER KIT CHECK — DELETE BEFORE PHASE-GATE SUBMISSION

Before submission:

1. Inventory only data the project actually handles.
2. Define the project's data-classification terms.
3. Confirm important data flows agree with the architecture.
4. Confirm access references agree with permission-boundaries.md.
5. Never include actual passwords, tokens, private keys, or secrets.
6. State logging restrictions explicitly for sensitive data.
7. Use synthetic or approved data for testing and demonstrations.
8. Do not invent unsupported retention or deletion guarantees.
9. Identify important external data flows.
10. Link data risks and open questions to authoritative evidence.
11. Verify important handling claims where practical.
12. Remove ALL instructional HTML comments.

The completed artifact should explain how important project data is handled
through its lifecycle without pretending that documentation alone provides
data protection.
-->
