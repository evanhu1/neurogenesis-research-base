# Stanley and Miikkulainen (2002) - Evolving Neural Networks through Augmenting Topologies

## Summary

- Main problem: how to evolve both neural-network weights and topology without
  crossover and selection breaking down as structures diverge.
- Core proposal: NEAT, a method that starts from minimal networks and gradually
  complexifies them through structural mutation.
- Three defining components:
- Historical markings align genes across different topologies during crossover.
- Speciation protects new structural innovations from immediate competition with
  already-optimized lineages.
- Incremental complexification keeps the initial search space small and adds
  complexity only when useful.
- Main empirical support: ablation studies show each of the three components
  materially contributes to performance.
- Benchmark emphasis: reinforcement-learning control tasks, especially
  pole-balancing.
- Conceptual importance: demonstrates that evolution can optimize and
  complexify simultaneously rather than requiring topology to be fixed in
  advance.
- Historical significance: became the canonical direct-encoding neuroevolution
  method for evolving structure plus parameters.

Source: `../../raw/papers/2002-stanley-miikkulainen-neat.pdf`
