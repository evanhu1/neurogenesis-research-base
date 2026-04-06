# Such et al. (2017) - Deep Neuroevolution

## Summary

- Main question: can traditional gradient-free genetic algorithms train very
  large deep neural networks competitively on hard RL tasks.
- Core answer: yes; a simple population-based GA can scale to networks with
  millions of parameters.
- Benchmarks emphasized: Atari and humanoid locomotion.
- Headline results:
- Strong competitiveness against prominent deep RL and evolution-strategy
  baselines.
- Very large evolved networks by the standards of traditional evolutionary
  algorithms.
- Good wall-clock efficiency due to easy parallelization.
- Conceptual contribution: challenges the assumption that large deep networks
  require gradient-following optimization.
- Broader significance: reopens the case for neuroevolution as a serious
  large-scale machine-learning method and connects deep RL to the wider toolbox
  of novelty search and compact encodings.

Source: `../../raw/papers/2017-such-et-al-deep-neuroevolution.pdf`
