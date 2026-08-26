# scripts

# Scripts

This directory contains project scripts used to support development, testing,
verification, deployment, maintenance, or other repeatable engineering tasks.

Examples may include:

- local development setup or startup scripts;
- database initialization or migration helpers;
- test or verification scripts;
- build or packaging helpers;
- deployment utilities;
- data-generation or test-fixture scripts;
- maintenance or administrative utilities.

## Expectations

Scripts placed here should:

- perform a meaningful and repeatable engineering task;
- use clear, descriptive filenames;
- be understandable by another team member;
- avoid hard-coded passwords, tokens, private keys, or other secrets;
- fail clearly when required inputs or dependencies are missing;
- document important prerequisites or usage when the purpose is not obvious;
- remain consistent with the current project architecture and operational procedures.

Do not place one-time personal utilities, temporary experiments, generated
output, or unrelated files in this directory.

## Usage Documentation

If a script requires arguments, environment variables, dependencies, or a
specific execution sequence, document that information either:

- in comments or help text within the script; or
- in this README when the guidance applies to multiple scripts.

For significant operational or deployment scripts, also reference the
appropriate engineering documentation, such as:

- `/docs/operations/runbook.md`
- `/docs/testing/`
- `/docs/observability/`

## Security

Never commit credentials or secret values in scripts.

Use the project's approved configuration or secret-management mechanism when a
script requires access to protected resources.
