# Repository Quality Audit — GLM 5.2 Pass v1

## Audit Status

This is a read-only audit. It does not modify any existing project files, does not edit `CANON.md`, does not edit `DECISION_LOG.md`, does not touch branch artifacts, does not commit any case-study detail to canon, and does not create any temporary scripts. The only file created by this pass is this audit document itself, placed at the repository root as instructed. All findings below are observations and recommendations; no fixes are applied in this pass.

## Repository State

Current branch: `main`. Working tree: clean. The local branch is 9 commits ahead of `origin/main`.

Recent commits (latest first) trace a clear, disciplined loop: add chapter 17 packet → review packet → revise packet → accept packet → position science as character → review that position → adopt science as character guidance → draft chapter 17 → review draft → revise draft. This loop is the strongest signal of a healthy workflow, but it is currently visible only in commit messages and in the case-study `BRANCHES/` directory. It is not yet captured in generalized framework documentation.

The repository contains 52 tracked files (excluding the `.git` directory). Framework-level files are thin: `FRAMEWORK.md` (76 lines), `AGENTS.md` (50 lines), `README.md` (61 lines), `templates/README.md` (14 lines, effectively a placeholder), `case-studies/README.md` (9 lines), and five one-line skill stubs under `.agents/skills/`. The Perth case study is substantially deeper: 19 files in canonical/structural directories plus 17 branch artifacts.

## Executive Verdict

**Verdict: Mixed; case study stronger than reusable framework.**

The Perth asteroid novel case study is the most fully developed and rigorously governed part of this repository. Its canon is dense, internally consistent, and cleanly separated from exploratory material. Its decision log captures both creative direction and governance boundaries — Entry 014 explicitly marks a style/method decision as non-canon. Its style guide is one of the strongest files in the repo: a genuine tone contract with concrete right/wrong examples. Its Chapter 17 workflow has produced a closed review loop (probe → probe review → packet → packet review → acceptance check → draft → draft review → revision) that protects the literary register from thriller collapse, info-dump failure, and melodrama.

The reusable framework, by contrast, is correct in spirit but underbuilt in practice. `FRAMEWORK.md` describes the method at a high altitude — core files, status types, commands, review gates — but stops short of templates, checklists, or step-by-step workflows. `templates/README.md` is effectively a wish list: eight planned templates, none of which exist. The five skills under `.agents/skills/` are one-line stubs whose front-matter descriptions are richer than their bodies. The repo-level `AGENTS.md` states the can/branch/framework rules but does not encode the workflow the Perth case study has actually proven.

The case study has, in effect, been doing R&D for the framework. Every pain it has solved — how to stop a probe hardening into canon, how to mark technical specifics as provisional, how to gate a draft on a packet, how to record an acceptance check — is a lesson that belongs in a general form. The irony is that the framework is now underweight because it has been too disciplined about not absorbing case-study lessons.

The governance posture is sound but unevenly enforced. The can/branch distinction is stated in three places (root `AGENTS.md`, case `AGENTS.md`, `FRAMEWORK.md`) but the actual mechanism — canon requires both `CANON.md` and `DECISION_LOG.md` — is repeated as prose rather than encoded as a runnable checklist. There is no acceptance-gate artifact in the framework at all. The Perth case study improvised one (`chapter-17-packet-v2-acceptance-check.md`), which is excellent but case-specific and ad hoc.

This is not a repo in trouble. It is a repo whose case study has outpaced its framework, and which now needs a consolidation pass to lift proven patterns into reusable form before more case studies or chapters accumulate. The risk of inaction is that the next model working here will reinvent the Perth workflow badly, or harden a branch detail into canon because no checklist told it not to.

## What Is Working Well

**Canon governance, in the case study.** `CANON.md` is dense, opinionated, and unambiguous about premise, characters, setting, structure, science principle, ending direction, and final image. `DECISION_LOG.md` records 14 numbered entries with reason, alternatives considered, downstream consequences, and status. Entry 014 is a model of governance literacy: it explicitly states that a style/method decision does not alter `CANON.md`. The two files clearly co-govern canon.

**Branch discipline.** Every branch artifact in `case-studies/perth-asteroid-novel/BRANCHES/` self-declares as non-canon. The packet files (`chapter-17-packet-v1.md`, `chapter-17-packet-v2.md`) include explicit "Branch Status" notices and a "Canon-Governance Notes" section that enumerates provisional specifics (asteroid designation `2031 AG3`, the 1-in-412 to 1-in-19 probability, the 14-day window, the document case). Reviews (`prose-probe-confession-review-v1.md`, `chapter-17-draft-review-v1.md`) repeat the canon-hygiene confirmation. This is unusually clean.

**Milestone progression.** The case study has moved through recognizable milestones — canon foundation (v0.1), naming (v0.2), style/method correction (v0.3), plot architecture, and now chapter drafting — without skipping steps or backsliding. `PROJECT_MANIFEST.md` and `README.md` are slightly stale on the current milestone (both still point at "Milestone 3: Plot Architecture" and the plot-architecture branch, while the actual work has advanced to Chapter 17 drafting), but the underlying trajectory is healthy.

**Case-study depth.** The Perth case study has a coherent world (`WORLD/`), a credible science bible (`SCIENCE_BIBLE/`), a three-strand structure with strand registers, a thematic architecture that explicitly refuses to answer its own question, and a style guide with concrete right/wrong prose examples. Few novel projects, human or AI-assisted, hold this much architectural weight without leaking.

**Review loops.** The Perth workflow has produced genuine closed-loop reviews: prose probe reviewed, packet reviewed, packet acceptance-checked, draft reviewed, draft revised. The reviews are specific, actionable, and structurally bounded (verdict, strengths, weaknesses, canon hygiene check, science-as-character check, packet compliance, recommendations). This is the pattern the framework should be generalizing.

**Acceptance gates, in vitro.** `chapter-17-packet-v2-acceptance-check.md` is a small but real acceptance-gate artifact: status notice, resolution check, remaining risks, final verdict. It proves the repo already understands what an acceptance gate is, even though the framework does not yet name or ship one.

**Prose/architecture separation.** The distinction between packet (architecture) and draft (prose) is clean. The packet explicitly says it "does not replace the act of drafting." The draft holds the packet's constraints loosely — see the v2 packet section "Prose Discoveries from the Probe (Optional Staging Guides)," which demotes probe staging details (wine glass, Mundijong oranges, the final "No") from requirements to optional discoveries. This is sophisticated revision discipline.

## Main Risks

**Branch artifacts hardening into canon.** The strongest protection today is convention and the goodwill of careful models. The packet files enumerate provisional specifics, but nothing programmatically stops a future model from writing a draft, then a downstream chapter, then a canon update that silently promotes `2031 AG3` or the 1-in-19 figure into canon. There is no checklist a model must pass before touching `CANON.md`.

**Overaccumulation of planning artifacts.** The Perth `BRANCHES/` directory already holds 17 files and is growing one or two per chapter cycle. Without a naming convention, a versioning convention, or a parking/archive rule, this directory will become unnavigable. The current naming (mixed `chapter-17-packet-v1.md`, `science-as-character-position-v1.md`, `confession-pressure-decision-stress-test-v1.md`) is descriptive but inconsistent in style andgranularity.

**Missing reusable templates.** The `templates/` directory is a placeholder. Every artifact the Perth case study has proven useful — prose probe, probe review, packet, packet review, acceptance check, draft, draft review — has no general form. New case studies would have to reverse-engineer Perth to discover them.

**Future model confusion.** A fresh model entering this repo gets: a 50-line root `AGENTS.md`, a 76-line `FRAMEWORK.md`, five one-line skill stubs, and a placeholder `templates/README.md`. It is told to read the case study's six files before acting, but it is not told what the working loop is, what an acceptance gate is, or how to route itself between architecture, science, prose, review, and cleanup tasks. The case-study `AGENTS.md` is more helpful than the framework, which inverts the intended direction of dependence.

**Overly case-specific guidance leaking into framework.** This risk is currently well controlled — the framework is thin partly because it has refused to absorb case detail. But the opposite risk is now live: the framework is so thin that the only working example of the method is a single case study, so any model trying to generalize will be tempted to copy Perth wholesale.

**Unclear next-step rules.** Nothing in the framework says what comes after a packet acceptance, after a draft review, or after a chapter is "done." The Perth case study has implicitly chosen "next chapter," but that is not written down as a rule.

**Poor discoverability for new contributors or models.** There is no top-level index of artifacts, no "how to start a new case study" guide, and no mapping from skill names to actual responsibilities. A new contributor's fastest path to understanding the repo is to read Perth's `BRANCHES/` in commit order, which is not documented anywhere as the recommended path.

## Reusable Framework Assessment

**Strong framework components:**

- `FRAMEWORK.md` gives a clean conceptual skeleton: core files, core directories, status types (CANON / BRANCH / PARKED), commands, and review gates. The "Exploration should be cheap. Canon should be deliberate." principle is a strong, portable governancemotto.
- `AGENTS.md` correctly separates repository-level rules (root is not a novel project; novel projects live in `case-studies/`) from case-level rules and states the canon and branch rules crisply.
- The split license (MIT for framework/tooling, All Rights Reserved for fiction) is well thought out and clearly stated in `README.md` and `LICENSE`.
- The skill taxonomy (`canon-maintainer`, `continuity-editor`, `literary-style-editor`, `plot-architect`, `science-checker`) is the right set of role labels for a novel project.

**Missing or underdeveloped framework components:**

- `templates/` is a placeholder with no actual templates.
- The five skills are one-line stubs. Their front-matter `description` is useful for routing but their bodies carry no instructions, no triggers, no outputs, no failure modes.
- There is no workflow document that names the loop the Perth case study has proven: architecture → probe → probe review → packet → packet review → acceptance → draft → draft review → revision.
- There is no acceptance-gate checklist in the framework.
- There is no model-routing guidance. The skills imply roles but do not state which model type fits which role.
- There is no canon-governance checklist a model can run before being allowed to touch `CANON.md` or `DECISION_LOG.md`.
- There is no "start a new novel project" guide.

**Lessons from the Perth case study that should be generalized:**

- The architecture / prose probe / packet / review loop. This is the single most valuable reusable pattern in the repo.
- The "provisional specifics" convention: branch files enumerate which details are provisional and must not harden into canon without ratification.
- The "optional discoveries" convention: a probe or draft yields staging details that later packets demote from requirements to optional references — a reusable revision discipline.
- The branch self-declaration pattern: every branch file opens with a status notice and a canon-governance note.
- The acceptance-check and review formats (status → resolution → remaining risks → verdict; verdict → strengths → weaknesses → canon hygiene → compliance → keep/change/avoid).
- The decision-log entry format, including Entry 014's explicit governance line distinguishing canon from guidance.

**What should not be generalized because it is too case-specific:**

- Any specific Perth content: Martin, Bianca, Giacob, the asteroid, the tram lines, the loquats, the document case, the 1-in-19 probability, `2031 AG3`, the three-strand structure, the seasonal architecture, the "Warm Room" title. These belong to the case study.
- The "Science as Character" style position. It is a strong method correction, but it was adopted as project-specific guidance in `DECISION_LOG.md` Entry 014, explicitly marked as non-canon and as a style/method decision. It should not be lifted into the framework verbatim; at most, the framework could generalize the meta-pattern ("a project may adopt a style/method position note that corrects a misread of the style guide, recorded in the decision log as guidance, not canon").
- The three-strand braided structure. Useful for Perth; not a universal novel shape.
- The specific reviewer checklist items (e.g., "Giacob should not weep," "evidence package must not be a MacGuffin"). These are case-specific failure modes.

## Perth Case Study Assessment

**Is the case-study documentation coherent?**

Yes, strongly. `CANON.md`, `THEMES.md`, `STYLE_GUIDE.md`, `OPEN_QUESTIONS.md`, `PLOT/three-strand-structure.md`, the character files, the world files, and the science bible are mutually consistent and cross-reference each other. The style guide's "Strand Registers" section is explicitly aligned with the three-strand structure in canon. The themes file's "What the Novel Is Not Arguing" section protects the ambiguity that canon mandates. The open questions file carries status, options, notes, and downstream impact per question — a quality level most novel projects never reach.

One minor incoherence: `OPEN_QUESTIONS.md` still lists `OQ-001` and `OQ-002` with "Status: Active — ready to decide"lines, even though both were closed by `DECISION_LOG.md` Entry 013 (Giacob, Bianca). `OQ-001`'s header says "✓ CLOSED" but its body still says "Active — ready to decide." `OQ-002` has no closure marker at all. This is a small stale-state leak, not a canon violation, and is a safe fix for a later implementation pass.

**Are `CANON.md` and `DECISION_LOG.md` being protected properly?**

Yes, in the observed commits. The branch files, reviews, drafts, and packets all explicitly disclaim canon authority. No commit in the recent history modifies canon accidentally. Entry 014 of the decision log is a particularly good example of governance hygiene: a style/method change is recorded as a decision but explicitly marked "Approved Guidance," not canon, with a "Governance" line stating it does not alter `CANON.md`. This is exactly the right discipline for non-story decisions that still need a paper trail.

**Are branch artifacts useful and clearly non-canon?**

Yes. The 17 branch files fall into a small number of clear types: position notes (`science-as-character-position-v1.md`), stress tests (`confession-pressure-decision-stress-test-v1.md`) and their reviews, plot architecture (`plot-architecture-v1.md`, `interweaving-map-v1.md`, `revelation-rhythm-v1.md`), prose probes (`prose-probe-confession-v1.md`) and their reviews, chapter packets and their reviews/acceptance checks, chapter drafts and their reviews, and a parking lot (`parked-ideas.md`). All carry non-canon notices. They are genuinely useful — the prose probe taught the packet; the packet taught the draft; the draft review drove the v2 revision.

**Is the Chapter 17 workflow becoming too overbuilt, or is the architecture/prose/review sequence justified?**

The sequence is justified, not overbuilt. Chapter 17 is the structural pivot of the novel — the confession scene that transfers the central burden from Giacob to Martin. It carries maximal load: genre collapse risk, info-dump risk, melodrama risk, canon-hardening risk, and the entire "science as character" tension. The four-stage loop (probe → packet → draft → review, with reviews at each stage) is proportionate to that load. The v2 packet's demotion of probe staging details to "optional discoveries" is the clearest evidence that the loop is not overbuilt: it is actively pruning its own earlier assumptions.

The one place to watch for overbuilding is the `BRANCHES/` directory's growth. If every chapter accumulates 4–6 branch artifacts, the directory will reach 100+ files before the novel is done. A chapter-scoped subdirectory convention (e.g., `BRANCHES/chapter-17/`) would help but is a medium-risk refactor, not an immediate one.

**What should happen next in the case study?**

The v2 draft is the current head. The natural next step is a v2 draft review (analogous to `chapter-17-draft-review-v1.md` but evaluating the v2 draft against the v1 review's revision recommendations), followed by either a v3 draft or an acceptance of the v2 draft as the canon-eligible Chapter 17 prose (where "canon-eligible" still means prose, not story facts — prose drafts are not canon in this project's governance model). After Chapter 17 is settled, the case study should move to Chapter 18 (Strand C, the conspiracy working) or whichever chapter the interweaving map dictates next.

## Canon-Governance Assessment

The repo states the canon rule in three places: root `AGENTS.md` ("Do not change canon unless explicitly instructed"; canon changes require both `CANON.md` and `DECISION_LOG.md`), case-study `AGENTS.md` (same rule, also lists required reading), and `FRAMEWORK.md` ("Canon must be recorded in `CANON.md` and logged in `DECISION_LOG.md`"). The branch rule is stated in root `AGENTS.md` and reinforced by every branch file's self-declaration.

The governance is clear in prose but soft in mechanism. Specifically:

- **`CANON.md` is the authority for accepted story facts.** Clear and consistently honored in practice.
- **`DECISION_LOG.md` records major accepted decisions.** Clear and consistently honored; Entry 014 extends the discipline to non-canon guidance decisions.
- **Branch files are exploratory.** Clear by rule and by branch-file convention.
- **Nothing becomes canon unless canon and decision log agree.** Stated as a rule, but no checklist verifies agreement before a canon edit is committed. The protection is convention, not a gate.
- **Branch technical specifics must not harden accidentally.** Stated per-file in the packets' "Canon-Governance Notes" sections, but not enforced by any framework-level rule or acceptance gate.

**Files or patterns that weaken this governance:**

- The thinness of the framework's enforcement layer. A model that skips the case-study `AGENTS.md` and reads only the root `AGENTS.md` and `FRAMEWORK.md` would understand the principle but not the mechanism.
- The absence of a canon-update-proposal template and a branch-to-canon merge template. The case study's reviews perform these functions informally; the framework does not formalize them.
- The `PROJECT_MANIFEST.md` and `README.md` in the Perth case study are stale (still pointing at Milestone 3 / plot-architecture-v1 as the current focus) while the actual work has advanced. This is not a governance violation but it creates a navigation hazard for a fresh model trying to orient.
- The skills under `.agents/skills/` are too thin to act as enforcement agents. A `canon-maintainer` skill with an eight-line body cannot actually perform a canon-update procedure.

## Template and Workflow Gaps

The `templates/README.md` lists eight planned templates (blank novel project, character file, decision log, canon file, open questions file, branch review report, chapter outline, style guide). None exist, and the list is incomplete relative to what the Perth case study has proven necessary. Missing or underdeveloped templates:

- **Architecture artifact.** Generalizes the plot-architecture, interweaving-map, and revelation-rhythm files. Includes design decisions, structure distribution, interweaving map, non-canon status.
- **Stress test / stress test review.** Generalizes the confession-pressure-decision stress test and its review. Includes core diagnosis, load distribution, failure modes, "what must remain unresolved," status confirmations.
- **Prose probe / prose probe review.** Generalizes `prose-probe-confession-v1.md` and its review. Probe includes prose plus self-audit; review includes verdict, what the probe proves/does not prove, strengths, risks, canon-governance risks, keep/change/avoid, recommendation.
- **Chapter packet / chapter packet review.** Generalizes `chapter-17-packet-v2.md` and its review. Includes chapter role, required inputs, scene objective, emotional states, revelation payload (canon-supported vs. branch-provisional), withheld information, handling notes, exposition limits, beat map, style constraints, failure modes, drafting checklist, canon-governance notes, verdict.
- **Acceptance-gate checklist.** Generalizes `chapter-17-packet-v2-acceptance-check.md`. Includes status notice, resolution check, remaining risks, final verdict.
- **Canon update proposal.** Currently absent. Requires the canon change, decision-log entry draft, downstream consequences, alternatives, governance status (canon vs. approved guidance), confirmation that `CANON.md` and `DECISION_LOG.md` will be edited together.
- **Branch-to-canon merge proposal.** Currently absent. Enumerates specifics promoted, dropped, and still provisional.
- **Model task prompt.** Currently absent. Standard envelope: role, inputs, branch status, canon-governance constraints, output format, acceptance gates.
- **Validation checklist.** Currently absent. Terminal gate: word count, required sections, changed-file restrictions, no canon edits unless explicitly requested, no absolute local links, no local file-scheme links, no temporary scripts left behind, `git status` clean, branch status declared.

## Acceptance-Gate Recommendations

The framework should ship a single reusable acceptance-gate checklist, parameterizable per artifact type. Recommended standard checks:

- **Word count:** within stated min/max for the artifact type.
- **Required sections:** all sections mandated by the artifact's template are present.
- **Changed-file restrictions:** only files within the artifact's intended scope were modified.
- **No canon edits unless explicitly requested:** `git diff --name-only` must not include `CANON.md` or `DECISION_LOG.md` for branch/probe/packet/draft/review tasks.
- **No absolute local links:** no `/Users/...`, `/home/...`, or any absolute filesystem path; use repo-relative paths only.
- **No local file-scheme links:** no `file:` URI scheme anywhere in the artifact.
- **No temporary scripts left behind:** no untracked scratch scripts; `git status --short` shows only intended changes.
- **Git status validation:** working tree state matches expectations.
- **Branch/non-canon status:** branch artifacts carry an explicit non-canon notice; canon operations update `CANON.md` and `DECISION_LOG.md` together.
- **Canon-governance notes:** provisional specifics are enumerated and not promoted to canon without a separate ratification step.

This checklist should live at `templates/acceptance-gate-checklist.md` and be referenced by the workflow docs, the skills, and the model-routing guidance.

## Model-Routing Recommendations

The framework should include a vendor-neutral model-routing guide that maps model strengths to roles. Recommended mapping, kept general:

- **Architecture synthesis.** Use a model strong at structured long-form reasoning, constraint satisfaction, and holding multiple strands in working memory. Route `plot-architect` skill. Output: architecture artifact or packet, never prose.
- **Science plausibility.** Use a model strong at technical accuracy and institutional realism. Route `science-checker` skill. Output: stress test, plausibility assessment, or science-as-character position note, never prose.
- **Literary prose drafting.** Use a model strong at voice, restraint, sensory grounding, and dialogue economy. Do not use the same model that built the packet if avoidable; separation reduces self-justification bias. Output: prose draft in `BRANCHES/`, never canon.
- **Prose review.** Use a model strong at critique, register-matching, and restraint enforcement. Route `literary-style-editor` skill. Must not be the same model that wrote the draft under review. Output: review with executive verdict, strengths, weaknesses, keep/change/avoid.
- **Repo cleanup.** Use a model strong at file-level consistency, naming conventions, and stale-state detection. Output: a read-only audit or a small, scoped diff for safe fixes only.
- **Consistency checking.** Use a model strong at contradiction detection across long contexts. Route `continuity-editor` skill. Output: contradiction report against canon, timeline, motivation, and prior decisions.
- **Canon governance.** Use a model strong at rule-following and at refusing to act without explicit instruction. Route `canon-maintainer` skill. Output: canon update proposal or branch-to-canon merge proposal only; actual edits to `CANON.md` and `DECISION_LOG.md` only on explicit instruction.
- **Implementation / scripted edits.** Use a model strong at precise file edits and verification commands. Output: scoped diff plus validation command results. Must run the acceptance-gate checklist before declaring done.

The guide should explicitly state the separation-of-authorship rule: a model that drafted prose should not be the same model that reviews it for the same gate, where alternatives are available. The Perth case study already follows this implicitly (probe, probe review, packet, packet review, draft, draft review are separate artifacts and would benefit from separate authorship); the framework should make it explicit.

## Suggested Fixes

### Immediate Safe Fixes

- Update `case-studies/perth-asteroid-novel/PROJECT_MANIFEST.md` "Current Milestone" and "Current Development Focus" to reflect Chapter 17 drafting rather than plot architecture. Low risk; documentation only.
- Update `case-studies/perth-asteroid-novel/README.md` "Development Status" similarly. Low risk.
- Reconcile `OPEN_QUESTIONS.md` `OQ-001` and `OQ-002` status lines with `DECISION_LOG.md` Entry 013 (mark both closed consistently). Low risk; touches open questions only, not canon.
- Add `.DS_Store` removal confirmation: the files exist on disk (per the untracked `find` output) but are gitignored and not tracked. No action needed beyond confirming they remain untracked. Low risk.
- Add a short top-level index to `README.md` linking to `FRAMEWORK.md`, `AGENTS.md`, `templates/`, `.agents/skills/`, and `case-studies/`. Low risk; improves discoverability.

### Medium Fixes

- Replace `templates/README.md`'s wish list with actual templates for at least the highest-value artifacts: prose probe, prose probe review, chapter packet, chapter packet review, acceptance-gate checklist. Medium risk; new files only, no edits to existing canon or branch files.
- Expand the five skill stubs under `.agents/skills/` with triggers, inputs, outputs, failure modes, and acceptance gates. Medium risk; new content in existing files, but no canon or story impact.
- Add a workflow document (e.g., `FRAMEWORK.md` appendix or a new `docs/workflow.md`) describing the architecture → probe → review → packet → packet review → acceptance → draft → draft review loop. Medium risk; framework-level, general.
- Add a model-routing guide under `docs/` or as an expansion of `AGENTS.md`. Medium risk; framework-level, vendor-neutral.
- Add a chapter-scoped subdirectory convention for `BRANCHES/` (e.g., `BRANCHES/chapter-17/`) and document it. Medium risk; only affects future artifacts, not existing ones, but requires a move plan.

### Larger Refactors

- Lift the entire Perth-proven workflow into a generalized framework with templates, acceptance gates, model routing, and a "start a new novel project" guide. High risk in scope, low risk in content (framework-level, no canon impact); should be planned before execution.
- Promote the "provisional specifics" and "optional discoveries" conventions into framework-level rules with examples drawn (abstractly) from Perth without copying case content. High value, medium risk; requires careful abstraction to avoid leaking case detail.
- Build a canon-update and branch-to-canon merge ritual with templates and an acceptance gate that verifies both `CANON.md` and `DECISION_LOG.md` are updated together. High value, medium risk; touches governance mechanics.

## Proposed New or Updated Files

Repo-relative paths only.

- `templates/prose-probe.md` — reusable prose probe template (non-canon notice, probe prose, self-audit, provisional specifics). Low risk.
- `templates/prose-probe-review.md` — reusable probe review (verdict, strengths, risks, keep/change/avoid, recommendation). Low risk.
- `templates/chapter-packet.md` — reusable packet template (branch status, chapter role, required inputs, revelation payload split canon-supported vs. branch-provisional, handling notes, beat map, failure modes, drafting checklist, canon-governance notes). Low risk.
- `templates/chapter-packet-review.md` — reusable packet review. Low risk.
- `templates/acceptance-gate-checklist.md` — reusable acceptance gate (status, resolution check, remaining risks, verdict) and the standard checks listed above. Low risk.
- `templates/architecture-artifact.md` — reusable architecture artifact (design decisions, structure distribution, interweaving map, failure modes). Low risk.
- `templates/stress-test.md` and `templates/stress-test-review.md` — reusable stress test and review. Low risk.
- `templates/canon-update-proposal.md` — standard canon-change proposal with confirmation that `CANON.md` and `DECISION_LOG.md` will be edited together. Medium risk.
- `templates/branch-to-canon-merge-proposal.md` — standard branch-promotion proposal (specifics promoted, dropped, provisional). Medium risk.
- `templates/model-task-prompt.md` — standard model-task envelope with separation-of-authorship note. Low risk.
- `templates/validation-checklist.md` — terminal validation checklist. Low risk.
- `docs/workflow.md` (new) or expanded `FRAMEWORK.md` — document the proven loop per-stage with inputs, outputs, and acceptance gate. Medium risk.
- `docs/model-routing.md` (new) or expanded `AGENTS.md` — vendor-neutral model-to-role mapping. Medium risk.
- `.agents/skills/*/SKILL.md` (expand all five) — make each skill actionable with triggers, inputs, procedure, outputs, refusal conditions, acceptance gate. Medium risk, framework-level.
- `case-studies/perth-asteroid-novel/PROJECT_MANIFEST.md` and `case-studies/perth-asteroid-novel/README.md` (update) — refresh stale milestone pointers to Chapter 17 drafting. Low risk, documentation only.
- `case-studies/perth-asteroid-novel/OPEN_QUESTIONS.md` (update) — reconcile `OQ-001`/`OQ-002` status with decision-log Entry 013. Low risk, open questions only.

## What Not To Change

- Do not change `CANON.md` or `DECISION_LOG.md` — both are dense, internally consistent, and explicitly protected; the decision-log entry format (especially Entry 014's governance line) is a model for future entries.
- Do not change any `BRANCHES/` artifact's content — retroactive rewriting would distort the audit trail.
- Do not change `STYLE_GUIDE.md` or `THEMES.md` — both are working well; the style guide is one of the strongest files in the repo.
- Do not lift Perth-specific content (Martin, Bianca, Giacob, the asteroid, the three-strand structure, the "Science as Character" position) into the framework. The framework rule against baking case detail into framework files is correct and should hold.
- Do not prematurely generalize "Science as Character"; at most the framework can generalize the meta-pattern (style/method positions recorded as decision-log entries marked "Approved Guidance," not canon).
- Do not restructure `BRANCHES/` into chapter subdirectories mid-chapter-cycle.
- Do not change the split license or `.gitignore` — both are correct and sensible.

## Recommended Next Sequence

A practical sequence for the next 3–6 tasks, balancing momentum and consolidation:

1. **Verify the v2 draft against its own acceptance criteria** — a v2 draft review (`BRANCHES/chapter-17-draft-review-v2.md`) checking the v2 draft against the v1 review's revision recommendations. Keeps Chapter 17 momentum without new framework work.
2. **Make the immediate safe fixes** — refresh `PROJECT_MANIFEST.md`, case `README.md`, and `OPEN_QUESTIONS.md` `OQ-001`/`OQ-002` status. Low risk, clears stale-state navigation hazards for any model that next enters the repo.
3. **Create the three highest-value templates** — `templates/chapter-packet.md`, `templates/acceptance-gate-checklist.md`, `templates/probe-probe-review.md` (probe + probe review). These are the artifacts the Perth case study has proven most necessary. Low risk, new files only.
4. **Add a short framework workflow document** — `docs/workflow.md` or an appended section to `FRAMEWORK.md` naming the architecture → probe → packet → draft → review loop. Medium risk, framework-level.
5. **Expand the two most safety-critical skills** — `canon-maintainer` and `continuity-editor` — from one-line stubs into actionable procedures with refusal conditions and acceptance gates. Medium risk, framework-level.
6. **Decide Chapter 17's disposition** — accept v2 as the chapter's working draft, or produce a v3, then move to Chapter 18. Preserve prose momentum; do not let framework consolidation stall the novel.

This sequence keeps the Perth case study moving (tasks 1 and 6) while doing the cheapest high-value framework consolidation first (tasks 2, 3) and deferring the larger structural framework work (tasks 4, 5) until after the cheapest wins land. It deliberately avoids the larger refactors in the suggested-fixes section; those should be planned, not improvised.

## Final Recommendation

**Hybrid approach: continue the Perth case study, but pause for a short, scoped framework consolidation first.**

The case study is not blocked and should not be stalled. But the framework is now thin enough that the next model entering the repo will have to reverse-engineer Perth to understand the working method, which is exactly the kind of case-specific dependency the framework rules are meant to prevent. A single short pass — immediate safe fixes, three high-value templates, one short workflow doc — would lift the proven Perth pattern into reusable form without touching canon, branch artifacts, style, or themes. That pass is low-risk and high-leverage. After it, the case study should resume with the v2 draft review and proceed toward Chapter 18.

The repo should not do a full framework refactor before continuing the case study. The larger refactors (expanded skills, full template set, model-routing guide, canon-update ritual) are valuable but should be planned and incremental, not blocking. The single most important principle to preserve is the one the repo already states well: exploration should be cheap; canon should be deliberate. The framework consolidation pass should make that principle easier for future models to follow, not heavier.