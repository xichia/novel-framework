# Novel Framework Workflow

A reusable workflow for developing chapters using architecture, probes, packets, and review gates.

---

## Overview

```
Architecture → Prose Probe → Probe Review → Chapter Packet → Packet Review → Acceptance → Draft → Draft Review → Revision
```

Each stage produces a specific artifact. The sequence is designed so that architectural and tonal problems are caught before prose is written, and prose problems are caught before a chapter is considered complete.

This is the standard loop. Not every chapter requires every stage — high-risk chapters (pivots, confessions, revelations) benefit from the full loop; low-risk chapters may compress it.

---

## Stage 1: Architecture

**Purpose:** Define the chapter's structural role, strand distribution, emotional arc, and load before any prose or packet work begins.

**When to use:** Before a chapter packet is written, especially for structurally significant chapters. May be merged with the packet for simpler chapters.

**Inputs:** `CANON.md`, `THEMES.md`, `PLOT/master-timeline.md`, `PLOT/three-strand-structure.md` (or equivalent project files), prior chapter drafts.

**Output artifact:** Architecture artifact in `BRANCHES/` — design decisions, structure distribution, interweaving map, failure modes, downstream consequences.

**Model-role guidance:** Best handled by a model strong at structured long-form reasoning, constraint satisfaction, and holding multiple strands in working memory. This is not a prose role.

**Acceptance gate:** Architecture artifact includes non-canon notice, clearly stated design decisions, and a list of downstream consequences for canon.

**What not to do:** Do not write prose at this stage. Do not commit architecture decisions to canon. Do not skip architecture for structurally pivotal chapters.

---

## Stage 2: Prose Probe

**Purpose:** Test tone, register, and voice for a single dramatic moment before committing to a full chapter draft. A probe is the cheapest way to discover whether an architectural idea works at sentence level.

**When to use:** Before a chapter packet, especially when the tone or register involves a new voice, a high-stakes scene, or an unfamiliar register. Optional for low-risk chapters that reuse an established voice.

**Inputs:** `CANON.md`, `STYLE_GUIDE.md`, `THEMES.md`, relevant architecture artifact. The model must read the project style guide for tone constraints.

**Output artifact:** Prose probe in `BRANCHES/` — 300–1,200 words of prose, self-audit (what worked / what did not work), open questions, and a list of provisional specifics.

**Model-role guidance:** Best handled by a model strong at voice, restraint, sensory grounding, and dialogue economy. Ideally a different model than the one that built the architecture artifact, to reduce self-justification bias.

**Acceptance gate:** Probe has non-canon notice, self-audit is complete, provisional specifics are enumerated. Word count is within limits.

**What not to do:** Do not write a full chapter. Do not introduce canon facts. Do not edit `CANON.md` or `DECISION_LOG.md`. Do not treat probe staging details as requirements.

---

## Stage 3: Probe Review

**Purpose:** Evaluate the prose probe for tone, voice, characterisation, and compliance with the style guide. Identify what the probe proves and what it does not prove, to inform the chapter packet.

**When to use:** After every prose probe. Mandatory before moving to the packet stage.

**Inputs:** The prose probe, `CANON.md`, `STYLE_GUIDE.md`, `THEMES.md`.

**Output artifact:** Probe review in `BRANCHES/` — executive verdict, what the probe proves/does not prove, literary strengths and risks, character/voice assessment, canon-governance risks, keep/change/avoid, final recommendation.

**Model-role guidance:** Best handled by a model strong at critique, register-matching, and restraint enforcement. Must not be the same model that wrote the probe under review.

**Acceptance gate:** Review has verdict, keep/change/avoid sections, canon-governance risks enumerated. No provisional specifics are hardened into canon by this review.

**What not to do:** Do not rewrite the probe. Do not assert canon status for probe details. Do not merge the review's recommendations into canon.

---

## Stage 4: Chapter Packet

**Purpose:** Translate architecture and probe findings into a constrained, actionable blueprint for prose drafting. The packet is the structural boundary between architecture and prose — it tells a drafting model what to write and what to avoid without writing the prose itself.

**When to use:** Before prose drafting for any chapter that carries significant structural or tonal risk. Optional for simple transitional chapters.

**Inputs:** Architecture artifact (if any), probe review (if any), `CANON.md`, `STYLE_GUIDE.md`, `THEMES.md`, `OPEN_QUESTIONS.md`.

**Output artifact:** Chapter packet in `BRANCHES/` — chapter role, required inputs, scene objective, emotional states, revelation payload split into canon-supported and branch-provisional, withheld information, character handling notes, exposition limits, beat map, style constraints, failure modes, drafting checklist, canon-governance notes.

**Model-role guidance:** Best handled by a model strong at structured constraint design and architectural reasoning. The packet writer must understand both the novel's thematic architecture and the practical constraints of prose drafting. A different model than the prose drafter is ideal for separation of concerns.

**Acceptance gate:** Packet clearly separates canon-supported from branch-provisional disclosures. Character handling notes are consistent with canon. Exposition limits are explicit. Failure modes are identified with specific risks and preventions. Canon-governance notes enumerate all provisional elements.

**What not to do:** Do not write prose in the packet. Do not over-prescribe staging details that a prose model could discover organically. Do not harden branch specifics into canon. Do not skip the canon-governance notes section.

---

## Stage 5: Packet Review

**Purpose:** Review the chapter packet for completeness, over-prescription, canon governance, character handling, exposition limits, and failure mode coverage before the packet is accepted as ready for drafting.

**When to use:** After every chapter packet. Mandatory before the acceptance gate.

**Inputs:** The chapter packet, `CANON.md`, `STYLE_GUIDE.md`, `THEMES.md`.

**Output artifact:** Packet review in `BRANCHES/` — executive verdict, what the packet gets right, main risks, canon-governance assessment, over-prescription assessment, character handling assessment, exposition/pacing/genre-risk assessment, missing guidance, recommended revisions, drafting readiness score, final recommendation.

**Model-role guidance:** Best handled by a model strong at structural critique and governance enforcement. Must be a different model than the packet writer.

**Acceptance gate:** Over-prescription assessment is completed. Canon-governance assessment is completed. Recommended revisions are actionable. Drafting readiness score is populated.

**What not to do:** Do not rewrite the packet. Do not add new content to the packet through the review. Do not treat review recommendations as canon unless explicitly merged.

---

## Stage 6: Acceptance

**Purpose:** Confirm that all revisions from the packet review have been addressed and that the packet is ready to guide prose drafting.

**When to use:** After the packet review and any revisions. Typically a single-verdict gate.

**Inputs:** The revised chapter packet, the packet review, any revision notes.

**Output artifact:** Acceptance check in `BRANCHES/` — status notice, resolution check (what was fixed and how), remaining risks, final verdict.

**Model-role guidance:** Best handled by a model strong at verification and completeness checking. This is a narrow gate, not a creative role.

**Acceptance gate:** All required revisions from the packet review are confirmed resolved. Remaining risks are documented. Final verdict is stated.

**What not to do:** Do not introduce new revisions or content at this stage. Do not skip acceptance for structurally significant chapters.

---

## Stage 7: Draft

**Purpose:** Write the chapter prose guided by the accepted packet, respecting the packet's constraints while discovering organic staging details.

**When to use:** After the packet has been accepted as ready for drafting.

**Inputs:** The accepted chapter packet, `CANON.md` (for verification), `STYLE_GUIDE.md` (for tone), `THEMES.md` (for thematic integrity), any relevant probe or probe review.

**Output artifact:** Prose draft in `BRANCHES/` with a non-canon notice header.

**Model-role guidance:** Best handled by a model strong at literary prose, voice consistency, and sensory grounding. Must not be the same model that wrote the packet (to avoid self-justification bias). Must not be the same model that will review the draft.

**Acceptance gate:** Draft carries non-canon notice. Draft respects the packet's constraints (exposition limits, failure mode avoidance, character handling notes). Draft is a complete chapter, not a fragment. No canon facts are added or changed.

**What not to do:** Do not edit `CANON.md` or `DECISION_LOG.md`. Do not treat probe or staging details as requirements. Do not exceed the packet's exposition limits. Do not introduce thriller mechanics or genre-cliché language.

---

## Stage 8: Draft Review

**Purpose:** Evaluate the prose draft for literary quality, character consistency, style-guide compliance, packet compliance, and canon hygiene.

**When to use:** After every prose draft. Mandatory before the draft is considered complete or promoted.

**Inputs:** The prose draft, the chapter packet, `CANON.md`, `STYLE_GUIDE.md`, `THEMES.md`.

**Output artifact:** Draft review in `BRANCHES/` — executive verdict, prose strengths, prose weaknesses, canon hygiene check, method-position check (if applicable), packet compliance check, characterisation check, exposition and pacing check, specific revision recommendations, final recommendation.

**Model-role guidance:** Best handled by a model strong at literary critique, register-matching, and restraint enforcement. Must not be the same model that wrote the draft under review. A third, independent model is ideal.

**Acceptance gate:** Review has a clear verdict (accept / accept with revisions / needs revision). Specific revision recommendations are actionable. Canon hygiene is confirmed.

**What not to do:** Do not rewrite the draft. Do not add new prose. Do not merge review recommendations into canon. Do not treat review observations as binding canon.

---

## Stage 9: Revision

**Purpose:** Revise the prose draft in response to the draft review's recommendations. This is a targeted editing pass, not a rewrite.

**When to use:** After a draft review that recommends revision. May be repeated if the first revision does not resolve all issues.

**Inputs:** The draft review's recommendations, the original draft prose, the chapter packet.

**Output artifact:** Revised prose draft in `BRANCHES/` (new version — v2, v3, etc.).

**Model-role guidance:** Best handled by a model strong at precise, scoped edits. The revision model should be different from the original drafter if possible.

**Acceptance gate:** Revision addresses every actionable recommendation in the review. Revised draft remains within packet constraints. Canon hygiene is preserved.

**What not to do:** Do not rewrite the entire chapter. Do not introduce new content beyond what the revision requires. Do not edit `CANON.md` or `DECISION_LOG.md`. Do not skip the revision review if the original review recommended revision.

---

## Canon Note

None of the artifacts in this workflow are canon unless explicitly merged. Branch artifacts remain exploratory. Prose is not canon — accepted story facts live in `CANON.md`, not in drafts. The workflow is designed to keep exploration cheap and canon deliberate.
