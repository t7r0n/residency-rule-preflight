# Decision Report: Durate Preflight

A compliance pre flight layer for Durate that converts plain English rules into typed constraints, statically proves every published schedule against the ACGME Common Program Requirements + specialty supplements, and produces an auditor ready PDF showing exactly which rule check passed which clause.

## Evidence-Grounded Findings

CLAIM: durate drift should `block release until replay is understood` because blocks=2 reviews=3 mean_severity=2.5. [EVID: ev_0088]
CLAIM: durate evidence recall should `block release until replay is understood` because blocks=3 reviews=3 mean_severity=1.875. [EVID: ev_0132]
CLAIM: leans failure replay should `block release until replay is understood` because blocks=2 reviews=4 mean_severity=3.333. [EVID: ev_0044]
CLAIM: marketing gap should `block release until replay is understood` because blocks=3 reviews=2 mean_severity=3.333. [EVID: ev_0011]
CLAIM: marketing reviewer handoff should `block release until replay is understood` because blocks=2 reviews=4 mean_severity=2.583. [EVID: ev_0121]
CLAIM: plain policy boundary should `block release until replay is understood` because blocks=2 reviews=3 mean_severity=1.708. [EVID: ev_0033]
