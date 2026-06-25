# Novel Framework

## Overview

Novel Framework is a version-controlled method for developing long-form fiction.

It borrows useful ideas from software development — branches, commits, diffs, review gates, and reversible changes — and adapts them to novel writing.

## Core Files in a Novel Project

Each novel project should include:

- `CANON.md` — accepted story truth
- `DECISION_LOG.md` — record of major creative decisions
- `OPEN_QUESTIONS.md` — unresolved questions
- `STYLE_GUIDE.md` — tone, prose, and aesthetic constraints
- `THEMES.md` — thematic architecture
- `AGENTS.md` — project-specific instructions for AI agents

## Core Directories in a Novel Project

- `CHARACTERS/` — character architecture
- `PLOT/` — timeline, structure, chapter outline, endings
- `WORLD/` — setting, society, place, atmosphere
- `SCIENCE_BIBLE/` or equivalent — technical plausibility, research, systems
- `DRAFT/` — manuscript prose and fragments
- `BRANCHES/` — exploratory non-canon alternatives

## Status Types

### CANON

Accepted story truth.

Canon must be recorded in `CANON.md` and logged in `DECISION_LOG.md`.

### BRANCH

An active alternative or exploratory structure.

Branches can be tested, revised, compared, parked, or merged.

### PARKED

A promising idea that is not currently active and has not been accepted as canon.

## Commands

Useful working commands:

- `commit this` — make an idea canon
- `branch this` — preserve an idea as an exploratory branch
- `show diff` — compare an idea against current canon
- `merge this` — integrate a branch into canon
- `park this` — preserve an idea without activating it
- `revert` — return to an earlier accepted state
- `stress test this` — test weaknesses and contradictions
- `science check this` — test technical plausibility
- `fork three versions` — generate alternate approaches

## Review Gates

Before merging major changes into canon, review them through:

1. Character
2. Theme
3. Structure
4. World
5. Style
6. Plausibility

## Guiding Principle

Exploration should be cheap.

Canon should be deliberate.
