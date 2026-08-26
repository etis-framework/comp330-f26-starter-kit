# Test Evidence

This directory contains reviewable evidence produced by actual test and
verification activity.

It is intended to preserve evidence that supports engineering claims such as:

- a test was executed;
- a requirement or acceptance criterion was verified;
- a defect was reproduced or corrected;
- a regression test passed;
- a release candidate was validated; or
- a runtime or integration behavior was observed.

This directory contains **evidence produced by testing**, not the team's
testing strategy or planning documentation.

Testing documentation is maintained under:

- `/docs/testing/test-strategy.md`
- `/docs/testing/test-plan.md`
- `/docs/testing/test-cases.md`
- `/docs/testing/ci-evidence.md`

## Appropriate Evidence

Examples of artifacts that may belong here include:

- exported test reports;
- machine-generated test-result files;
- integration-test output;
- acceptance-test evidence;
- screenshots that demonstrate a specific verified behavior;
- logs captured for a defined verification scenario;
- performance or benchmark results;
- contract-test output;
- security-test evidence;
- regression-test results; and
- other reviewable artifacts produced during verification.

Only preserve evidence that has a clear engineering purpose.

## Evidence Organization

Use descriptive filenames and, where practical, organize evidence by release,
phase gate, test run, or verification activity.

For example:

    test-evidence/
    ├── a4/
    │   ├── integration-results.md
    │   └── authorization-test-results.md
    ├── a5/
    │   ├── acceptance-results.md
    │   └── regression-results.md
    └── release-1/
        └── verification-summary.md

The exact structure may differ based on the project's testing approach.

Avoid creating unnecessary folders or duplicating evidence already preserved
authoritatively elsewhere.

## Traceability

Important test evidence should be traceable to the engineering expectation it
supports.

Where practical, identify related evidence such as:

- requirement IDs;
- acceptance-criteria IDs;
- test-case IDs;
- defect IDs;
- CI evidence IDs;
- release or Git commit identifiers; and
- runtime-evidence IDs.

A useful evidence chain may look like:

    REQ-001
      ->
    AC-REQ-001-02
      ->
    TC-004
      ->
    Test execution
      ->
    test-evidence/a5/TC-004-result.md

Do not create traceability links to tests or evidence that did not actually
exist or execute.

## Generated Evidence

Machine-generated evidence may be stored here when it is useful for review or
historical verification.

Examples include:

- JUnit or similar test reports;
- coverage reports;
- static-analysis output; and
- benchmark results.

Do not commit large volumes of generated output merely because a tool produces
it.

Preserve only evidence that materially supports engineering review,
traceability, or release verification.

## Screenshots

Screenshots may be useful when they demonstrate behavior that is difficult to
capture otherwise.

A screenshot should have a clear verification purpose.

Avoid screenshots that merely show:

- that the application opened;
- that code exists;
- that a test command was typed; or
- that a user interface generally looks correct without an associated
  verification claim.

Where possible, accompany screenshots with enough context to explain:

- what was being verified;
- what the expected result was;
- what was observed; and
- what requirement, acceptance criterion, test case, or defect it relates to.

## Logs

Logs may be retained when they provide useful evidence for a specific test or
failure investigation.

Do not commit unrestricted application logs or large log dumps without a clear
reason.

Never place passwords, access tokens, private keys, secrets, or unnecessarily
sensitive information in committed test evidence.

## Evidence Integrity

Test evidence should represent what actually occurred.

Do not:

- create evidence for a test that was never executed;
- alter a failed result to make it appear successful;
- describe an expected result as an observed result;
- hide meaningful failures;
- claim evidence belongs to a different release or commit; or
- use AI-generated output as a substitute for actual test execution.

Failed tests can be valuable engineering evidence when they lead to defect
discovery, investigation, correction, and regression verification.

## Relationship to CI

CI results may be referenced here when preserved test artifacts provide useful
additional detail.

The authoritative summary of CI execution remains:

`/docs/testing/ci-evidence.md`

Avoid unnecessarily copying the same CI information into multiple locations.

## Expectations

Evidence stored in this directory should be:

- authentic;
- reviewable;
- relevant;
- traceable where practical;
- tied to a known test, release, or engineering claim;
- free of secrets and inappropriate sensitive data; and
- retained only when it provides meaningful engineering value.
