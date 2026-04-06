# Miconi, Stanley, and Clune (2018) - Differentiable Plasticity

## Summary

- Main idea: plasticity itself can be parameterized and trained by gradient
  descent rather than hand-designed.
- Representation: each synapse has both a baseline weight and a plasticity
  coefficient governing how activity updates effective connectivity online.
- Training scheme: backpropagation jointly optimizes fixed weights and
  plasticity parameters.
- Functional consequence: the network can retain stable long-term structure
  while still adapting rapidly within an episode.
- Main demonstration domains:
- Memorization and reconstruction of unseen natural images.
- Omniglot-style few-shot learning.
- Maze-navigation reinforcement learning.
- Strong empirical point: plastic recurrent networks succeed on tasks where
  comparable nonplastic recurrent networks fail.
- Historical significance: key bridge between Hebbian/plasticity ideas from
  neuroscience and scalable modern meta-learning.

Source: `../../raw/papers/2018-miconi-stanley-clune-differentiable-plasticity.pdf`
