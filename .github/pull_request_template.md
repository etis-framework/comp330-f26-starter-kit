# Pull Request

<!--
Use this template to explain the engineering change being proposed.

A pull request should make it possible for another engineer to understand:

- what changed;
- why the change is needed;
- what engineering evidence it relates to;
- how the change was verified;
- what risks or limitations remain.

Keep the PR concise, but provide enough evidence for meaningful review.

HTML comments like this are guidance only and will not appear in the submitted
pull request.
-->

## Summary

<!--
Briefly describe what this pull request changes.

Focus on meaningful behavior or engineering outcomes rather than listing every
modified file.

Prefer:
"Adds server-side validation for required workflow fields and regression
coverage for DEF-004."

Avoid:
"Updated validation.py and tests.py."
-->

## Why

<!--
Explain what motivated this change.

Where applicable, reference:

- requirement;
- acceptance criterion;
- defect;
- issue;
- architecture decision;
- task;
- risk;
- review finding;
- operational need.

The reviewer should understand WHY this change exists before reviewing HOW it
was implemented.
-->

## Related Engineering Evidence

<!--
Link the evidence that defines or motivates the change.

Examples:
- REQ-###
- AC-REQ-###-##
- DEF-###
- ADR-###
- API-###
- R-###
- TASK-###
- review finding
- related issue
- relevant documentation path

Include only evidence that actually relates to this change.
-->

- 

## What Changed

<!--
Summarize the important implementation or evidence changes.

Include significant areas such as:

- application behavior;
- architecture or interface;
- test coverage;
- configuration;
- documentation;
- operational behavior.

Do not reproduce the Git diff.
-->

- 

## Verification

<!--
Describe how the change was verified.

Do not write only:
"Tests pass."

Identify the meaningful verification performed.

Examples:
- unit tests;
- integration tests;
- acceptance criteria;
- regression tests;
- manual verification;
- CI run;
- runtime evidence.

If important verification could not be completed, state that under
Risks / Limitations rather than implying complete verification.
-->

- [ ] Relevant automated tests were run
- [ ] New or changed behavior was verified
- [ ] Negative or failure behavior was reviewed where relevant
- [ ] Regression coverage was added or updated where appropriate
- [ ] CI checks pass where CI is configured
- [ ] Documentation and traceability were updated where needed

### Verification Evidence

<!--
Reference reviewable evidence.

Examples:
- test case IDs;
- CI run;
- test-evidence path;
- runtime evidence;
- screenshots where appropriate;
- acceptance criterion result.

Remove this subsection only if the verification description above already
contains sufficient evidence.
-->

- 

## Architecture / Interface Impact

<!--
Complete this section when the change materially affects architecture,
component responsibilities, interfaces, or contracts.

Consider whether updates are required to:

- /docs/architecture/architecture.md
- /docs/architecture/component-responsibilities.md
- /docs/architecture/api-contracts.md
- /docs/decisions/

If there is no meaningful architecture or interface impact, state:

None identified.
-->

## Security / Data Impact

<!--
Complete this section when the change affects:

- authentication;
- authorization;
- permission boundaries;
- sensitive data;
- secrets;
- logging of sensitive information;
- external data flows.

Reference /docs/security/ where appropriate.

If there is no meaningful security or data impact, state:

None identified.
-->

## Risks / Limitations / Follow-Up

<!--
Identify known concerns that remain after this change.

Examples:
- known limitation;
- deferred work;
- unresolved risk;
- test gap;
- operational limitation;
- follow-up task.

Do not hide known issues simply to make the PR appear complete.

If none are known, state:

None identified.
-->

## Reviewer Focus

<!--
Optional but useful for significant changes.

Tell reviewers where engineering judgment is especially needed.

Examples:
- authorization boundary;
- state transition behavior;
- API compatibility;
- failure handling;
- migration logic;
- concurrency behavior;
- test adequacy.

Remove this section if no specific review focus is needed.
-->

## Issue / Work Item

<!--
Use GitHub closing syntax when this PR should close an issue.

Examples:

Closes #42
Fixes #27

If the PR should not automatically close an issue, replace or remove the line
below.
-->

Closes #
