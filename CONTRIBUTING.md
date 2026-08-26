# Contributing

This repository is a team engineering workspace for COMP 330/474 Software
Engineering.

Contributions should improve both the software system and the engineering
evidence needed to understand, review, verify, operate, and evolve it.

Repository activity alone is not evidence of engineering quality. Issues,
branches, commits, pull requests, tests, reviews, and documentation should
represent meaningful engineering work.

## Team Working Agreement

Each team should establish and maintain its working agreement in:

`/docs/team/working-agreements.md`

The working agreement should define the team's specific practices for
communication, ownership, branching, commits, review, testing, and completion.

This file establishes the repository-wide contribution expectations that apply
regardless of the team's additional working agreements.

## Engineering Workflow

For substantive work, use the following general workflow:

1. Identify the engineering need.
2. Create or reference the appropriate GitHub issue.
3. Identify related requirements, defects, decisions, risks, or other evidence.
4. Create a focused branch.
5. Implement the change.
6. Add or update appropriate verification.
7. Update affected engineering evidence.
8. Open a pull request.
9. Complete meaningful peer review.
10. Resolve required review findings.
11. Verify required checks.
12. Merge only when the change is ready.

Not every trivial edit requires the same level of process.

Use engineering judgment, but preserve review and traceability for changes that
materially affect system behavior or engineering evidence.

## Issues

Use the repository's issue templates for meaningful work.

Available issue types include:

- **Task** — actionable engineering work;
- **Feature Request** — a proposed new or materially changed capability;
- **Defect Report** — incorrect, unexpected, or failed system behavior.

Issues should explain the engineering need rather than serving only as generic
to-do items.

Where applicable, link issues to relevant evidence such as:

- requirements;
- acceptance criteria;
- defects;
- risks;
- ADRs;
- API contracts;
- review findings;
- phase-gate evidence.

Do not create artificial issues solely to increase repository activity.

## Branches

Use short, descriptive branch names that communicate the purpose of the work.

Examples:

- `feature/authentication`
- `fix/session-timeout`
- `docs/architecture-update`
- `test/workflow-edge-cases`
- `security/authorization-check`
- `ops/health-check`

Avoid vague branch names such as:

- `changes`
- `updates`
- `work`
- `test2`

The team may define a more specific branch convention in its working agreement.

## Commits

Commits should represent understandable increments of engineering work.

Use concise commit messages that describe the outcome of the change.

Prefer:

- `Add request validation`
- `Fix authorization regression`
- `Update workflow API contract`
- `Add persistence integration tests`

Avoid:

- `update`
- `changes`
- `fix stuff`
- `final`
- `final2`

Where a change requires additional context, include an extended commit
description explaining the engineering intent.

Do not combine unrelated changes into one commit merely for convenience.

## Pull Requests

Substantive changes should normally be integrated through pull requests.

Use the repository pull-request template.

A useful pull request should make clear:

- what changed;
- why the change was needed;
- what engineering evidence motivated or defines the change;
- how the change was verified;
- whether architecture, interfaces, security, or data handling are affected;
- what risks or limitations remain; and
- what reviewers should focus on.

Link the pull request to its corresponding issue when appropriate.

A pull request should contain enough information for another engineer to review
the change without reconstructing its purpose from the diff alone.

## Code Review

Peer review should evaluate engineering quality rather than merely confirm that
a pull request exists.

Reviewers should consider areas relevant to the change, including:

- correctness;
- requirements and acceptance criteria;
- architecture and component boundaries;
- API or interface contracts;
- readability and maintainability;
- error and failure handling;
- security and authorization;
- data integrity;
- test adequacy;
- operational impact;
- documentation and traceability.

Review depth should be proportional to the importance and risk of the change.

Do not approve a change simply because the code compiles or automated tests
pass.

Review guidance and examples are maintained under:

`/docs/review/`

## Testing and Verification

Changes that affect behavior should include appropriate verification.

Depending on the change, this may include:

- unit tests;
- integration tests;
- contract tests;
- regression tests;
- acceptance verification;
- security-focused tests;
- runtime verification;
- manual review where human judgment is required.

Testing guidance is maintained under:

`/docs/testing/`

Executable tests belong under:

`/tests/`

Preserved test artifacts may belong under:

`/test-evidence/`

Do not weaken, remove, skip, or bypass a meaningful failing test merely to make
a change mergeable.

## Continuous Integration

The Starter Kit initially contains a guard workflow rather than
project-specific CI.

Teams are responsible for replacing that guard with meaningful automated build
and test checks appropriate to the project's actual technology stack.

Once configured, CI should:

- execute meaningful automated checks;
- fail when required checks fail;
- run against known repository baselines;
- avoid hard-coded secrets;
- use only necessary GitHub permissions; and
- provide reviewable engineering evidence.

CI evidence is documented in:

`/docs/testing/ci-evidence.md`

A green workflow is evidence only for the checks the workflow actually
performed.

## Engineering Evidence

Implementation and engineering documentation must remain consistent.

When a change affects an authoritative artifact, update that artifact as part
of the same engineering work where practical.

Relevant evidence may include:

- `/docs/requirements/`
- `/docs/architecture/`
- `/docs/decisions/`
- `/docs/planning/`
- `/docs/testing/`
- `/docs/security/`
- `/docs/quality/`
- `/docs/release/`
- `/docs/operations/`
- `/docs/observability/`
- `/docs/review/`
- `/docs/ai/`

Do not allow source code and engineering evidence to silently diverge.

## Traceability

Meaningful changes should be traceable where appropriate.

A typical relationship may include:

    Engineering Need
      ->
    Issue / Requirement / Defect
      ->
    Decision or Design
      ->
    Implementation
      ->
    Test / Review
      ->
    Verification Evidence
      ->
    Release Evidence

Not every change requires every link.

The goal is useful engineering traceability, not paperwork.

## AI-Assisted Contributions

AI may assist development, analysis, testing, review, or documentation, but it
does not replace human engineering responsibility.

Contributors remain responsible for:

- understanding AI-assisted work;
- reviewing generated output;
- independently verifying important claims;
- rejecting incorrect or inappropriate recommendations;
- preserving required AI-use evidence; and
- making final engineering decisions.

AI policy and evidence are maintained under:

`/docs/ai/`

Do not submit AI-generated work that the contributor or team cannot explain,
verify, and defend.

## Security and Sensitive Information

Never commit:

- passwords;
- access tokens;
- private keys;
- API secrets;
- database credentials;
- protected authentication material;
- inappropriate sensitive personal information.

Use approved configuration and secret-management mechanisms.

Security and data-handling evidence is maintained under:

`/docs/security/`

If a credential is accidentally committed, treat it as potentially compromised.
Removing the current file alone does not remove the value from repository
history or make the credential safe to continue using.

## Documentation Changes

Documentation is engineering evidence and should receive appropriate review.

When changing documentation:

- preserve accuracy;
- update stale references;
- maintain terminology consistency;
- verify repository paths and links;
- avoid duplicating authoritative evidence;
- keep lifecycle artifacts synchronized with relevant implementation changes.

Documentation-only changes may use a lighter review process when appropriate,
but they should still represent accurate engineering work.

## Definition of Ready to Merge

Before merging a substantive change, confirm as appropriate that:

- the engineering need is understood;
- implementation is complete;
- applicable tests have been executed;
- required review findings are resolved;
- CI passes where configured;
- related documentation is current;
- traceability has been updated where needed;
- known risks or limitations are documented; and
- no secrets or inappropriate sensitive information were introduced.

The team's working agreement may define additional completion criteria.

## Evidence Integrity

Engineering evidence must represent what actually occurred.

Do not:

- fabricate tests or test results;
- fabricate reviews;
- create fictional defects or incidents;
- claim verification that did not occur;
- hide meaningful failures;
- manufacture GitHub activity solely to satisfy an expected pattern;
- describe AI-generated predictions as observed system behavior.

Failed tests, rejected approaches, defects, limitations, and changed decisions
can all be valuable engineering evidence when they accurately show how the team
learned and improved.
