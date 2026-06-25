# Novel Framework

A Git-style framework for developing novels with canon, branches, decision logs, agent skills, and reversible story architecture.

## Purpose

Novel Framework treats long-form fiction development like a version-controlled creative project.

It is designed to help writers:

- separate accepted canon from exploratory branches
- preserve major creative decisions
- test alternate plot structures without losing earlier work
- use AI agents safely without accidental canon drift
- manage worldbuilding, character development, plot architecture, and drafting as distinct layers

## Core Idea

A novel project should be able to branch, test, merge, park, and revert ideas without losing the emotional and thematic integrity of the work.

## Repository Structure

- `FRAMEWORK.md` — the reusable method
- `AGENTS.md` — repo-level agent instructions
- `.agents/skills/` — reusable agent skills
- `templates/` — future reusable project templates
- `case-studies/` — case studies

## Current Case Study

The first case study is `case-studies/perth-asteroid-novel/`.

It is a literary novel project about a post-crisis utopia built on a lie. A secret elite group fabricates an asteroid impact threat, forcing humanity into cooperation. The crisis is false, but the better world it produces is real.

The case study demonstrates how Novel Framework manages:

- canon versus exploratory branches
- character architecture
- moral and thematic questions
- science plausibility
- three-strand plot structure
- reversible plot decisions
- AI-assisted development without accidental canon drift

## Canon Rule

Nothing becomes canon inside a novel project unless it is added to that project’s `CANON.md` and recorded in that project’s `DECISION_LOG.md`.

## Status

Early experimental framework.

## License

This repository uses a split license.

Reusable framework/tooling materials are licensed under the MIT License.

Original fiction, story worlds, character materials, draft prose, plot outlines, chapter text, and case-study narrative content are All Rights Reserved unless a file explicitly states otherwise.

See [LICENSE](LICENSE) for details.
