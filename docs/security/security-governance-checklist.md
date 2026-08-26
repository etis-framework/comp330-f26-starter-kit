# Security Governance Checklist

<!--
STARTER KIT GUIDANCE — DELETE BEFORE PHASE-GATE SUBMISSION

This file provides a project-level review of important security responsibilities
and the evidence supporting them.

The purpose is NOT to create a generic cybersecurity checklist.

The purpose is to help the team ask:

- What security concerns actually matter to this system?
- Where are those concerns addressed?
- What evidence shows the control exists?
- What remains incomplete or uncertain?
- Who owns follow-up?

Security should be treated as an engineering responsibility that spans
requirements, architecture, implementation, verification, deployment, and
operations.

This file should reference authoritative evidence elsewhere rather than
duplicating detailed requirements, architecture, or tests.

Relevant evidence may include:

/docs/requirements/
/docs/architecture/
/docs/decisions/
/docs/security/permission-boundaries.md
/docs/security/data-handling-notes.md
/docs/quality/
/docs/operations/
/docs/observability/
/docs/planning/risk-register.md

IMPORTANT:

- Everything inside HTML comments like this is Starter Kit guidance.
- Remove ALL instructional comments before the applicable phase-gate submission.
- Examples inside comments are guidance only.
- Do not claim a security control exists unless actual evidence supports it.
- Do not invent enterprise security controls that are irrelevant to the project.
-->

## Security Review Identification

**Review Date:**  
**Applicable Gate / Milestone:**  
**System / Release Baseline:**  
**Reviewer(s):**  

<!--
TEAM CONTENT REQUIRED

Identify the actual engineering baseline being reviewed.

Where practical, reference:

- Git commit;
- release tag;
- phase-gate baseline;
- deployed version.

Do not leave placeholder metadata in the completed artifact.
-->

## Security Context

<!--
TEAM CONTENT REQUIRED

Briefly describe the security context of the system.

Consider:

- who uses the system;
- what valuable or sensitive data exists;
- what external services are trusted;
- what actions require authorization;
- what could go wrong if access controls fail;
- what deployment environment is used.

Do not attempt to write a complete threat model here.

Replace this comment with your team's actual security context.
-->

## Governance Checklist

<!--
TEAM CONTENT REQUIRED

Review each item based on your ACTUAL system.

Status values may include:

- Complete
- Partial
- Planned
- Not Applicable
- Gap

Evidence should reference real repository or runtime evidence.

Owner identifies who is responsible for resolving a gap or keeping the area
current.

Do not mark an item Complete merely because the team discussed it.
-->

| Security Area | Status | Evidence | Owner | Notes / Required Action |
|---|---|---|---|---|
| Authentication approach is defined |  |  |  |  |
| Authorization responsibilities are defined |  |  |  |  |
| Permission boundaries are documented |  |  |  |  |
| Sensitive data is identified |  |  |  |  |
| Data handling expectations are documented |  |  |  |  |
| Secrets and credentials are kept out of source control |  |  |  |  |
| Important security requirements are documented |  |  |  |  |
| Security-relevant assumptions and risks are visible |  |  |  |  |
| Important trust boundaries are understood |  |  |  |  |
| Input validation responsibilities are defined |  |  |  |  |
| Security-relevant failure behavior is defined |  |  |  |  |
| Important security behavior has verification evidence |  |  |  |  |
| Security-sensitive logging avoids inappropriate data exposure |  |  |  |  |
| Deployment configuration does not expose known secrets |  |  |  |  |
| Known security limitations are documented |  |  |  |  |

<!--
The checklist items above are intended to remain part of the finished artifact.

They are not sample project answers.

For items that genuinely do not apply, use "Not Applicable" and explain why.

Do not delete a checklist item merely because the answer is inconvenient.
-->

## Authentication Review

<!--
TEAM CONTENT REQUIRED

Summarize the current authentication approach.

Questions to consider:

- Who establishes user identity?
- Is authentication handled internally or by an external provider?
- Where is authenticated identity trusted?
- What happens when authentication fails?
- Does the system store credentials?

Reference architecture, requirements, or ADRs rather than duplicating them.

Replace this comment with the actual authentication review.
-->

## Authorization Review

<!--
TEAM CONTENT REQUIRED

Summarize how authorization decisions are made.

Reference:

/docs/security/permission-boundaries.md

Important questions include:

- What component makes authoritative authorization decisions?
- Is authorization enforced server-side or at another trusted boundary?
- Are UI restrictions incorrectly being treated as security controls?
- Are resource-level permissions required?
- What happens when access is denied?

Replace this comment with the actual review.
-->

## Sensitive Data Review

<!--
TEAM CONTENT REQUIRED

Summarize security concerns related to stored or transmitted data.

Reference:

/docs/security/data-handling-notes.md

Consider:

- authentication information;
- personal information;
- application records;
- logs;
- secrets;
- identifiers;
- external-service data.

Do not duplicate the complete data-handling artifact.
-->

## Secrets and Credential Handling

<!--
TEAM CONTENT REQUIRED

Document how the project avoids exposing secrets.

Consider:

- environment variables;
- deployment secret stores;
- local configuration;
- .gitignore;
- repository history;
- CI/CD secrets.

DO NOT place actual secret values in this file.

If secrets were accidentally committed, do not merely delete the current file.
Treat exposed credentials as compromised and rotate them as appropriate.

Replace this comment with the team's actual approach.
-->

## Input and Boundary Validation

<!--
TEAM CONTENT REQUIRED

Identify where untrusted input enters the system and which component is
responsible for authoritative validation.

Consider:

- browser or UI input;
- API requests;
- file uploads;
- query parameters;
- external-service responses;
- configuration.

Client-side validation may improve usability but should not be treated as
authoritative when requests can bypass it.

Reference component responsibilities and API contracts where useful.
-->

| Input / Boundary | Source | Authoritative Validator | Failure Behavior | Evidence |
|---|---|---|---|---|
|  |  |  |  |  |

## Security Verification

<!--
TEAM CONTENT REQUIRED

Identify actual verification performed for important security behavior.

Examples might include:

- unauthorized-access test;
- authentication-failure test;
- input-validation test;
- permission-boundary verification;
- secret scanning;
- code review;
- dependency review;
- runtime evidence.

Do not claim penetration testing, security auditing, or automated scanning
unless it actually occurred.

EXAMPLE ONLY:

| Security Concern | Verification | Result | Evidence |
|---|---|---|---|
| Unauthorized request access | Integration test using second user identity | Passed | AC-REQ-008-02 / test reference |

DELETE the example and populate the actual table below.
-->

| Security Concern | Verification | Result | Evidence |
|---|---|---|---|
|  |  |  |  |

## Security Risks and Open Questions

<!--
TEAM CONTENT REQUIRED

Reference rather than duplicate authoritative evidence from:

/docs/planning/risk-register.md
/docs/requirements/assumptions-open-questions.md

Include only risks or questions that materially affect security.
-->

| Risk / Question | Security Impact | Current Action / Monitoring |
|---|---|---|
|  |  |  |

## Known Security Limitations

<!--
TEAM CONTENT REQUIRED

Document actual security limitations that remain.

Examples might include:

- authorization model not yet fully implemented;
- recovery path not verified;
- external identity dependency;
- audit evidence incomplete;
- security verification limited to manual testing.

Do not hide important limitations.

Reference:

/docs/release/known-limitations.md

when the limitation affects a release.
-->

| Limitation | Impact | Disposition | Related Evidence |
|---|---|---|---|
|  |  |  |  |

## Required Security Actions

<!--
TEAM CONTENT REQUIRED

Convert meaningful gaps into concrete actions.

Use stable IDs when useful:

SEC-ACT-###

EXAMPLE ONLY:

| Action ID | Required Action | Driver | Owner | Target | Status |
|---|---|---|---|---|---|
| SEC-ACT-001 | Add resource-level authorization test for workflow history | Authorization review gap | Quality & Review Lead | A4 | Planned |

DELETE the example and populate actual actions below.
-->

| Action ID | Required Action | Driver | Owner | Target | Status |
|---|---|---|---|---|---|
|  |  |  |  |  |  |

## Review Conclusion

<!--
TEAM CONTENT REQUIRED

Summarize the current security posture based on actual evidence.

Do not write:

"System is secure."

Security is not a permanent binary state.

Instead, describe:

- what important controls are currently supported;
- what has been verified;
- what remains incomplete;
- what risk remains.

Replace this comment with the team's evidence-based conclusion.
-->

<!--
FINAL STARTER KIT CHECK — DELETE BEFORE PHASE-GATE SUBMISSION

Before submission:

1. Complete the security review identification.
2. Review every checklist item against actual evidence.
3. Use Not Applicable only with a clear reason.
4. Confirm permission references agree with permission-boundaries.md.
5. Confirm data references agree with data-handling-notes.md.
6. Confirm security risks exist in the authoritative risk register where appropriate.
7. Confirm verification claims point to real evidence.
8. Do not expose secrets or protected data in this file.
9. Record known security limitations honestly.
10. Convert meaningful gaps into owned actions.
11. Remove ALL instructional HTML comments.

The completed artifact should show how the team governs security-relevant
engineering decisions and evidence without pretending that a checklist alone
makes the system secure.
-->
