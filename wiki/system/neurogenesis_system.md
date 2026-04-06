# Neurogenesis System

## Observation: Current System Shape

The current Neurogenesis system is a deterministic artificial-life simulation on
a toroidal 2D hex grid. Organisms have explicit energy budgets, aging,
reproduction, and neural controllers whose structure and parameters are encoded
in genomes and can mutate over time.

The simulation already includes several mechanisms that are directly relevant to
the research program:

- ecological pressure through food, terrain, spikes, and optional predation;
- structural evolution through add-synapse, remove-synapse, and split-edge /
  add-neuron mutations;
- runtime plasticity with eligibility traces and a dopamine-like reward signal;
- multi-seed evaluation that scores viability, foraging, control, competition,
  and adaptation rather than only raw reward.

## Observation: Brain And Policy

The controller is a three-layer sensory/inter/action network with leaky
integrator inter-neurons and a single sampled action per tick. The design is
not trying to mimic biology in full detail, but it intentionally imports
biologically inspired priors that may improve evolvability.

## Observation: Ecology And Evolution

The environment is not a passive backdrop. Food regrowth, terrain, hazards,
metabolism, reproduction cost, and periodic seed-genome injection all shape the
search landscape. The project treats these ecological details as part of the
intelligence problem.

## Interpretation

The current system already embodies a strong point of view: cognition is
expected to arise from the interaction of ecology, structural evolution, and
within-lifetime adaptation. This means that changes to world dynamics, mutation
operators, or plasticity rules are not independent tuning knobs. They interact.

## Open Questions

- Are the current sensory channels rich enough to select for memory and
  navigation rather than mostly reactive policies?
- Is the evaluation harness rewarding the right mixture of competencies?
- Which current bottlenecks are due to ecology, which to representation, and
  which to evolutionary search?

## Related Pages

- [../research_program.md](../research_program.md)
- [../concepts/ecological_curriculum.md](../concepts/ecological_curriculum.md)
- [../concepts/runtime_plasticity.md](../concepts/runtime_plasticity.md)
- [../open_problems.md](../open_problems.md)

## Source Traceability

- `../research_statement.md`
- `../../raw/articles/neurogenesis-readme.md`
- `../../raw/articles/neurogenesis-agents.md`
- `../../raw/articles/neurogenesis-autoresearch.md`
