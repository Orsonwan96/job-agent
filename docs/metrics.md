# Metrics and release gates

## Week 0 decisions

For each metric, define the calculation, dataset, owner, and acceptable threshold.

| Metric | Calculation | Initial threshold | Notes |
|---|---|---:|---|
| Job-extraction field accuracy | TBD | TBD | Measure important fields separately. |
| Missing-field honesty | TBD | TBD | Missing information must remain unknown. |
| Hard-filter accuracy | Correct hard-filter decisions / labeled cases | 100% | Required before daily use. |
| Ranking agreement | TBD | TBD | Compare pursue/review/skip and rationale. |
| Retrieval precision | TBD | TBD | Measure requirement-to-evidence matches. |
| Evidence coverage | TBD | TBD | Measure supported requirements found. |
| Unsupported-claim rate | Unsupported claims / audited claims | 0 known | Required before daily use. |
| Resume edit acceptance | Accepted generated edits / reviewed edits | TBD | Primary Stage 2 quality metric. |
| Cost per analyzed job | Total model cost / analyzed jobs | TBD | Record by model and prompt version. |
| Latency per analyzed job | TBD | TBD | Report median and tail latency. |

## Stage 2 release gates

- [ ] Hard-filter accuracy is 100% on the labeled evaluation set.
- [ ] No known fabricated claims exist in the held-out adversarial set.
- [ ] Sensitive question categories reliably route to review.
- [ ] The evaluation harness runs for every prompt, schema, and model change.
