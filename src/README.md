# Source Code

This directory contains the application's production source code.

Project implementation should be organized here using a structure that reflects
the team's architecture, component responsibilities, and technology stack.

## Expectations

Source code placed here should:

- implement approved project requirements and acceptance criteria;
- remain consistent with the documented architecture;
- respect component and permission boundaries;
- use clear, maintainable organization and naming;
- include appropriate error handling and validation;
- avoid unnecessary duplication and tightly coupled responsibilities;
- be supported by relevant automated or manual verification evidence.

Do not place unrelated notes, temporary experiments, generated output, build
artifacts, or documentation-only files in this directory.

## Structure

Organize source code around meaningful application responsibilities rather than
creating folders only to mirror arbitrary technical categories.

As the project evolves, the source structure should remain consistent with:

- `/docs/architecture/architecture.md`
- `/docs/architecture/component-responsibilities.md`
- `/docs/architecture/api-contracts.md`
- `/docs/security/permission-boundaries.md`

If the implementation requires a meaningful change to the documented
architecture, update the engineering evidence rather than allowing the source
code and architecture to silently diverge.

## Configuration and Secrets

Do not hard-code passwords, access tokens, private keys, connection secrets, or
other protected credentials in source code.

Use the project's approved configuration and secret-management mechanisms.

Configuration needed to understand or operate the application should be
documented in the appropriate operational or deployment evidence.

## Testing

Production source code should be supported by appropriate verification.

Tests should normally reside in the project's designated test location rather
than being mixed indiscriminately with production code, unless the language,
framework, or project structure intentionally places them together.

Related testing evidence is maintained under:

- `/docs/testing/`
- `/docs/quality/`

## Traceability

For significant functionality, the team should be able to trace implementation
back to relevant engineering evidence such as:

- requirements;
- acceptance criteria;
- architecture components;
- API or interface contracts;
- architecture decisions;
- defects or corrective actions.

The implementation itself is part of the engineering evidence chain, not a
replacement for that evidence.
