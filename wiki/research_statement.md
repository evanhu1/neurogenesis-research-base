# Research Statement

## 1. Mission

Build an artificial-life system in which cognition can emerge and keep
complexifying through evolution.

More concretely: we want organisms in a simulated world to evolve from simple
reactive policies into agents with memory, internal state, navigation,
competition, and adaptive behavior, without hand-coding those behaviors or
collapsing the task into a trivial benchmark.

## 2. Core questions

- What kinds of environments and ecological pressures actually produce
  progressively richer cognition instead of brittle local optima?
- How should evolutionary curriculum be structured so environmental complexity
  rises with agent capability rather than overwhelming or trivializing search?
- Which inductive biases help most: topology growth, spatial priors,
  excitatory/inhibitory structure, leaky integrator dynamics, or runtime
  plasticity?
- When does within-lifetime learning help evolution discover better genomes, and
  when does it just add noise or instability?
- How should diversity be preserved so the system does not converge to
  degenerate niches or one-action hacks?
- What metrics actually detect meaningful progress toward cognition rather than
  shallow score maximization?
- What mechanisms are necessary for memory, navigation, predation, and
  behavioral adaptation to emerge reliably?

## 3. Hypotheses / beliefs

- Open-ended cognition is more likely to emerge in an ecology than in a
  single-task optimization setting.
- Structural and algorithmic priors from biology can improve evolvability even
  when implemented in a simplified, silicon-friendly way.
- Topology should be allowed to complexify over evolutionary time instead of
  being fixed up front.
- Within-lifetime plasticity is likely important because evolution alone may be
  too slow to discover adaptive behavior in rich environments.
- Diversity preservation matters. Fresh injections, champion carryover, and
  eventually stronger lineage/speciation mechanisms likely help avoid collapse.
- Good progress signals should reward viability, foraging, control, competition,
  and adaptation simultaneously; optimizing only one of these is likely to
  produce pathologies.
- The right curriculum is probably ecological rather than explicitly staged:
  food, hazards, competition, predation, and nonstationarity should create the
  pressure for richer cognition.

## 4. Approach

- Deterministic artificial-life simulation on a toroidal 2D hex grid.
- Large populations of organisms with explicit energy budgets, reproduction,
  aging, death, food ecology, terrain, spikes, and optional predation.
- Neural controllers whose topology and parameters are genetically specified and
  can mutate over time.
- NEAT-style structural mutation operators, plus spatial priors over new
  connections.
- Runtime Hebbian-style plasticity with eligibility traces and a dopamine-like
  reward signal derived from energy change.
- Multi-seed evaluation harness that scores viability, foraging, control,
  competition, and adaptation rather than only raw reward.
- Interactive simulator plus champion-pool persistence so promising lineages can
  be inspected and reused.

## 5. Non-goals

- Hand-authoring behaviors we claim to want evolution to discover.
- Inflating scores by simplifying the world or automating decisions organisms
  are supposed to learn.
- Maximum biological realism at every level. The project borrows useful priors
  from biology but is not trying to be a faithful wet-neuroscience simulator.
- Solving morphology, embodiment, and real-world robotics. The current focus is
  cognition in a simulated 2D world.

## 6. Current bets

- Neuromorphic brain priors help: leaky integrator interneurons,
  excitatory/inhibitory signed weights, sensory/action separation, and
  structured topology.
- Runtime plasticity helps bootstrap behavior within a lifetime and changes what
  evolution can discover across generations.
- Structural evolution matters: add-synapse, remove-synapse, split-edge /
  add-neuron mutations are core rather than peripheral.
- Spatial priors over connectivity are worth keeping because geometry can make
  the search space more learnable.
- Ecology is the curriculum: food distribution, hazards, predation, and energy
  economics are part of the intelligence problem, not just scenery.
- Diversity needs active support: periodic seed-genome injections and champion
  pools are already in the system, and stronger diversity preservation is an
  obvious next lever.
- Reward-reversal and control metrics matter because adaptive cognition should
  survive nonstationarity, not just memorize one policy.

## 7. Open problems

- A real curriculum for cognition: not just harder worlds, but worlds whose
  pressures naturally select for memory, planning, and adaptive internal state.
- Robust diversity preservation. The repo currently tracks lineage diversity,
  but it does not yet have a true speciation / niche-management story in
  `sim-core`.
- Reliable emergence of memory and navigation rather than mostly reactive
  stimulus-response behavior.
- Better evolutionary credit assignment across timescales: immediate reward,
  lifetime learning, and lineage-level selection.
- Ecologies that sustain non-degenerate competition and predation without
  turning into collapse or exploit farming.
- Better measures of cognition and open-endedness than any single aggregate
  score.
- Mechanisms for modularity, hierarchy, and reuse in evolving brains.
- Long-horizon experiment management: how to accumulate discoveries across runs
  without overfitting to one config or one metric bundle.

## Reference Pages

- [research_program.md](research_program.md)
- [open_problems.md](open_problems.md)
- [system/neurogenesis_system.md](system/neurogenesis_system.md)
- [concepts/ecological_curriculum.md](concepts/ecological_curriculum.md)
- [concepts/runtime_plasticity.md](concepts/runtime_plasticity.md)
- [summaries/1991-ray-approach-to-synthesis-of-life.md](summaries/1991-ray-approach-to-synthesis-of-life.md)
- [summaries/1994-sims-evolving-virtual-creatures.md](summaries/1994-sims-evolving-virtual-creatures.md)
- [summaries/2002-stanley-miikkulainen-neat.md](summaries/2002-stanley-miikkulainen-neat.md)
- [summaries/2007-florian-reward-modulated-stdp.md](summaries/2007-florian-reward-modulated-stdp.md)
- [summaries/2008-soltoggio-et-al-neuromodulated-plasticity.md](summaries/2008-soltoggio-et-al-neuromodulated-plasticity.md)
- [summaries/2009-ofria-bryson-wilke-avida.md](summaries/2009-ofria-bryson-wilke-avida.md)
- [summaries/2009-stanley-dambrosio-gauci-hyperneat.md](summaries/2009-stanley-dambrosio-gauci-hyperneat.md)
- [summaries/2011-lehman-stanley-novelty-search.md](summaries/2011-lehman-stanley-novelty-search.md)
- [summaries/2012-coleman-blair-evolving-plastic-neural-networks.md](summaries/2012-coleman-blair-evolving-plastic-neural-networks.md)
- [summaries/2015-mouret-clune-map-elites.md](summaries/2015-mouret-clune-map-elites.md)
- [summaries/2016-taylor-et-al-open-ended-evolution-york.md](summaries/2016-taylor-et-al-open-ended-evolution-york.md)
- [summaries/2017-such-et-al-deep-neuroevolution.md](summaries/2017-such-et-al-deep-neuroevolution.md)
- [summaries/2018-miconi-stanley-clune-differentiable-plasticity.md](summaries/2018-miconi-stanley-clune-differentiable-plasticity.md)
- [summaries/2018-soltoggio-stanley-risi-born-to-learn.md](summaries/2018-soltoggio-stanley-risi-born-to-learn.md)
- [summaries/2019-hintze-open-endedness-for-the-sake.md](summaries/2019-hintze-open-endedness-for-the-sake.md)
- [summaries/2019-taylor-routes-to-open-ended-evolution.md](summaries/2019-taylor-routes-to-open-ended-evolution.md)
- [summaries/2019-wang-et-al-poet.md](summaries/2019-wang-et-al-poet.md)
- [summaries/2020-taylor-importance-of-open-endedness.md](summaries/2020-taylor-importance-of-open-endedness.md)
