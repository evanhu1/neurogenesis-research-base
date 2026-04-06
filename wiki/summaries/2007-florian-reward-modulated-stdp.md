# Florian (2007) - Reinforcement Learning Through Modulation of STDP

## Summary

- Main question: how can local spike-timing-dependent plasticity implement
  reinforcement learning when reward is global and often delayed.
- Core answer: modulate STDP with reward, and use an eligibility trace to store
  a decaying memory of recent pre/post spike relationships.
- Two rule variants studied:
- Direct reward-modulated STDP.
- Reward-modulated STDP with an eligibility trace for delayed credit assignment.
- Main theoretical contribution: derives biologically plausible plasticity rules
  from a reinforcement-learning perspective on stochastic spiking neurons.
- Main mechanistic insight: local timing information can be combined with a
  global scalar reward signal without requiring centralized backprop-style
  credit assignment.
- Experimental demonstrations: XOR with rate-coded and temporally coded inputs,
  plus target firing-rate pattern learning in spiking networks.
- Key importance: influential bridge between synaptic mechanism and behavioral
  reinforcement learning.
- Enduring takeaway: eligibility traces are crucial when the effect of a synapse
  must be credited only after reward arrives later.

Source: `../../raw/papers/2007-florian-reward-modulated-stdp.pdf`
