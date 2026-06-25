# Agent Instructions

This is a literary novel project managed like a Git repository.

## Primary Rule

Do not change canon unless explicitly instructed.

Canon lives in `CANON.md`.

## Required Reading

Before making any story decision, read:

1. `CANON.md`
2. `DECISION_LOG.md`
3. `OPEN_QUESTIONS.md`
4. `STYLE_GUIDE.md`

## Workflow

For any major story decision:

1. Identify whether the request is canon work, branch exploration, stress testing, research, or drafting.
2. If exploring, create or update a branch file in `BRANCHES/`.
3. If committing, update `CANON.md` and `DECISION_LOG.md` together.
4. Never silently overwrite existing decisions.
5. Always report downstream consequences.

## Tone

Literary fiction.

Restrained, morally complex, class-conscious, scientifically credible, emotionally precise.

## Avoid

- conspiracy-thriller clichés
- villain monologues
- easy moral answers
- hand-waved asteroid science
- sentimental treatment of Martin's former partner
- making the elder manipulative
- making Martin purely heroic
- vague utopia

## Prefer

- concrete domestic detail
- Perth atmosphere
- class texture
- institutional realism
- scientific plausibility
- moral ambiguity
- warmth against cold
- private life echoing public crisis

## Operating Commands

| Command | Action |
|---|---|
| `commit this` | Make the current idea canon. Update CANON.md and DECISION_LOG.md. |
| `branch this` | Explore without accepting. Create a branch file. Do not alter canon. |
| `show diff` | Compare proposed change against current canon. |
| `merge this` | Accept a branch into canon. Update canon and decision log. |
| `park this` | Save the idea for later. Add to BRANCHES/parked-ideas.md. |
| `revert` | Undo a canon decision. Restore previous state. Record the revert. |
| `stress test this` | Attack the idea. Check plausibility, character, theme, science, cliché risk. |
| `science check this` | Assess factual plausibility of asteroid science and institutional mechanics. |
| `fork three versions` | Generate three viable alternatives with gains, risks, and a recommendation. |
