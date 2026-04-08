# Agent Instructions

This repository is a knowledge base for an ongoing neuroevolution research
project ([NeuroGenesis](https://github.com/evanhu1/NeuroGenesis)). The purpose
of this repo is to support the scientific method and help
the lab do original, novel science research.

## Repository Map

1. The home page for the wiki is `wiki/research_statement.md`
2. Raw sources are stored in `raw/`. These are the source-of-truth materials:
   papers, archived articles, images, and the mirrored Neurogenesis codebase.
3. The wiki under `wiki/`. This is the main synthesized knowledge layer. It is
   LLM-maintained.
4. `log.md` is chronological. It's an append-only record of what happened and
   when — ingests, queries, lint passes, this timeline helps the LLM understand
   what's been done recently. Format: `## [YYYY-MM-DD] operation | short title`
5. `index.md` is a complete catalog of everything in the wiki, each page.

## Principles

Prefer:

- explicit hypotheses over vague intuitions;
- concrete evidence over broad claims;
- clean separation between observations, interpretations, and open questions;
- synthesis that compounds existing knowledge instead of duplicating it;
- explicit notes about contradictions, uncertainty, and missing evidence.

Do not smooth over disagreements between sources. Surface them.

When new material arrives, do not only answer the immediate question. Update the
relevant wiki pages so the synthesis is preserved for future work.

When a useful answer or comparison is produced in conversation, consider filing
it back into the wiki as a new page or as an update to an existing page.

## Three Operations

### 1. Ingest

Use ingest when new source material is added or when the user points to a new
document, article, paper, dataset, image set, or code artifact.

Default ingest workflow:

1. Read the new source carefully.
2. Extract the key observations, claims, methods, and open questions.
3. Decide which existing wiki pages should change.
4. Create or update wiki pages to integrate the new information.
5. Update `wiki/index.md`.
6. Append a chronological entry to `log.md`.

Ingest should usually touch more than one file. A single source may update the
main source summary, a concept page, an experiment page, and a higher-level
synthesis page.

### 2. Query

Use query when the user asks a research question, requests a synthesis, wants a
comparison, or asks for the current state of understanding on some topic.

Default query workflow:

1. Read `wiki/index.md` first.
2. Identify the most relevant wiki pages and read them.
3. Drill down into raw sources only where needed for verification or deeper
   evidence.
4. Answer with citations or explicit source traceability.
5. If the answer creates reusable synthesis, file it back into the wiki and log
   the action in `log.md`.

### 3. Lint

Use lint to health-check and improve the wiki itself.

Look for:

- contradictions between pages;
- stale claims that newer evidence should weaken or replace;
- orphan pages with weak integration into the rest of the wiki;
- important concepts, mechanisms, or experiments that are mentioned but do not
  have their own page;
- missing cross-references;
- places where a new source search would likely be high value.

When running lint, fix what can be fixed directly, record unresolved issues, and
append a `lint` entry to the log.

## Wiki Structure

The wiki should stay organized by topic instead of becoming a flat pile of
notes. Use subdirectories when helpful, for example:

- `wiki/concepts/` for recurring research ideas such as ecological curriculum,
  open-endedness, or diversity preservation;

Create new pages when a concept becomes important enough to deserve a stable
home, not only when explicitly asked.

## Page Conventions

- link to related wiki pages;
- include a `Source` section listing the root docs and raw sources the page
  currently depends on.

## Research-Specific Guidance

This repo is for building a scientific research memory

That means:

- optimize for hypothesis generation and experiment design;
- preserve why a claim matters for the research program;
- track mechanisms, expected causal pathways, and failure modes;
- note what evidence would support or weaken a hypothesis;
- distinguish "the system currently does X" from "we think X may help cognition
  emerge."

Prefer pages that help the lab ask better next questions.

## Editing Discipline

- Do not edit raw sources during routine wiki maintenance.
- Do not collapse nuanced uncertainty into confident summary.
- Do not create duplicate pages when updating an existing one would be cleaner.
- Keep cross-links current when pages are added or renamed.
- When new evidence contradicts an existing page, update the page instead of
  letting both versions silently coexist.
