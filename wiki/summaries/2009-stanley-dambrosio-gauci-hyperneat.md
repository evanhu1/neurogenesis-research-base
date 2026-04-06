# Stanley, D'Ambrosio, and Gauci (2009) - HyperNEAT

## Summary

- Main problem: direct encodings scale poorly when every network connection must
  be represented independently.
- Core proposal: HyperNEAT, an indirect encoding method that evolves a CPPN
  which maps geometry to connectivity.
- Representation: neuron coordinates are input to a compositional
  pattern-producing network; its outputs define connection weights.
- Central insight: many useful large neural networks exhibit symmetry,
  repetition, and spatial regularity, so connectivity should be generated as a
  pattern rather than listed edge by edge.
- Main advantages:
- Compact representation of large structured networks.
- Natural exploitation of task geometry.
- Ability to query the same generative pattern at different resolutions.
- Demonstrated domains: visual discrimination and food-gathering tasks,
  including networks with millions of connections.
- Historical significance: extends NEAT from topology growth into powerful
  generative encoding and becomes a central reference for geometry-aware
  neuroevolution.

Source: `../../raw/papers/2009-stanley-dambrosio-gauci-hyperneat.pdf`
