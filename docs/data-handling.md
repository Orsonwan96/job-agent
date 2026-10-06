# Data-handling decisions

Complete these decisions before sending private candidate data to any model provider.

## Model API boundary

- [ ] Decide which candidate fields may be sent to a model API.
- [ ] Select an acceptable provider and data-retention setting.
- [ ] Decide whether full resumes may be transmitted or only evidence records.

## Storage

- [ ] Decide where private candidate data is stored.
- [ ] Encrypt private data at rest where appropriate.
- [ ] Define retention periods for job postings, drafts, traces, and generated artifacts.
- [ ] Define a complete deletion procedure.

## Logging and observability

- [ ] Keep API keys, tokens, and credentials out of prompts and logs.
- [ ] Identify personal fields that must be redacted from traces.
- [ ] Decide whether raw prompts and responses may be retained.
- [ ] Define who may access logs and generated artifacts.

## Git policy

- Private candidate data belongs in `data/private/` and must not be committed.
- Generated application artifacts belong in `artifacts/` and must not be committed by default.
- Sanitized fixtures may be committed under `data/fixtures/`.
- Configuration examples must contain placeholders rather than real personal information.
