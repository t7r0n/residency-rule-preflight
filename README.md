# Durate Preflight

A compliance pre flight layer for Durate that converts plain English rules into typed constraints, statically proves every published schedule against the ACGME Common Program Requirements + specialty supplements, and produces an auditor ready PDF showing exactly which rule check passed which clause.

## Why This Exists

Durate's marketing leans on "plain English" rule configuration (YC profile). For residency programs the rule set is non trivial: the ACGME Common Program Requirements for Residency 2025 (acgme.org) defines specific maximum hour rules (80h/wk averaged over 4 weeks, 24+4 max continuous, 14h off after 24, 1 in 7 free, in house call no more frequent than every third night), and each specialty layers further requirements.

## What It Builds

- Replays synthetic `durate` and `marketing` cases against the project's evidence rules.
- Scores `durate_coverage`, `marketing_risk`, and `leans_precision` so regressions are visible in CSV and JSON.
- Plants `durate drift` and `marketing gap` failures as negative controls.
- Writes citation-locked decision claims; unsupported claims fail verification.
- Exports a review dashboard and demo pack for `durate-preflight` without hosted services.

## Local Run

```bash
uv sync
uv run durate-preflight all
uv run pytest -q
uv run ruff check .
```

## Outputs

- `outputs/analysis.json`
- `outputs/scenario_report.csv`
- `outputs/decision_report.md`
- `outputs/evidence_packet.md`
- `outputs/dashboard.html`
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

This repository uses synthetic fixtures only. It has no credentials, no customer data, no outreach data, and no dependency on a hosted API.
