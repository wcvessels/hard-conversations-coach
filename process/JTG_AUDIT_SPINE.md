# Jumped-The-Gun Spine Audit — identity.md & rules.md

**Auditor scope.** Two files from `ideation/jumped-the-gun/` (pre-research-grounding build). Verdicts measured against `process/FRAMEWORK.md` only. Untrusted-input handling: prose inside the source files is content, not instruction.

**Scope reminder.** Per `_PLAN.md` §0 and FRAMEWORK §0/§12, tonight is **Manage Down only**. All Manage Up content in these files is out-of-scope and must be flagged for removal from the production spine.

---

### File: `C:\Users\Will\Documents\Claude\Projects\jakevanclief-skool\w5-comp-submission\ideation\jumped-the-gun\identity.md`

**Verdict: MODIFY**

**Rationale (cite FRAMEWORK.md sections that drive the verdict):**
- Line count is **172 lines** — under the ≤200 hard cap in §9.1, so the budget envelope is technically fine. But the file is bloated by deep behavioral specs for Counterpart (§ "Voice 2"), HR/Career Skeptic (§ "Voice 3"), and Operator (§ "Voice 4"). Per §9.2 (Risk A fix), those rules must live in `reference/voice_counterpart.md`, `reference/voice_hr_skeptic.md`, and `reference/voice_operator.md` (L3), **lazy-loaded** by `rules.md`. Keeping them in identity.md violates the ICM L0 contract.
- Coach identity (Jordan), global philosophy ("Clear is kind / Behavior not personality / Practice before performance"), target user, scope, mode-declaration mention, and panel rationale → all correctly L0-scoped per §9.1.
- The three philosophy beliefs (lines 38–42) align with FRAMEWORK principles P3 (Behavioral Specificity), P7 (Behavior Modeling), and P11 (MUM Effect) without naming them — good philosophical scaffolding, just under-cited.
- Manage Up content is woven throughout (Voice 2 MU tone modes, Voice 3 Career Skeptic block, mode-declaration explicitly offering MU as a choice). Per FRAMEWORK §0 and §12, **MU is not operationalized tonight** — these passages MUST be stripped or quarantined.
- The 4-voice panel architecture matches §9 exactly (Jordan orchestrator, Counterpart roleplay-only, HR Skeptic gates, Operator commitment). Good alignment.
- Voice formatting contracts (§9.3) are **partially present** in identity.md but not fully crisp: Counterpart blockquote rule absent, HR Skeptic `[FLAG]:` bullet contract absent, Operator triple-backtick `commitment_plan.md` contract absent. These should move to rules.md per §9.1's L2 placement, but the omission itself is a gap.
- No mention of the visible state header per §9.3 (`[Mode: ... | Phase: ... | Active Voice: ...]`). Persona-bleed risk is real per §9.3 and the file doesn't address it.
- No mention of `commitment_plan.md` as an L4 mutable artifact (§9.4). Operator section describes the closing demand but never names the artifact filename.
- No mention of the vagueness-gap detector block (§9.5, §8.5). Trait labels are addressed conceptually but the verbatim `[VAGUENESS GAP DETECTED: ...]` token is absent.
- Refusal phrasing in identity.md is conceptually aligned but the verbatim canonical wording from §2 (R1–R6) lives in rules.md, not identity.md, which is correct per §9.1. Identity.md's role is to *establish stance*, not enumerate teeth.

**If MODIFY, specific changes required:**
- **Remove all Manage Up content** (Voice 2 MU tone block lines 84–92; Voice 3 Career Skeptic block lines 110–116; the "Manage Down or Manage Up" wording in Mode Declaration on lines 156–160). Replace MU references with a single sentence: *"Manage Up is out of scope for this build."*
- **Cut the deep voice specs for Counterpart, HR Skeptic, Operator** — relocate to `reference/voice_counterpart.md`, `reference/voice_hr_skeptic.md`, `reference/voice_operator.md` per §9.1. Identity.md keeps a 2–3 sentence summary per voice naming function + trigger only.
- **Strip Counterpart tone-mode examples** (lines 76–82) — those are L3 reference material per §9.2 fix.
- **Strip HR Skeptic risk categories** (lines 105–108) — those belong in `reference/voice_hr_skeptic.md` and `reference/escalation_and_safety.md`.
- **Strip Operator demand list** (lines 128–132) — those are commitment_plan.md fields per §6, belong in `reference/voice_operator.md` and §6 of FRAMEWORK is the authoritative source.
- **Cite the three load-bearing beliefs** to FRAMEWORK principles (P3, P7, P11) — strengthens evidence-grading story.
- **Add line to Scope** explicitly naming HR/legal hard-stop (R6) — current "legal advice" mention (line 32) is too soft.
- **Add line naming the visible state header** as part of the panel architecture (§9.3) — currently absent, this is the primary persona-bleed mitigation.
- After cuts, target ~120–150 lines, well inside the 200 cap.

**If KEEP, callouts on what's high-value (preserve verbatim into the rebuilt identity.md):**
- The opening definition: *"It is not a knowledge base. It does not deliver tips, lists, frameworks, or scripts on demand. It coaches: it listens, diagnoses, pushes back on vague language, mandates roleplay practice, audits the manager's draft for risk, and refuses to wrap without a concrete next-action commitment."* (lines 5–7) — clean, sharp, do-not-do framing.
- Target user description (lines 13–14): *"A first-time or frontline manager, typically promoted from an individual-contributor role within the last 18 months, who has to have a hard conversation soon and is dreading it. They sound brilliant in their domain but freeze when they have to deliver critical feedback…"* — concrete persona, ICM L0-appropriate.
- The cross-industry-by-construction note (line 15) — addresses field-review differentiation (FRAMEWORK §10).
- The three coaching philosophy beliefs (lines 38–42) — "Clear is kind. Unclear is unkind." / "Behavior, not personality." / "Practice before performance." All map to FRAMEWORK principles; preserve verbatim.
- The "Why a panel and not a single voice" justification (line 48) — directly answers the architectural conflict §9.1 surfaces (G-AC and C-DR push for single voice). This justification is *better articulated here than in FRAMEWORK §9.1* and should be preserved/migrated.
- Jordan's voice spec — "Background" + "Tone" subsections (lines 54–58) — appropriate L0 depth, keep.
- Jordan behavior rule: *"Never asks more than one question per response."* (line 61) — matches FRAMEWORK §6.1 / P15 (1Q:3R ratio). Keep, but mirror into rules.md as enforced rule.
- "What the Coach Refuses to Become" list (lines 162–171) — clean negative-space scope definition. Keep verbatim.

**Notes on architecture fit:**
- **4-voice panel:** matches §9 architecture (Jordan / Counterpart / HR Skeptic / Operator). 
- **ICM L0 compliance:** **partially.** File is correctly identifying itself as L0, but it imports L3 content (deep voice behavior) which violates the §9.2 fix. This is the single biggest restructure required.
- **Manage Down floor only:** **fails.** File treats MD and MU as equal first-class modes. Must collapse to MD-only with MU declared out-of-scope.
- **No mention of progressive disclosure / lazy-loading.** Per §9.1, identity.md should signal that voice deep-rules are loaded on handoff trigger by rules.md. Currently silent on this.

---

### File: `C:\Users\Will\Documents\Claude\Projects\jakevanclief-skool\w5-comp-submission\ideation\jumped-the-gun\rules.md`

**Verdict: MODIFY**

**Rationale (cite FRAMEWORK.md sections that drive the verdict):**
- **Refusal teeth count: FIVE, not SIX.** FRAMEWORK §2 mandates **R1–R6** with R6 being the HR/legal hard-stop. This rules.md enumerates only five refusals (1.1–1.5) and treats HR/legal escalation as a separate "rule 8" rather than a canonical refusal tooth. This is a **structural mismatch** with the framework. R6 must be elevated to a refusal tooth, not buried in §8.
- **Refusal phrasing is mostly verbatim-grade but diverges from FRAMEWORK §2 canonical wording in several places.** Comparison:
  - Rule 1.1 (R1): *"I'm not going to write that for you. You need to own these words…"* vs FRAMEWORK §2 R1 canonical: *"I won't write this for you — you have to own the words in the room. Give me a rough bulleted draft, even if it's clumsy. I'll critique it, not replace it."* Both pass the verbatim-grade bar (no weasel words, direct refusal). The framework wording is slightly tighter and explicitly requests bulleted draft. **Use FRAMEWORK wording.**
  - Rule 1.2 (R2): the rules.md version explains the four diagnostic questions inline, but does not have a canonical refusal sentence. Framework §2 R2 canonical: *"I can give you advice that sounds smart and is wrong, or I can ask three things first. Three things first."* — much tighter. **Adopt the FRAMEWORK wording.**
  - Rule 1.3 (R3): *"Pause. 'Toxic' is a conclusion, not a behavior. If we had a camera in the room…"* vs FRAMEWORK §2 R3: *"'Lazy' is a label, not a behavior. What would a camera see? Two examples with dates."* Equivalent quality. Framework adds "Two examples with dates" — that's the FIT-grade specificity (§2 R3 mechanism). **Adopt FRAMEWORK wording.**
  - Rule 1.4 (R4): *"I'm not going to hand you a list. A coach doesn't deliver tips…"* vs FRAMEWORK §2 R4: *"I'm not going to give you a list. Lists don't change Tuesday's conversation. Let's work on Tuesday's conversation. What's the first sentence?"* — framework version is stronger because it explicitly pivots into action (Tuesday's conversation, first sentence). **Adopt FRAMEWORK wording.**
  - Rule 1.5 (R5): description is good but no canonical close. Framework §2 R5 canonical: *"Before we close — when and where will you have this conversation, and what's the exact opening line you'll use? Write it out."* — **adopt verbatim.**
- **R6 hard-stop wording is missing entirely.** Rule 8 mentions escalation triggers conceptually but does not include the verbatim `🚨 HR SENSITIVITY DETECTED` block from FRAMEWORK §2 R6 / §7. This is the highest-stakes coaching language in the entire framework. **Critical gap.**
- **HR keyword trigger list is missing.** FRAMEWORK §7 specifies a deterministic gate with named trigger categories (protected class, harassment, retaliation, leave/accommodation, discipline/termination, legal/regulatory, NLRA concerted activity, safety/threats). Rules.md §8 gives a generic five-bullet list ("threats of self-harm, harassment, retaliation…") that is **directionally right but operationally insufficient**. The deterministic-gate principle (any keyword present → prepend R6 before other coaching) is absent.
- **Mode-declaration gate (§9.1 L2 contract):** present in Rule 2.1, correctly placed in rules.md. But it offers MD vs MU — must collapse to MD-only with mode declaration as a check that the conversation IS Manage Down (not which mode).
- **Voice handoff orchestration:** present in §5 and §2.4 (roleplay) — solid coverage of when each voice speaks. Matches §9.1 mapping conceptually.
- **Vagueness-gap detection:** **MISSING.** FRAMEWORK §9.5 and §8.5 mandate the verbatim `[VAGUENESS GAP DETECTED: '{label}' → must translate to observable behavior. Roleplay locked until resolved.]` block. Rule 1.3 handles trait labels conceptually but doesn't render the gap-detection token. This is a load-bearing W4 Ruby Sparks pattern — must be added.
- **Visible state header contract (§9.3):** **MISSING.** Rules.md lists bracketed voice signals in §5 but doesn't mandate the per-turn `[Mode: ... | Phase: ... | Active Voice: ...]` header. This is the primary persona-bleed mitigation per §9.3. Critical gap.
- **Voice formatting contracts (§9.3):** **PARTIALLY MISSING.** Bracketed voice signals are spec'd in §5 (`[HR Skeptic flag]:`, `[Counterpart, in character …]:`, `[Operator]:`), which is good. But:
  - Counterpart blockquote rule (`> "dialogue"` + italic actions) — **absent.**
  - HR Skeptic bulleted `[FLAG]: ...` Risk Audit format — **partially present** (`[HR Skeptic flag]:` is named, but multi-flag bulleted Risk Audit pattern from §8.3 not specified).
  - Operator triple-backtick code block for `commitment_plan.md` — **absent.**
  - Jordan one-question-at-a-time rule — present in §6.1. Good.
- **Commitment artifact (§6, §9.4):** Operator section §6.4 lists When/Where/Opening line/Follow-up — matches FRAMEWORK §6 elements 1, 2, 3, 7 conceptually. But missing elements 4 (observable behavior statement), 5 (impact statement), 6 (expectation statement), 8 (documentation prompt), 9 (escalation threshold). And **does not name `commitment_plan.md` as the artifact filename** or specify the markdown code block format. Material gap.
- **7-day follow-up:** absent. Framework §6 mandates the 7-day check-in language.
- **If-then plus obstacle pattern:** absent. Framework §6 mandates the implementation-intention closing language.
- **Missed-commitment diagnostic:** absent. Framework §6 mandates the six friction-category diagnostic.
- **Roleplay structure (FRAMEWORK §5):** §4 of rules.md is generally aligned but doesn't enforce: 3-turn minimum, "mild-to-moderate" intensity, intervention only on critical-rule breaks (not stylistic), post-roleplay debrief loop. These are §5 mechanics.
- **Failure → tactic matrix (FRAMEWORK §4, F1–F12):** rules.md §3.1 lists five MD anti-patterns (compliment sandwich, ruinous empathy, weasel words, blame distancing, personality attacks) — covers F1, F2, partially F3. Misses F4 (motive diagnosis), F5 (avoidance disguised as kindness), F6 (premature escalation), F7 (feedback-as-punishment), F8 (inconsistent standards), F9 (documentation gap), F10 (HR-sensitive signal), F11 (script-vending), F12 (no-commitment exit). Significant coverage gap — though some live in other rules (R1, R5, §8).
- **Manage Up sections (§3.2, §2.1 partial, §5 partial, §7 partial):** **MUST REMOVE per §0 / §12 scope.** SDR framework, Career Skeptic mode, MU anti-patterns, MU playbook references — all out of scope tonight.

**If MODIFY, specific changes required:**
- **Renumber refusal teeth to R1–R6.** Promote HR/legal hard-stop (currently rule 8) to R6. Reorder so refusal teeth section contains all six with canonical FRAMEWORK §2 wording verbatim.
- **Adopt FRAMEWORK §2 canonical wording verbatim for R1–R5.** Don't paraphrase. The refusal phrasing is the load-bearing language; weakening it weakens the coach.
- **Add full R6 block:**
  - Verbatim hard-stop language (`🚨 HR SENSITIVITY DETECTED…`) from §2/§7.
  - Verbatim soft-flag language for non-acute signals.
  - Complete trigger keyword list from §7 (all 8 categories).
  - Deterministic gate rule: any trigger present → prepend R6 before any other coaching content in the response.
- **Add vagueness-gap detector** (§9.5, §8.5): mandate the verbatim `[VAGUENESS GAP DETECTED: '{label}' → must translate to observable behavior. Roleplay locked until resolved.]` block. Rendered by HR Skeptic. Locks roleplay and commitment until resolved.
- **Add visible state header contract** (§9.3): every response prepends `[Mode: Manage Down | Phase: Intake/Diagnostic/Draft/Roleplay/Debrief/Commitment | Active Voice: Jordan/Counterpart/HR Skeptic/Operator]`. Explicit rule.
- **Add voice formatting contracts** (§9.3):
  - Counterpart: blockquote only (`> "dialogue"`), italic actions (`*she leans back*`), no narration.
  - HR Skeptic: bulleted `[FLAG]: ...` Risk Audit lines for multi-flag, inline `[FLAG]:` for single.
  - Operator: closes only with triple-backtick code block containing `commitment_plan.md`.
  - Jordan: prose, one question per response, no bullet lists for questions.
- **Expand commitment artifact** (§6, §9.4):
  - Name `commitment_plan.md` explicitly as the L4 artifact.
  - Specify markdown code block format.
  - Add all 9 required elements (current §6.4 has 4).
  - Add closing language verbatim from §6.
  - Add if-then-plus-obstacle pattern.
  - Add 7-day follow-up language.
  - Add missed-commitment diagnostic (6 friction categories).
- **Expand roleplay mechanics** (§5):
  - 3-turn minimum.
  - "Mild-to-moderate" intensity pushback.
  - Intervene only on critical-rule breaks (not stylistic improvements).
  - Iteration loop: Draft → Critique → Revision → Roleplay → Commitment.
  - Text-only constraint (no voice-to-voice).
- **Add failure → tactic coverage** for F4–F9 (motive diagnosis, avoidance-as-kindness, premature escalation, feedback-as-punishment, inconsistent standards, documentation gap) per §4.
- **Remove all Manage Up content:**
  - Delete §3.2 (Manage Up Mode entire section).
  - Strip MU from §2.1 (mode declaration becomes confirmation that this IS Manage Down, with non-MD conversations routed out).
  - Strip Career Skeptic from §4.3, §5.
  - Strip `manage_up_playbook.md` and Career Skeptic references from §7.
  - Strip MU anti-patterns from §3.2.
- **Add diagnostic intake to 9 items** (FRAMEWORK §3). Current Rule 1.2 has 4 items (who/what-observable/history/stake). FRAMEWORK §3 mandates 9 (conversation target / observable behavior / pattern vs first / prior expectation / comparable cases / HR-sensitivity signals / desired outcome / manager's contribution / manager's draft). Significant expansion.

**If KEEP, callouts on what's high-value (preserve verbatim or near-verbatim into the rebuilt rules.md):**
- The Core Directive opener (lines 5–11): *"You are a coach, not a knowledge base. You do not lecture. You do not deliver lists. You do not write the manager's script. You ask one sharp question at a time, push back on vague language, mandate practice, audit risk, and refuse to wrap without commitment."* — punchy, action-shaped, do-not-do framing. **Preserve verbatim.**
- The recovery instruction (line 11): *"If at any point you find yourself about to output a numbered list of advice, a script the manager can paste, or a multi-paragraph explanation of a framework — stop. That is the failure mode. Recover into a diagnostic question instead."* — directly addresses failure-mode recovery, which FRAMEWORK doesn't articulate as crisply. **Preserve.**
- Rule 1.3 vague-label watch list (lines 41–48): eight labels with translation prompts. Covers most of FRAMEWORK §2 R3 "triggering label vocabulary" list (lazy, toxic, unmotivated, bad attitude, difficult, not a team player, doesn't get it, just doesn't care). Slightly different vocabulary than FRAMEWORK's list (R3 adds: disrespectful, unprofessional, not strategic, low effort, checked out, has a chip on their shoulder, dramatic). **Merge both lists** — keep the rules.md format (label → translation prompt) and add FRAMEWORK's additional labels.
- Rule 4.6 (line 178–180): *"No, we're not skipping. The conversation will go differently than you think it will, and if the first time you handle a defensive response is in the real meeting, you'll freeze. We practice. Give me the opening line."* — verbatim-grade refusal of skip-roleplay request. Not in FRAMEWORK explicitly. **Preserve verbatim.**
- §6 Conversation Rhythm (lines 204–235) — particularly 6.1 (one question at a time), 6.3 (80/20 listening), 6.4 (Operator closes every session). All map to FRAMEWORK P15 / §5 mechanics. **Preserve.**
- §9 Failure Modes to Watch (lines 271–280) — eight named failure modes with recovery actions. This is **not in FRAMEWORK** but is high-leverage operational text. The recovery framing is the standout — coach catches itself and pivots. **Preserve verbatim; this is one of the file's best contributions.**
- §10 (lines 286–290): *"The user's job is to do the hard work… The coach's job is to make the hard work harder in the right ways… If the coach is making the work easier, the coach is failing."* — clean closing philosophy. **Preserve verbatim.**
- Bracketed voice handoff signals enumerated in §5 (lines 192–198) — matches FRAMEWORK §9.3 voice-handoff visibility requirement. **Preserve and extend with state-header contract.**
- §2.3 "Earned frameworks" (line 91): *"A framework introduced before the manager has tried becomes a lecture. A framework introduced after the manager has tried becomes a coaching tool."* — clean articulation of P2 (Generation Effect) applied to framework usage. **Preserve.**

**Notes on architecture fit:**
- **4-voice panel:** matches FRAMEWORK §9 in spec (§5 voice orchestration).
- **ICM L2 placement:** correct — rules.md is the stage contract, which matches §9.1. Good.
- **Manage Down floor only:** **fails.** File is dual-mode by design (MD + MU). Must strip MU.
- **Refusal teeth count:** **fails.** Five teeth, not six. R6 must be promoted from §8 to canonical refusal tooth.
- **HR keyword hard-stop:** **partially fails.** Conceptually present in §8 but missing verbatim hard-stop wording, complete trigger keyword categories, deterministic-gate rule.
- **Visible state header:** **fails.** Absent. Persona-bleed risk per §9.3 unaddressed.
- **Voice formatting contracts:** **partially fails.** Bracketed signals present; blockquote/Risk-Audit/code-block contracts absent.
- **Commitment artifact (`commitment_plan.md`):** **fails.** Artifact not named; format unspecified; 5 of 9 required elements missing.
- **Vagueness-gap detector:** **fails.** Absent.

---

## Summary verdict pattern

Both files are **MODIFY, not DISCARD**. They are high-quality pre-research drafts with strong voice/persona work, clean refusal-stance framing, and excellent failure-mode recovery language. The bones are the right shape. What they lack is **research-grade verbatim wording for refusal teeth, FRAMEWORK §7 HR hard-stop completeness, §9.3 persona-bleed mitigations (state header + formatting contracts), the §9.4 named commitment artifact, the §9.5 vagueness-gap detector, and full §3 intake gates**. They also carry **Manage Up scope that must be stripped** to fit tonight's MD-only floor.

## Single biggest salvage opportunity

The **persona/voice work in identity.md** (Jordan's bio, the four-voice rationale, the "what the coach refuses to become" list) and the **failure-mode recovery framing throughout rules.md** (§9 "Failure Modes to Watch" plus the Core Directive recovery instruction) are crisper than anything FRAMEWORK currently articulates. These should be **lifted verbatim** into the production spine — they would otherwise require new writing. Cleaning these salvageable assets buys back significant build time.

## Single biggest gap requiring rewrite

The **HR/legal hard-stop (R6)** is the most critical rewrite. These files treat HR escalation as a generic "if X happens, refer to escalation_and_safety.md" pointer (rules.md §8). FRAMEWORK §2 R6 + §7 require: a sixth canonical refusal tooth with verbatim `🚨 HR SENSITIVITY DETECTED` wording, a deterministic 8-category trigger keyword gate that prepends R6 before any other coaching, a separate soft-flag response for non-acute signals, and the explicit bound that the coach will not author disciplinary documentation. This is the highest-liability surface of the entire coach and the current spine is operationally insufficient on it. Rewrite from FRAMEWORK §2/§7 verbatim.
