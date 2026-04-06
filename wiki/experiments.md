# Experiments

| Experiment | Claim | Method | Conclusion |
| --- | --- | --- | --- |
| [Evolvable Gestation](experiments/evolvable_gestation.md) | Evolvable gestation can expand the reachable set of viable life-history strategies by making parental investment ecology-dependent. | Implemented evolvable `gestation_ticks` with offspring transfer energy `100 + 100 * gestation_ticks`; compared evolvable populations against fixed gestation controls across `rich`, `poor`, and `harsh` ecologies at 50k steps, then ran a 100k follow-up against fixed `2`. | Supported for real tradeoffs and ecology-dependent gestation regimes. Not yet supported for universal dominance over the best fixed schedule; by 100k, evolvable overtook fixed `2` in `poor` but still trailed it in `rich` and `harsh`. |
