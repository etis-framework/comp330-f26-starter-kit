# Metrics Notes

<!--
STARTER KIT GUIDANCE — DELETE BEFORE PHASE-GATE SUBMISSION

This file defines the runtime metrics that matter to your project and explains
how the team intends to interpret them.

A metric is a measured value collected over time or across events.

Examples might include:

- request count;
- failure count;
- failure rate;
- response time;
- active jobs;
- queue depth;
- successful workflow completions;
- dependency failures.

Do NOT collect metrics simply because they are easy to collect.

Each metric should help answer an engineering or operational question.

This file defines metrics and their meaning.

Actual runtime observations and captured evidence belong in:

/docs/observability/runtime-evidence.md

IMPORTANT:

- Everything inside HTML comments is Starter Kit guidance.
- Remove all instructional comments before the applicable phase-gate submission.
- Examples are guidance only and must not become project evidence unless they
  independently describe your actual system.
-->

## Metric Catalog

<!--
TEAM CONTENT REQUIRED

Use stable metric IDs:

MET-###

Examples:

MET-001
MET-002
MET-003

Do not reuse an ID for a different metric after it has been referenced elsewhere.

COLUMN GUIDANCE

Metric
Use a clear name.

Type
Examples include Counter, Gauge, Rate, Duration, Distribution, or another
appropriate measurement type.

Definition
State exactly what is measured.

Unit
Examples: count, requests/second, milliseconds, percent.

Source
Identify the component or mechanism producing the measurement.

Engineering Question
State what the metric helps the team understand.

Status
Suggested values:

- Proposed
- Implemented
- Verified
- Deprecated
- Removed

EXAMPLE ONLY:

| ID | Metric | Type | Definition | Unit | Source | Engineering Question | Status |
|---|---|---|---|---|---|---|---|
| MET-001 | Request failure rate | Rate | Failed workflow requests divided by total workflow requests during the observation window | Percent | Application Service | Are user operations failing more frequently than expected? | Proposed |

DELETE the example and populate the actual table below.
-->

| ID | Metric | Type | Definition | Unit | Source | Engineering Question | Status |
|---|---|---|---|---|---|---|---|
|  |  |  |  |  |  |  |  |

## Interpretation and Expected Behavior

<!--
TEAM CONTENT REQUIRED FOR METRICS WHERE INTERPRETATION MATTERS

A number without context may not be useful.

Explain what values mean.

Do NOT invent arbitrary thresholds merely because this section exists.

At an early phase gate, it is acceptable to state that a useful baseline has
not yet been established.

Possible interpretations:

- zero failures is expected during a defined test;
- response time should remain within an agreed range;
- a sudden increase from baseline warrants investigation;
- the metric is informational and does not have an alert threshold.

EXAMPLE ONLY:

| Metric ID | Normal / Expected Behavior | Concerning Behavior | Basis |
|---|---|---|---|
| MET-001 | No failures during the defined acceptance scenario | Any repeatable failure during the scenario | Acceptance criteria and verification plan |

Populate the actual table below.
-->

| Metric ID | Normal / Expected Behavior | Concerning Behavior | Basis |
|---|---|---|---|
|  |  |  |  |

## Thresholds and Alerting

<!--
TEAM CONTENT REQUIRED ONLY WHERE A THRESHOLD IS MEANINGFUL

A threshold should have a reason.

Avoid arbitrary statements such as:

"Alert if CPU is over 80%"

unless the team has evidence or a justified operational reason for that value.

A metric does not need an alert threshold merely because it exists.

Possible threshold bases include:

- requirement;
- acceptance criterion;
- measured baseline;
- experiment;
- service-level expectation;
- known platform constraint;
- operational experience.

If no threshold has been established, state that honestly in the table.

EXAMPLE ONLY:

| Metric ID | Threshold / Trigger | Action | Basis |
|---|---|---|---|
| MET-001 | No fixed production threshold yet | Investigate repeatable failures observed during verification | Baseline not yet established |

Populate the actual table below if relevant.
-->

| Metric ID | Threshold / Trigger | Action | Basis |
|---|---|---|---|
|  |  |  |  |

## Collection and Calculation Notes

<!--
TEAM CONTENT REQUIRED WHEN A METRIC COULD BE MISINTERPRETED

Explain important details needed to reproduce or understand the metric.

Consider:

- observation window;
- numerator and denominator;
- excluded events;
- reset behavior;
- aggregation method;
- percentile calculation;
- sampling;
- environment differences.

EXAMPLE ONLY:

MET-001 calculation:

failed request count / total request count * 100

Observation window:
One verification run.

The example above is NOT project evidence. Replace this comment with actual
calculation or collection notes where needed.
-->

## Metric Relationships

<!--
OPTIONAL TEAM CONTENT

Some metrics are more useful when considered together.

Examples ONLY:

- request count + failure count -> failure rate;
- response time + dependency latency -> possible dependency bottleneck;
- workflow completion count + workflow failure count -> execution health.

Document relationships only when they help interpret your system.
-->

## Requirements and Verification Traceability

<!--
TEAM CONTENT REQUIRED WHERE METRICS SUPPORT REQUIREMENTS OR VERIFICATION

Metrics may provide evidence for:

- requirements;
- acceptance criteria;
- performance expectations;
- reliability expectations;
- operational checks;
- phase-gate verification.

Do not force every metric to map to a requirement.

EXAMPLE ONLY:

| Metric ID | Related Requirement / Criterion | How the Metric Supports Evidence |
|---|---|---|
| MET-001 | AC-REQ-004-02 | Helps quantify failed submissions during verification |

Populate the actual table below where applicable.
-->

| Metric ID | Related Requirement / Criterion | How the Metric Supports Evidence |
|---|---|---|
|  |  |  |

## Metric Limitations

<!--
TEAM CONTENT REQUIRED FOR IMPORTANT LIMITATIONS

Metrics can mislead.

Identify limitations such as:

- only collected in one environment;
- no historical baseline;
- small sample size;
- metric does not distinguish failure categories;
- instrumentation may miss client-side failures;
- values reset at application restart.

A known limitation is useful engineering evidence.

Use the table below for material limitations.
-->

| Metric ID | Limitation | Impact on Interpretation |
|---|---|---|
|  |  |  |

<!--
FINAL STARTER KIT CHECK — DELETE BEFORE PHASE-GATE SUBMISSION

Before submission:

1. Define only metrics that are meaningful to the actual project.
2. Replace all blank scaffold rows with actual content or remove unnecessary rows.
3. Confirm every metric definition is precise enough to interpret.
4. Confirm metric IDs are unique and consistent with observability-plan.md.
5. Avoid unsupported or arbitrary thresholds.
6. Link metrics to requirements or verification only where the relationship is real.
7. Record known limitations honestly.
8. Remove ALL instructional HTML comments.

The finished file should explain what the team measures and what those
measurements mean. It should not be a generic monitoring checklist.
-->
