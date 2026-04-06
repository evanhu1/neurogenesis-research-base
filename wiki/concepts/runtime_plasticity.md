# Runtime Plasticity

## Observation: What The System Currently Does

The current system implements runtime Hebbian-style plasticity with eligibility
traces and a dopamine-like reward signal derived from energy change. Mature
organisms learn with `hebb_eta_gain`, juveniles can learn earlier through a
scaled pathway, and per-tick updates are clamped.

## Why It Matters

Runtime plasticity is one of the project's most important bets because it may
change what evolution can discover. If useful behavior can be partly assembled
within a lifetime, evolution may only need to find genomes that make adaptive
learning possible, rather than genomes that directly encode the full behavior.

## Interpretation

Plasticity may matter in at least three ways:

- it can bootstrap competence inside a single lifetime;
- it can smooth the evolutionary search landscape by rewarding learnable
  structures;
- it may interact with ecology by making nonstationary environments more
  tractable.

The risk is that plasticity also adds noise, instability, or hard-to-interpret
credit assignment across timescales.

## Open Questions

- Under what ecologies does plasticity help versus hurt?
- Are current reward-signal and eligibility settings aligned with the behaviors
  the lab wants to emerge?
- How much of any observed gain is true adaptation versus a measurement or
  accounting artifact?

## Related Pages

- [../research_program.md](../research_program.md)
- [ecological_curriculum.md](ecological_curriculum.md)
- [../system/neurogenesis_system.md](../system/neurogenesis_system.md)
- [../open_problems.md](../open_problems.md)

## Source Traceability

- `../research_statement.md`
- `../../raw/articles/neurogenesis-readme.md`
- `../../raw/articles/neurogenesis-agents.md`
- `../../raw/papers/2007-florian-reward-modulated-stdp.pdf`
- `../../raw/papers/2008-soltoggio-et-al-neuromodulated-plasticity.pdf`
- `../../raw/papers/2018-soltoggio-stanley-risi-born-to-learn.pdf`
