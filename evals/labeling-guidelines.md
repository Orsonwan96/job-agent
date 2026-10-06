# Job-labeling guidelines

Use these labels consistently when creating the historical-job evaluation set.

## `pursue`

The job passes all known hard constraints and is meaningfully aligned with the candidate's skills and career direction.

## `review`

The job may be suitable, but important information is missing or a material tradeoff requires judgment.

## `skip`

The job violates a hard constraint or is clearly misaligned with the candidate's goals.

## Required fields

Each label must contain:

- a stable local identifier;
- title and company;
- `pursue`, `review`, or `skip`;
- a one-sentence decision reason;
- any hard-constraint failures;
- important positive signals; and
- important gaps or uncertainties.

## Seed-set composition

The first 10–15 jobs should include:

- obvious pursue cases;
- obvious skip cases;
- borderline review cases;
- an incomplete posting;
- a misleading or inflated posting; and
- a posting containing irrelevant or prompt-injection-like instructions.

## JSONL example

```json
{"id":"job-001","title":"Senior Backend Engineer","company":"Example","decision":"pursue","reason":"Strong distributed-systems fit and acceptable location.","hard_constraint_failures":[],"important_positive_signals":["Python","distributed systems"],"important_gaps":["limited Kubernetes evidence"]}
```
