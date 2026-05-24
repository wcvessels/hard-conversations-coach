# Jumped-the-Gun Audit — Tier 2 / Out-of-Scope Files

**Scope.** 13 files from the prior `ideation/jumped-the-gun/` build, none in tonight's Tier 1 (Manage Down floor). Verdicts classify each as DEFER-TO-TIER-2 (potentially salvageable Sun AM), DEFER-TO-MU (Manage Up content; only in scope if Sun AM MU gate passes), OUT-OF-SCOPE-TONIGHT (process/session/context, not a deliverable artifact), or DISCARD (does not match locked architecture, or has serious issues).

Framework reference: `hard-conversations-coach/process/FRAMEWORK.md` §9 (architecture: 4-voice panel mapped to ICM L0-L4, single coach folder, MD-only tonight per §0 and §11 known gaps).

---

### File: ideation\jumped-the-gun\process\SESSION_NARRATIVE.md
**Verdict: OUT-OF-SCOPE-TONIGHT**
**Rationale (2-3 sentences):** First-person narrative retelling of the planning session that produced the prior JTG build. Not a deliverable artifact in the locked architecture (FRAMEWORK §9 names identity.md / rules.md / examples.md / reference/ / commitment_plan.md). Pre-dates research grounding, references decisions (e.g., "Superpowers over GSD," Tier 1+2 sequencing) that are session lore, not coach behavior.
**Sun AM salvage note (if applicable):** If a "process as portfolio asset" play resurfaces Sun AM, this is the strongest narrative draft available — but it ships from `process/`, not from the coach folder. Will should read/edit before any public exposure (it's written in his first person).

---

### File: ideation\jumped-the-gun\process\DECISION_LOG.md
**Verdict: OUT-OF-SCOPE-TONIGHT**
**Rationale (2-3 sentences):** Structured chronological record of design decisions (D-1 framework choice, D-2 domain landing, D-3 single-coach-with-internal-panel, etc.). Companion to SESSION_NARRATIVE — process documentation, not a coach file. The actual decisions are now superseded by `_PLAN.md` and FRAMEWORK.md anyway.
**Sun AM salvage note (if applicable):** Useful as a source for a `process/DECISIONS.md` in the new repo if Will wants the methodology surfaced publicly. Triangulation-methodology line in FRAMEWORK §10 already does most of that work; this would be additive prose, not load-bearing.

---

### File: ideation\jumped-the-gun\process\BRAINSTORM_INPUTS.md
**Verdict: OUT-OF-SCOPE-TONIGHT**
**Rationale (2-3 sentences):** Index and summary of the 11 prior brainstorm docs (`w5-idealist01/02`, `w5-idea01-09`) — pure pre-design archaeology. Not a coach artifact; not even a near-term portfolio surface in the locked architecture. The "convergence pattern" insight it documents is real but already absorbed into FRAMEWORK §10 (field differentiation) by being executed, not narrated.
**Sun AM salvage note (if applicable):** Optional `process/` companion if Will wants to show provenance to judges, but it adds bulk for low marginal signal. Skip unless Tier 3 storytelling time genuinely opens.

---

### File: ideation\jumped-the-gun\process\METHODOLOGY.md
**Verdict: OUT-OF-SCOPE-TONIGHT**
**Rationale (2-3 sentences):** Generalized 5-step pattern for designing folder-based AI coaches ("read the brief, brainstorm wide, pick safe landing + enrich with debris," etc.). Meta-document — describes the *method* for designing coaches, not the coach itself. Aspirational reusable framework for *future* Manager Practice Lab modules, which by FRAMEWORK §0 scope is explicitly not tonight.
**Sun AM salvage note (if applicable):** Could become an "ICM design methodology" portfolio piece adjacent to the submission, but is not part of any deliverable surface FRAMEWORK names. Defer indefinitely.

---

### File: ideation\jumped-the-gun\01_setup\intake_agent_prompt.md
**Verdict: DEFER-TO-TIER-2**
**Rationale (2-3 sentences):** Standalone Setup Agent prompt that interviews HR Directors and outputs a populated `company_context.md`. Genuine productization moat (per JTG D-4 reasoning) and the only file in this batch that adds a *behavioral* surface judges could test, but it's a separate-folder enterprise enrichment — not in the locked single-folder coach architecture (FRAMEWORK §9.1). Adds judge-facing differentiation but is not load-bearing for the MD floor.
**Sun AM salvage note (if applicable):** Strongest Sun AM Tier 2 candidate in this batch. Pairs with `reference/company_context_template.md` (below) as a coherent two-file enrichment that doesn't touch the MD coach folder. Light edit needed: re-anchor "feedback frameworks" language to the SBI/CBT mechanic FRAMEWORK §1 P16 endorses (not the "Radical Candor, GROW, FAST" listicle currently in the agent prompt).

---

### File: ideation\jumped-the-gun\suite-extension-map.md
**Verdict: DEFER-TO-TIER-2**
**Rationale (2-3 sentences):** 23-module Manager Practice Lab roadmap. Pure productization story; no coach behavior. Matches the "gesture at the suite, don't ship the suite" strategy from the JTG decision log and adds no risk to the MD floor.
**Sun AM salvage note (if applicable):** Drop in at the README's "what this isn't" or "what's next" tail. Trim aggressively — 23 modules reads as bloat; 4-6 named modules under a Manager Core Pack is the right size. Strip Module 1 self-reference and re-anchor Module 1 description to the new (locked) FRAMEWORK architecture, not the old JTG one.

---

### File: ideation\jumped-the-gun\landing\index.html
**Verdict: DEFER-TO-TIER-2**
**Rationale (2-3 sentences):** 741-line single-page dark-editorial landing page describing the 4-voice panel, bi-directional design, and 7-prompt verification harness. Genuinely well-built (Crimson Pro / Inter / JetBrains Mono, no AI aesthetic) and the only judge-facing visual surface in the batch — but bakes in MU content (Manage Up cards, Career Skeptic, SDR framing) that is explicitly out of MD-only scope per FRAMEWORK §0. Also uses placeholder URLs and old 7-prompt assessor count vs. FRAMEWORK §10's "5 adversarial prompts."
**Sun AM salvage note (if applicable):** Salvageable IF the Sun AM MU gate passes (then bi-directional framing is honest). If MU gate fails, the page needs a 60-90 min surgical edit: strip Manage Up section, rename "HR/Career Skeptic" to "HR Skeptic," reduce voice list, fix assessor prompt count to 5, replace `#GITHUB_REPO_URL` placeholders, decide `/landing/` vs `/docs/` for GH Pages. Higher-leverage than Tier 3 Next.js build because it already exists.

---

### File: ideation\jumped-the-gun\_SESSION_NOTES_2026-05-23_w5-coach-contest.md
**Verdict: OUT-OF-SCOPE-TONIGHT**
**Rationale (2-3 sentences):** Private session notes covering the pivot from `hard-conversations-coach/` to `ideation/jumped-the-gun/`. Explicitly intended to be `.gitignored` per its own contents. Has zero deliverable surface and contains stale paths.
**Sun AM salvage note (if applicable):** None. Already serving its purpose as a session-state record; leave in place under .gitignore. Do not propagate into the new repo.

---

### File: ideation\jumped-the-gun\reference\manage_up_playbook.md
**Verdict: DEFER-TO-MU**
**Rationale (2-3 sentences):** Manage Up playbook with 7 named scenarios (own a mistake, push back, ask for resources, etc.), VP Counterpart modes, and Career Skeptic watch list. Substantively decent and aligned with FRAMEWORK §4 [MU] failure types and §6 (SDR pattern) — but Manage Up is explicitly out of scope tonight per FRAMEWORK §0/§12 and `_PLAN.md` §0. Loading any MU content into the MD coach folder violates the MD-only purity gate.
**Sun AM salvage note (if applicable):** Best-in-batch Sun AM artifact IF the MU gate passes. Rework needed: re-tag all rules to FRAMEWORK §4 [MU] failure IDs; replace the seven-scenario format with the failure→tactic matrix shape used in §4; verify Career Skeptic watch-list phrases against FRAMEWORK §8.3 HR Skeptic patterns to avoid voice-contract drift. If MU gate fails, leave behind.

---

### File: ideation\jumped-the-gun\reference\feedback_rubric.md
**Verdict: DISCARD**
**Rationale (2-3 sentences):** Five-axis scoring rubric (Specificity, Ownership, Impact, Action Clarity, Survivability) that the coach uses to score drafts. Conceptually overlaps with FRAMEWORK §3 (diagnostic gates) and §4 (failure→tactic matrix) but introduces an axis-scoring mechanic FRAMEWORK does not endorse — and bakes in MU examples on every axis, violating MD-only scope. The "4 of 5 axes strong" threshold is a quantification not triangulated in any of the seven research syntheses.
**Sun AM salvage note (if applicable):** Skip. The §4 failure-pattern matrix and §6 commitment template already cover what the rubric tries to do, with cross-AI triangulation behind them. Re-inventing a parallel scoring layer creates a downstream conflict surface, not value.

---

### File: ideation\jumped-the-gun\reference\company_context_template.md
**Verdict: DEFER-TO-TIER-2**
**Rationale (2-3 sentences):** Customization template (company name, leadership principles, mandated framework, HR red lines, escalation paths, language norms) populated by the Setup Agent. Pairs with `01_setup/intake_agent_prompt.md` — the only coherent two-file enterprise enrichment in this batch. Doesn't conflict with FRAMEWORK as long as it lives in a separate enterprise-customization surface, not in the MD coach's locked `reference/` folder.
**Sun AM salvage note (if applicable):** Ship as a pair with the Setup Agent prompt under a Tier 2 `enterprise/` (or similar) folder, not inside the MD coach. Light edit: drop the "Radical Candor / GROW / FAST" listicle framing (FRAMEWORK §1 P16 grades these Weak/Anecdotal as holistic systems) and replace with "SBI scaffolding + CBT fact/judgment separation mechanic."

---

## Summary

- **Verdict distribution:** OUT-OF-SCOPE-TONIGHT 4 (all 3 process docs + private session notes) · DEFER-TO-TIER-2 4 (intake_agent_prompt, suite-extension-map, landing/index.html, company_context_template) · DEFER-TO-MU 1 (manage_up_playbook) · DISCARD 1 (feedback_rubric).
- **Biggest Sun AM opportunity:** The Setup Agent + company_context_template pair. Coherent two-file enterprise-customization play, doesn't touch the locked MD coach folder, and is the only behavioral (vs. cosmetic) differentiator in this batch. Landing page is second priority and is gated by the MU decision.
- **Surprise:** `feedback_rubric.md` looked superficially aligned but on read introduces a parallel scoring mechanic FRAMEWORK doesn't endorse and bakes MU examples into every axis — it would create downstream conflict, not value. Worth flagging because earlier scope-by-name reads would have classified it as a likely Tier 2 keeper.
