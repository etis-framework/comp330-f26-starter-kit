# Data

This directory contains project data artifacts that are intentionally stored in
the repository.

Examples may include:

- small reference datasets;
- seed data;
- controlled test data;
- lookup tables;
- static configuration data;
- sample input files;
- data fixtures shared across the team.

Only place data here when keeping it in version control is appropriate and
useful to the project.

## What Belongs Here

Data stored in this directory should be:

- intentionally part of the project;
- understandable by another team member;
- small enough to manage reasonably in Git;
- safe to store in the repository;
- free of secrets and inappropriate sensitive information;
- documented when its purpose or format is not obvious.

Do not use this directory as a general dumping location for files produced
during development.

## What Does Not Belong Here

Do not commit:

- passwords;
- API keys;
- access tokens;
- private keys;
- connection secrets;
- credentials;
- real sensitive personal information;
- confidential institutional data;
- unrestricted production exports;
- large generated datasets;
- database files created only by local development;
- temporary files;
- cache files;
- logs;
- test-result output that belongs under `/test-evidence/`.

If a file is generated automatically and can be recreated reliably, consider
whether it belongs in version control at all.

## Test and Sample Data

Prefer synthetic or intentionally created data for:

- tests;
- demonstrations;
- development;
- examples.

Test data should be realistic enough to exercise meaningful behavior without
introducing unnecessary privacy or security concerns.

Related guidance is maintained in:

- `/docs/security/data-handling-notes.md`
- `/docs/testing/test-strategy.md`
- `/docs/testing/test-plan.md`

## Data Organization

Use descriptive filenames and organize files according to their engineering
purpose.

For example:

    data/
    ├── seed/
    ├── fixtures/
    ├── reference/
    └── samples/

The project does not need to use this exact structure.

Create subdirectories only when they improve clarity.

## Data Formats

Prefer formats that are:

- appropriate for the application;
- understandable by the team;
- easy to review when practical;
- supported by the project's tooling.

Common examples may include:

- JSON;
- CSV;
- YAML;
- SQL seed files;
- other structured formats required by the project.

When a file format or schema is not self-explanatory, document:

- what the file contains;
- what consumes it;
- whether it is authoritative;
- how it should be updated.

## Data Ownership

Where important, identify which system or component is authoritative for the
data.

Repository data may be:

- authoritative project reference data;
- seed data used to initialize another data store;
- test fixtures;
- examples only.

Do not allow sample or fixture data to be mistaken for authoritative runtime
data.

Architecture and data ownership should remain consistent with:

- `/docs/architecture/architecture.md`
- `/docs/architecture/component-responsibilities.md`
- `/docs/security/data-handling-notes.md`

## Sensitive Data

Before committing data, consider whether it contains:

- personal information;
- authentication information;
- protected identifiers;
- internal-only information;
- confidential project information.

If the data is sensitive or its handling is unclear, do not commit it until the
team has determined the appropriate handling approach.

Never commit secrets.

## Large Files and Generated Data

Git is not intended to serve as general-purpose storage for large datasets or
frequently changing generated output.

Before committing a large or generated data artifact, ask:

- Does the team need this file to reproduce or understand the project?
- Can it be generated instead?
- Does it change frequently?
- Does it belong in another storage location?
- Will it create unnecessary repository history?

If the answer suggests that repository storage is inappropriate, document how
the data is obtained or generated instead.

## Changes to Data

Changes to important project data should receive the same engineering care as
source-code changes when they can affect system behavior.

Review:

- schema changes;
- seed-data changes;
- lookup-table changes;
- test-fixture changes;
- data that influences requirements or expected behavior.

Where appropriate, update related tests, documentation, and traceability.

## Expectations

Data committed under this directory should be:

- intentional;
- relevant;
- understandable;
- appropriately organized;
- safe to store in version control;
- free of secrets;
- traceable to its purpose where useful;
- maintained when related system behavior changes.
