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

## 7. Canon

Project and field-defining source materials:

- `Neurogenesis` repo itself, especially the README, AGENTS notes, config, and
  evaluation harness.
- Neuroevolution overview material such as the Wikipedia neuroevolution page.

Foundational neuroevolution and indirect-encoding papers:

- Stanley and Miikkulainen (2002), _Evolving Neural Networks through Augmenting
  Topologies_.
- Stanley, D'Ambrosio, and Gauci (2009), _A Hypercube-Based Encoding for
  Evolving Large-Scale Neural Networks_.
- Such et al. (2018), _Deep Neuroevolution: Genetic Algorithms Are a Competitive
  Alternative for Training Deep Neural Networks for Reinforcement Learning_.

Diversity, exploration, and open-ended search:

- Lehman and Stanley (2011), _Abandoning Objectives: Evolution Through the
  Search for Novelty Alone_.
- Mouret and Clune (2015), _Illuminating Search Spaces by Mapping Elites_.
- Wang et al. (2019), _Paired Open-Ended Trailblazer (POET)_.

Artificial life and open-ended evolution:

- Ray (1991/1992), _An Approach to the Synthesis of Life_.
- Ofria, Bryson, and Wilke (2009), _Avida: A Software Platform for Research in
  Computational Evolutionary Biology_.
- Taylor et al. (2016), _Open-Ended Evolution: Perspectives from the OEE
  Workshop in York_.
- Taylor (2019), _Evolutionary Innovations and Where to Find Them: Routes to
  Open-Ended Evolution in Natural and Artificial Systems_.
- Hintze (2019), _Open-Endedness for the Sake of Open-Endedness_.
- Taylor (2020), _The Importance of Open-Endedness (for the Sake of
  Open-Endedness)_.

Plasticity, neuromodulation, and lifetime learning:

- Florian (2007), _Reinforcement Learning Through Modulation of Spike-Timing-
  Dependent Synaptic Plasticity_.
- Soltoggio and Bullinaria (2008), _Evolutionary Advantages of Neuromodulated
  Plasticity_.
- Coleman and Blair (2012), _Evolving Plastic Neural Networks for Online
  Learning: Review and Future Directions_.
- Soltoggio, Stanley, and Risi (2018), _Born to Learn: The Inspiration,
  Progress, and Future of Evolved Plastic Artificial Neural Networks_.
- Miconi, Stanley, and Clune (2018), _Differentiable Plasticity_.

Embodied evolution / artificial creatures:

- Sims (1994), _Evolving Virtual Creatures_.

## 8. Open problems

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
