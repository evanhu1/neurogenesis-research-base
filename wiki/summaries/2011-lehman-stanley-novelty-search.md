# Lehman and Stanley (2011) - Abandoning Objectives: Evolution Through the Search for Novelty Alone

## Summary

- Core argument: objective functions can be deceptive, so search should
  sometimes reward behavioral novelty instead of progress toward a predefined
  target.
- Main proposal: novelty search, which scores individuals by how behaviorally
  different they are from previously encountered behaviors.
- Mechanism:
- Define a behavior characterization.
- Compute novelty as sparseness in behavior space relative to neighbors in the
  population and archive.
- Add sufficiently novel individuals to an archive to preserve exploration
  history.
- Main empirical result: novelty search outperforms objective-driven evolution
  in deceptive maze navigation.
- Additional strong result: novelty search also performs well in difficult 3D
  biped locomotion where objective-based search often gets trapped in poor local
  optima.
- Conceptual contribution: reorients evolutionary computation around
  open-ended exploration rather than direct objective maximization.
- Historical significance: foundational paper for later quality-diversity,
  open-ended search, and behavioral-repertoire methods.

Source: `../../raw/papers/2011-lehman-stanley-novelty-search.pdf`
