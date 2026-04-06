# Karl Sims (1994) - Evolving Virtual Creatures

## Summary

- Main contribution: evolves both morphology and control for virtual creatures in
  simulated 3D physics worlds instead of assuming a fixed body plan.
- Representation: graph-based genetic encoding that can generate articulated
  bodies, joints, muscles, and neural controllers.
- Selection setup: different fitness functions reward behaviors such as
  swimming, walking, jumping, and following.
- Key technical idea: compositional encoding allows repetition, hierarchy, and
  coordinated structure rather than flat parameter search.
- Why the representation matters: body and controller can co-adapt, producing
  solutions that fit each other instead of being optimized independently.
- Physics-grounded search: evolved behavior is constrained by inertia, force,
  torque, contact, and environmental dynamics rather than abstract scoring
  alone.
- Typical outcome: locomotion strategies are often surprising, non-intuitive,
  and difficult to hand-design directly.
- Broader message: evolutionary search can be used as a generator of complex
  design, not just as a tuner of known architectures.
- Historical significance: landmark demonstration that embodied adaptive
  structure can emerge when representation, environment, and selection are well
  matched.

Source: `../../raw/papers/1994-sims-evolving-virtual-creatures.pdf`
