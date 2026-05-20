# Failure Matrix: Durate Preflight

| Scenario | Failure mode | Metric | Gate | Evidence |
| --- | --- | --- | --- | --- |
| durate evidence replay | durate_drift | durate_coverage | block release until cited evidence is regenerated | ev_0000 |
| plain operator packet | plain_blindspot | plain_latency | accept only if decision claims cite fixture evidence | ev_0007 |
| plain operator packet | plain_blindspot | plain_latency | accept only if decision claims cite fixture evidence | ev_0011 |
| leans regression harness | leans_misroute | leans_precision | open a regression issue with trace and benchmark delta | ev_0014 |
| marketing boundary probe | marketing_gap | marketing_risk | route to reviewer with evidence packet | ev_0021 |
| leans regression harness | leans_misroute | leans_precision | open a regression issue with trace and benchmark delta | ev_0022 |
| durate evidence replay | durate_drift | durate_coverage | block release until cited evidence is regenerated | ev_0028 |
