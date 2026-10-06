# Job Agent

A learning project for building a grounded job-search assistant that discovers and ranks jobs, then prepares truthful, reviewable application packets.

## Current scope

The first release targets **Stage 2: Prepare**:

- ingest approved job sources;
- normalize and deduplicate postings;
- evaluate fit using hard rules plus model judgment;
- tailor application materials from verified evidence;
- validate every generated claim; and
- present the packet for human review and submission.

Automated application submission is explicitly out of scope for the first release.

## Current milestone

**Week 0 — Policy, success criteria, and seed data**

1. Complete the private candidate profile from the provided example.
2. Review and customize the operating policy.
3. Finish the data-handling decisions.
4. Define metric calculations and release gates.
5. Label the first 10–15 historical jobs.

## Planning document

[Building an Autonomous Job Application Agent — Learning and Implementation Plan](https://docs.google.com/document/d/1xDiS3xG2dpGwSvJk5RMJKcqJgiFtyxVL0kdKQ1-ZBHg/edit)

## Repository layout

```text
config/          Shareable configuration templates and non-secret policy
data/fixtures/   Sanitized job-description fixtures
data/private/    Private candidate and job data; ignored by Git
docs/            Architecture, privacy, metrics, and decisions
evals/           Labeling guidance and evaluation assets
src/job_agent/   Application source code
tests/           Automated tests
artifacts/       Generated resumes and reports; ignored by Git
```

## Development status

The project is initialized but intentionally contains no agent implementation yet. Week 1 begins with a typed `JobPosting` schema and structured extraction fixtures.
