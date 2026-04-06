# Wang et al. (2019) - POET

## Summary

- Full name: Paired Open-Ended Trailblazer.
- Main idea: generate new environments and optimize agents for them at the same
  time instead of assuming a fixed benchmark.
- System structure:
- Maintain a population of environment-agent pairs.
- Mutate environments to create new challenges.
- Train or optimize the paired agent for each environment.
- Periodically attempt transfer, letting solutions discovered in one environment
  replace incumbents in others if they work better there.
- Key mechanistic claim: progress often depends on stepping stones discovered in
  other niches rather than direct optimization on the final challenge.
- Demonstration domain: 2-D biped locomotion with increasingly difficult
  obstacle courses.
- Main result: POET finds diverse challenging environments and corresponding
  behaviors that direct optimization alone often fails to reach.
- Historical significance: major reference point for endogenous curriculum
  generation, stepping-stone search, and open-ended machine learning.

Source: `../../raw/papers/2019-wang-et-al-poet.pdf`
