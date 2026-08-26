---
name: Defect Report
about: Report incorrect, unexpected, or failed system behavior
title: ""
labels: ""
assignees: ""
---

# Defect Report

<!--
Use this template when actual system behavior differs from an expected
requirement, acceptance criterion, interface contract, test expectation, or
other established engineering behavior.

Record what actually happened. Do not guess at the root cause unless evidence
supports it.

HTML comments like this are guidance only and will not appear in the submitted
GitHub issue.
-->

## Summary

<!--
Briefly describe the observed defect.

Prefer a specific behavioral statement.

Example:
"Submitting a request with a whitespace-only description creates a workflow
record instead of rejecting the request."
-->

## Environment / Baseline

<!--
Identify where the defect occurred.

Include information useful for reproducing the same system state, such as:
- local / CI / test / deployed environment;
- branch;
- commit;
- release or tag;
- browser or platform when relevant.

Do not include credentials or secrets.
-->

## Steps to Reproduce

<!--
Provide the smallest repeatable sequence that demonstrates the problem.

Include required starting state or test data when relevant.
-->

1. 
2. 
3. 

## Expected Behavior

<!--
What should have happened?

Where possible, reference the requirement, acceptance criterion, API contract,
test case, or other evidence establishing the expectation.
-->

## Actual Behavior

<!--
What actually happened?

Describe the observed result rather than an assumed cause.
-->

## Reproducibility

<!--
How consistently does the problem occur?

Examples:
- Every time
- Intermittently
- Once so far
- Unable to reproduce consistently

Include relevant conditions when known.
-->

## Impact

<!--
Describe the practical consequence.

Consider:
- user impact;
- incorrect state;
- security;
- data integrity;
- requirement satisfaction;
- testing;
- deployment;
- operations;
- release readiness.

Do not exaggerate the impact.
-->

## Evidence

<!--
Link or attach useful evidence.

Examples:
- failing test;
- CI run;
- screenshot;
- relevant log excerpt;
- runtime-evidence entry;
- test-case result.

Never include passwords, tokens, private keys, or unnecessarily sensitive data.
-->

## Related Engineering Evidence

<!--
Link relevant evidence when applicable.

Examples:
- REQ-###
- AC-REQ-###-##
- TC-###
- API-###
- ADR-###
- RUN-###
- related defect;
- pull request;
- relevant documentation path.
-->

## Investigation / Notes

<!--
Add investigation findings here as evidence develops.

Distinguish clearly between:
- observed fact;
- current hypothesis;
- confirmed cause.

Do not rewrite the original defect description merely because the team later
learned more about the cause.
-->

## Resolution Evidence

<!--
Complete this section when the defect is resolved.

Reference:
- fixing pull request or commit;
- regression test;
- CI evidence;
- rerun test case;
- updated engineering evidence.

A code change by itself does not demonstrate that the defect is resolved.
-->
