# Durate Preflight

A compliance pre flight layer for Durate that converts plain English rules into typed constraints, statically proves every published schedule against the ACGME Common Program Requirements + specialty supplements, and produces an auditor ready PDF showing exactly which rule check passed which clause.

![Durate Preflight working dashboard](outputs/project_working.svg)

## Why it exists

Durate's marketing leans on "plain English" rule configuration (YC profile).

Most internal demos stop at a pretty chart. This repository is built around the harder part: a repeatable path from fixture, to failure, to evidence, to the operator action a serious team would actually trust.

## What is inside

- A deterministic replay harness tuned around durate, marketing, and leans.
- Company-specific strategy code in `src/durate_preflight/strategy.py`, not just README-level customization.
- Citation-locked reports where every decision claim has to point back to a generated evidence ID.
- Two visual artifacts generated from the latest run: `outputs/project_working.svg` and `outputs/evidence_map.svg`.
- A portable demo pack with JSON, CSV, Markdown, HTML, SVG, and benchmark artifacts.

![Durate Preflight evidence map](outputs/evidence_map.svg)

## Signals it measures

- `durate coverage`
- `marketing risk`
- `leans precision`
- `plain latency`

## Failure modes it plants

- durate drift
- marketing gap
- leans misroute
- plain blindspot

## Run it locally

```bash
uv sync
uv run durate-preflight all
uv run pytest -q
uv run ruff check .
```

## Outputs worth opening

- `outputs/dashboard.html`
- `outputs/project_working.svg`
- `outputs/evidence_map.svg`
- `outputs/operator_brief.md`
- `outputs/decision_report.md`
- `outputs/strategy_model.json`
- `outputs/demo_pack.zip`

## Sources

- https://www.crunchbase.com/organization/docflow-61f0
- https://www.durate.com/products/specialties/other
- https://bem.durate.com/
- https://foundertrace.com/companies/durate_yc_f24/
- https://www.linkedin.com/posts/michael-mounajjed_excited-to-say-ben-liu-and-i-have-left-rice-activity-7261425844105994241-7hMX
- https://www.acgme.org/globalassets/pfassets/programrequirements/2025-reformatted-requirements/cprresidency_2025_reformatted.pdf
- https://pmc.ncbi.nlm.nih.gov/articles/PMC4304277/
- https://pmc.ncbi.nlm.nih.gov/articles/PMC10790185/
- https://www.bidmcharvardpsychiatry.org/residentlife/callschedule.html
- https://github.com/Z3Prover/z3

## Boundary

Everything runs locally against synthetic fixtures. There are no credentials, no customer records, no outreach files, and no hosted API dependency.
