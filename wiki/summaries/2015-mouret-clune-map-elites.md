# Mouret and Clune (2015) - MAP-Elites

## Summary

- Core shift: from optimization to illumination.
- Traditional search asks for the single best solution; MAP-Elites asks what
  high-performing solutions exist across a user-chosen feature space.
- Main mechanism:
- Define behavioral or phenotypic descriptors.
- Partition that space into cells.
- Store the highest-performing individual found in each cell.
- Key result: produces a repertoire of high-quality yet qualitatively distinct
  solutions rather than one champion.
- Important conceptual point: diversity is treated as part of the output, not as
  a side effect or penalty term.
- Scientific value: exposes performance tradeoffs across dimensions the user
  cares about.
- Search benefit: broad archive-based exploration often uncovers stepping stones
  and better overall solutions than narrow optimization.
- Historical significance: foundational quality-diversity algorithm and central
  reference for archive-based behavioral repertoires.

Source: `../../raw/papers/2015-mouret-clune-map-elites.pdf`
