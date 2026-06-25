# Agent Instructions — Novel Framework

This repository contains a reusable framework for developing novels, plus case studies.

## Repository-Level Rule

Do not assume that the repository root is itself a novel project.

Novel projects live inside `case-studies/` unless otherwise specified.

## Working on a Case Study

Before making story decisions inside a case study, read that case study’s:

- `AGENTS.md`
- `CANON.md`
- `DECISION_LOG.md`
- `OPEN_QUESTIONS.md`
- `STYLE_GUIDE.md`
- `THEMES.md`

For the Perth asteroid case study, read:

```text
case-studies/perth-asteroid-novel/AGENTS.md
case-studies/perth-asteroid-novel/CANON.md
case-studies/perth-asteroid-novel/DECISION_LOG.md
case-studies/perth-asteroid-novel/OPEN_QUESTIONS.md
case-studies/perth-asteroid-novel/STYLE_GUIDE.md
case-studies/perth-asteroid-novel/THEMES.md
```

## Canon Rule

Do not change canon unless explicitly instructed to commit or merge.

Canon changes require updates to both:

* the project’s `CANON.md`
* the project’s `DECISION_LOG.md`

## Branch Rule

Files inside a project’s `BRANCHES/` directory are exploratory and non-canon unless explicitly merged.

## Framework Rule

When editing framework-level files, keep them general and reusable.

Do not bake details from a specific case study into the framework unless clearly marked as a case study.
