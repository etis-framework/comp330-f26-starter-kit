# Tests

This directory contains executable tests used to verify the behavior of the
project's source code.

Tests should provide repeatable evidence that important requirements,
acceptance criteria, interfaces, defect fixes, and system behaviors continue to
work as intended.

This directory contains **test implementation**, not test planning or preserved
test-result artifacts.

Related engineering documentation is maintained under:

- `/docs/testing/test-strategy.md`
- `/docs/testing/test-plan.md`
- `/docs/testing/test-cases.md`
- `/docs/testing/ci-evidence.md`

Preserved output or other reviewable artifacts produced by test execution belong
under:

- `/test-evidence/`

## What Belongs Here

Depending on the technology stack and project architecture, this directory may
contain:

- unit tests;
- component tests;
- integration tests;
- contract tests;
- regression tests;
- security-focused tests;
- acceptance-test automation;
- test fixtures;
- test helpers;
- mocks or stubs used specifically for testing.

Do not create every category simply because it appears in this list.

Use the test types that provide meaningful verification for the actual system.

## Test Organization

Organize tests so another engineer can understand what is being verified.

Where practical, test structure should correspond to meaningful application
responsibilities, behaviors, or architectural boundaries.

For example:

    tests/
    ├── unit/
    ├── integration/
    ├── contract/
    └── regression/

The exact structure should reflect the project's language, framework, and
testing approach.

Do not create unnecessary directory layers merely to match this example.

## Test Naming

Use descriptive names that communicate the behavior being verified.

Prefer names that describe expected behavior, such as:

    test_valid_request_is_created
    test_missing_required_description_is_rejected
    test_user_cannot_access_another_users_request

Avoid names that reveal only implementation mechanics, such as:

    test_method_1
    test_handler
    test_new_code

A reviewer should be able to understand the intent of a test without first
reading its entire implementation.

## Requirements and Acceptance Criteria

Important tests should be traceable to the behavior they verify.

Where practical, connect significant tests to:

- requirement IDs;
- acceptance-criteria IDs;
- API or interface contracts;
- defect IDs;
- security rules;
- architecture responsibilities.

The broader traceability record is maintained in:

- `/docs/planning/traceability.md`

Do not force every low-level unit test to map directly to a requirement.

Traceability is most important for tests that support meaningful engineering or
release claims.

## Positive and Negative Paths

Tests should verify more than successful behavior.

Where relevant, include conditions such as:

- valid input;
- missing required input;
- invalid input;
- unauthorized access;
- missing resources;
- duplicate operations;
- invalid state transitions;
- dependency failures;
- boundary conditions.

Negative-path testing should focus on behavior that matters to correctness,
security, data integrity, or documented requirements.

## Regression Tests

When a meaningful defect is corrected, add or update a regression test where
practical so the same failure would be detected if it returned.

Defect evidence is maintained under:

- `/docs/quality/defect-log.md`

A useful engineering chain may look like:

    DEF-007
      ->
    Corrective implementation
      ->
    Regression test
      ->
    Passing CI evidence

## Test Independence

Tests should be as repeatable and independent as practical.

Avoid tests that depend unnecessarily on:

- execution order;
- manually prepared local state;
- another test having run first;
- hidden developer configuration;
- uncontrolled external data.

Where shared setup is required, make that setup explicit.

## Test Data

Use synthetic, controlled, or otherwise approved test data.

Do not place passwords, access tokens, private keys, secrets, or inappropriate
real-world sensitive information in test code or fixtures.

Data-handling guidance is maintained in:

- `/docs/security/data-handling-notes.md`

## Mocks and Stubs

Mocks, stubs, and fakes may be useful for isolating behavior, but they do not
prove that the real integration works.

When an important external or component boundary is mocked in one level of
testing, use appropriate integration or contract verification elsewhere when
the risk justifies it.

Tests should make clear when a dependency is simulated rather than real.

## CI

Tests intended to protect the shared codebase should run in Continuous
Integration where practical.

CI configuration and execution evidence are documented in:

- `/docs/testing/ci-evidence.md`

A local passing test is useful development evidence, but CI provides stronger
shared evidence that the test passed against a known repository baseline.

## Failed Tests

Do not disable, skip, delete, or weaken a meaningful failing test merely to make
the test suite pass.

When a test fails, determine whether:

- the implementation is wrong;
- the test expectation is wrong;
- the requirement changed;
- the environment is incorrect;
- an external dependency caused the failure.

Update the appropriate engineering evidence based on what is actually learned.

## Expectations

Tests in this directory should be:

- repeatable;
- understandable;
- relevant to meaningful system behavior;
- appropriately isolated;
- traceable where useful;
- safe to execute in their intended environment;
- free of embedded secrets;
- maintained when requirements or implementation change.

The test suite should provide engineering evidence about system behavior, not
simply increase a test-count number.
