# Evolvable Gestation

## Status

Implemented and evaluated.

## Question

Does an evolvable gestation duration increase the reachable range of viable
life-history strategies relative to fixed reproduction schedules?

## Mechanism

- `gestation_ticks` is evolvable in the range `[0, 4]`.
- Offspring transfer energy is `100 + 100 * gestation_ticks`.
- Gestation is non-interruptible once reproduction starts.
- If the birth target is blocked when gestation completes, the birth attempt is
  a no-op.
- The parent pays the transfer cost directly, so higher gestation increases
  offspring starting energy but also delays future births and increases failure
  risk during gestation.

## Ecologies

Three ecologies were evaluated with the same seed genome and mutation settings.

- `rich`: higher food energy, faster regrowth, lower spike density
- `poor`: lower food energy, slower regrowth
- `harsh`: lower food energy, slower regrowth, higher spike density

## Evaluation Design

Two comparison rounds were run.

1. A 50k-step matrix comparing evolvable gestation against fixed gestation
   controls `0`, `2`, and `4` in each ecology.
2. A 100k-step follow-up comparing evolvable gestation only against fixed
   gestation `2` in each ecology.

All runs used seeds `42,123,7,2026,99`.

## Main Readouts

- aggregate evaluation score
- mean gestation among living organisms
- successful births by gestation bin
- adult population by gestation bin
- survival to age 30 by birth gestation bin
- blocked births by gestation bin
- parent death during gestation by gestation bin
- mean parent energy immediately after successful birth
- mean successful birth interval

## 50k Results

Aggregate-score differences below are treatment minus evolvable control.

| Ecology | Fixed 0 | Fixed 2 | Fixed 4 |
| --- | ---: | ---: | ---: |
| rich | -2.96 | +1.48 | -3.47 |
| poor | +2.27 | +3.12 | -5.53 |
| harsh | +3.59 | +6.09 | +2.38 |

Observations:

- The mechanism produced a real tradeoff. Fixed `4` was harmful in `rich` and
  `poor`, and only modestly better than evolvable in `harsh`.
- The favored gestation regime depended on ecology. The evolvable control mean
  gestation was about `0.23` in `rich`, `0.64` in `poor`, and `1.09` in
  `harsh`.
- Fixed `2` was the strongest fixed treatment in all three ecologies at 50k.
- Evolvable populations did not collapse to a single universal gestation value;
  they maintained mixed birth distributions with more high-investment births in
  harsher ecologies.

## 100k Follow-Up: Evolvable vs Fixed 2

Aggregate-score differences below are fixed `2` minus evolvable control.

| Ecology | Evolvable | Fixed 2 | Diff |
| --- | ---: | ---: | ---: |
| rich | 61.64 | 64.20 | +2.56 |
| poor | 61.07 | 60.10 | -0.97 |
| harsh | 53.41 | 54.83 | +1.42 |

Associated mean gestation values:

| Ecology | Evolvable Mean Gestation | Fixed 2 Mean Gestation |
| --- | ---: | ---: |
| rich | 0.240 | 0.234 |
| poor | 0.613 | 0.668 |
| harsh | 1.006 | 1.002 |

Observations:

- In `rich`, the longer horizon strengthened the fixed `2` advantage.
- In `poor`, the 50k fixed `2` advantage reversed by 100k, with evolvable
  slightly ahead.
- In `harsh`, the large 50k fixed `2` advantage shrank substantially by 100k.
- By 100k, evolvable and fixed `2` had converged to very similar mean
  gestation regimes in all three ecologies.

## Interpretation

The experiment supports two claims.

1. Gestation introduced a real life-history tradeoff rather than a monotone
   improvement.
2. Different ecologies favored different parental-investment regimes.

The stronger claim that evolvable gestation consistently outperforms the best
fixed schedule is not supported. At 50k, fixed `2` was best in all ecologies.
At 100k, that conclusion weakened: fixed `2` remained better in `rich` and
`harsh`, but evolvable slightly overtook it in `poor`.

The 100k follow-up suggests that evolvable gestation needs longer horizons to
approach ecology-specific intermediate optima. The remaining gap in `rich` and
`harsh` may reflect slower adaptive convergence rather than a failure to
discover the relevant phenotype class.

## Conclusion

Evolvable gestation changed the search landscape in a meaningful way. It did
not merely select one globally optimal gestation value. Instead, the favored
investment regime shifted with ecology, and the evolvable populations moved in
that direction over longer horizons.

The best-supported conclusion is:

- evolvable gestation creates real parental-investment tradeoffs;
- ecology changes which gestation regimes are viable;
- longer runs improve the competitive position of evolvable gestation relative
  to the strongest fixed control, but do not yet show universal dominance.

## Follow-Up Questions

- Does the evolvable treatment overtake fixed `2` in `rich` or `harsh` at even
  longer horizons?
- Does reducing blocked-birth frequency change the relative advantage of higher
  gestation bins?
- Are there curriculum or ecology schedules that accelerate convergence toward
  the ecology-specific gestation optimum?

## Source Traceability

- `../../raw/neurogenesis/eval_runs/gestation_ecologies_50k/*/summary.json`
- `../../raw/neurogenesis/eval_runs/gestation_fixed2_vs_evolvable_100k/*/summary.json`
- `../../raw/neurogenesis/sim-evaluation/ecologies/*/config.toml`
- `../../raw/neurogenesis/sim-types/src/lib.rs`
- `../../raw/neurogenesis/sim-core/src/turn/reproduction.rs`
- `../../raw/neurogenesis/sim-evaluation/src/ledger.rs`
