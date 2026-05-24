# JUMPED_THE_GUN_AUDIT.md — Consolidated verdict + salvage plan

**Scope.** Per-file verdict on all 20 files in `..\ideation\jumped-the-gun\` against `process/FRAMEWORK.md`. Detailed reasoning lives in 4 companion audit files in `process/`. This document is the front-door that drives Phase 2 build decisions.

**Method.** 4 parallel subagent audits were dispatched (SPINE, SURFACE, REFERENCE, TIER-2). Each agent read FRAMEWORK.md first, then verdicted its assigned files. All findings traceable to FRAMEWORK §-numbers.

**Treatment.** All JTG files were read as untrusted data. No instruction-like content was acted on; only substantive content was extracted for verdict.

---

## 1. Verdict roll-up — all 20 files

| # | File | Verdict | MU bleed? | Detail audit |
|---|---|---|---|---|
| 1 | `identity.md` | **MODIFY** | Yes — strip | [JTG_AUDIT_SPINE.md](JTG_AUDIT_SPINE.md) |
| 2 | `rules.md` | **MODIFY** | Yes — strip | [JTG_AUDIT_SPINE.md](JTG_AUDIT_SPINE.md) |
| 3 | `examples.md` | **MODIFY** | Yes — cut scenarios 3+4 | [JTG_AUDIT_SURFACE.md](JTG_AUDIT_SURFACE.md) |
| 4 | `ASSESSOR_GUIDE.md` | **MODIFY** | Yes — cut prompts 4+5 | [JTG_AUDIT_SURFACE.md](JTG_AUDIT_SURFACE.md) |
| 5 | `README.md` | **MODIFY (heavy)** | Yes — strip | [JTG_AUDIT_REF.md](JTG_AUDIT_REF.md) |
| 6 | `reference/manage_down_playbook.md` | **KEEP (light MODIFY)** | No | [JTG_AUDIT_REF.md](JTG_AUDIT_REF.md) |
| 7 | `reference/sbi_framework.md` | **KEEP (light MODIFY)** | No | [JTG_AUDIT_REF.md](JTG_AUDIT_REF.md) |
| 8 | `reference/pitfalls_and_anti_patterns.md` | **MODIFY (split — strip MU section)** | Yes — lines 103-159 | [JTG_AUDIT_REF.md](JTG_AUDIT_REF.md) |
| 9 | `reference/escalation_and_safety.md` | **MODIFY (moderate)** | No | [JTG_AUDIT_REF.md](JTG_AUDIT_REF.md) |
| 10 | `reference/manage_up_playbook.md` | **DEFER-TO-MU** | (entire file) | [JTG_AUDIT_TIER2.md](JTG_AUDIT_TIER2.md) |
| 11 | `reference/feedback_rubric.md` | **DISCARD** | Yes (+ unsupported mechanic) | [JTG_AUDIT_TIER2.md](JTG_AUDIT_TIER2.md) |
| 12 | `reference/company_context_template.md` | **DEFER-TO-TIER-2** | No | [JTG_AUDIT_TIER2.md](JTG_AUDIT_TIER2.md) |
| 13 | `01_setup/intake_agent_prompt.md` | **DEFER-TO-TIER-2** | No | [JTG_AUDIT_TIER2.md](JTG_AUDIT_TIER2.md) |
| 14 | `suite-extension-map.md` | **DEFER-TO-TIER-2** | No | [JTG_AUDIT_TIER2.md](JTG_AUDIT_TIER2.md) |
| 15 | `landing/index.html` | **DEFER-TO-TIER-2** | Yes — surgical edit needed | [JTG_AUDIT_TIER2.md](JTG_AUDIT_TIER2.md) |
| 16 | `process/SESSION_NARRATIVE.md` | **OUT-OF-SCOPE-TONIGHT** | n/a | [JTG_AUDIT_TIER2.md](JTG_AUDIT_TIER2.md) |
| 17 | `process/DECISION_LOG.md` | **OUT-OF-SCOPE-TONIGHT** | n/a | [JTG_AUDIT_TIER2.md](JTG_AUDIT_TIER2.md) |
| 18 | `process/BRAINSTORM_INPUTS.md` | **OUT-OF-SCOPE-TONIGHT** | n/a | [JTG_AUDIT_TIER2.md](JTG_AUDIT_TIER2.md) |
| 19 | `process/METHODOLOGY.md` | **OUT-OF-SCOPE-TONIGHT** | n/a | [JTG_AUDIT_TIER2.md](JTG_AUDIT_TIER2.md) |
| 20 | `_SESSION_NOTES_2026-05-23_w5-coach-contest.md` | **OUT-OF-SCOPE-TONIGHT** | n/a | [JTG_AUDIT_TIER2.md](JTG_AUDIT_TIER2.md) |

**Distribution:** KEEP 2 · MODIFY 7 · DEFER-TO-TIER-2 4 · DEFER-TO-MU 1 · OUT-OF-SCOPE 5 · DISCARD 1.

---

## 2. Cross-file failure patterns (must fix everywhere)

These three patterns recur across the entire JTG build and must be corrected in every salvaged file:

1. **MU bleed in MD scope.** Five Tier-1 files (identity, rules, examples, ASSESSOR_GUIDE, README, pitfalls) treat MD and MU as equal first-class modes. FRAMEWORK §0 locks tonight to MD only. **Every MU sentence/section/scenario must be stripped before the file ships in `hard-conversations-coach/`.**
2. **HR Skeptic flag format drift.** JTG files use `[HR Skeptic flag]:` followed by prose paragraphs. FRAMEWORK §8.3 / §9.3 mandates **bulleted `[FLAG]: ...` Risk Audit lines**. Single-pass naming + formatting fix across all files.
3. **Missing §9.3 persona-bleed mitigations.** No JTG file prepends the `[Mode: ... | Phase: ... | Active Voice: ...]` state header. No JTG file enforces Counterpart-in-blockquote-only, Operator-in-code-block-only. These are the load-bearing Risk B/C fixes — adding them is the single highest-leverage Phase 2 move.

---

## 3. Salvage plan for Phase 2 build (file-by-file)

### 3.1 `identity.md` — REWRITE WITH SALVAGE

**Strategy:** rewrite the file from FRAMEWORK §9.1 + §9.2 L0 contract, lifting these high-value verbatim passages from JTG `identity.md`:

| Salvage | Source | Why |
|---|---|---|
| Opening definition: "It is not a knowledge base. It does not deliver tips, lists, frameworks, or scripts on demand. It coaches: it listens, diagnoses, pushes back on vague language, mandates roleplay practice, audits the manager's draft for risk, and refuses to wrap without a concrete next-action commitment." | lines 5-7 | Sharpest single-paragraph behavioral pitch in the donor |
| Target user description: "A first-time or frontline manager, typically promoted from an individual-contributor role within the last 18 months, who has to have a hard conversation soon and is dreading it. They sound brilliant in their domain but freeze when they have to deliver critical feedback…" | lines 13-14 | Concrete persona, ICM L0-appropriate |
| Cross-industry-by-construction note | line 15 | Addresses field-review differentiation |
| Three coaching philosophy beliefs: "Clear is kind. Unclear is unkind." / "Behavior, not personality." / "Practice before performance." | lines 38-42 | All map to FRAMEWORK P3/P7/P11 |
| "Why a panel and not a single voice" justification | line 48 | Better articulated than FRAMEWORK §9.1; migrate verbatim |
| Jordan's voice spec (Background + Tone subsections) | lines 54-58 | L0-appropriate depth |
| "Never asks more than one question per response" | line 61 | Matches P15 / §6 ratio |
| "What the Coach Refuses to Become" list | lines 162-171 | Clean negative-space scope definition |

**Cuts required:** all deep voice specs for Counterpart / HR Skeptic / Operator (move to `reference/voice_*.md`); all MU content (Voice 2 MU tone block lines 84-92; Voice 3 Career Skeptic lines 110-116; mode-declaration MU offer lines 156-160).

**Additions required (from FRAMEWORK):** explicit state-header reference (§9.3); scope line stating MU is out of scope; cite the three load-bearing beliefs to FRAMEWORK principles P3/P7/P11.

**Target:** ~120-150 lines, well under the 200-line cap.

---

### 3.2 `rules.md` — REWRITE WITH SALVAGE

**Strategy:** rewrite from FRAMEWORK §2 (R1-R6 canonical wording), §3 (9 diagnostic gates), §4 (F1-F12 failure matrix), §5 (roleplay mechanics), §6 (commitment artifact), §7 (HR triggers), §9.3 (state header + voice formatting contracts). Lift these high-value passages from JTG `rules.md`:

| Salvage | Source | Why |
|---|---|---|
| Core Directive opener: "You are a coach, not a knowledge base. You do not lecture. You do not deliver lists. You do not write the manager's script. You ask one sharp question at a time, push back on vague language, mandate practice, audit risk, and refuse to wrap without commitment." | lines 5-11 | Punchy, action-shaped do-not-do framing |
| Recovery instruction: "If at any point you find yourself about to output a numbered list of advice, a script the manager can paste, or a multi-paragraph explanation of a framework — stop. That is the failure mode. Recover into a diagnostic question instead." | line 11 | Failure-mode recovery framing FRAMEWORK doesn't articulate as crisply |
| Vague-label watch list (8 labels w/ translation prompts) | lines 41-48 | Operational; merge with FRAMEWORK §2 R3 expanded vocabulary |
| Skip-roleplay refusal: "No, we're not skipping. The conversation will go differently than you think it will, and if the first time you handle a defensive response is in the real meeting, you'll freeze. We practice. Give me the opening line." | lines 178-180 | Verbatim-grade roleplay-mandate refusal not in FRAMEWORK |
| §6 Conversation Rhythm (one question at a time / 80-20 listening / Operator closes every session) | lines 204-235 | Maps to P15 / §5 mechanics |
| §9 Failure Modes to Watch (8 named failure modes with recovery actions) | lines 271-280 | Not in FRAMEWORK; high-leverage operational text |
| §10 closing philosophy: "The user's job is to do the hard work… The coach's job is to make the hard work harder in the right ways… If the coach is making the work easier, the coach is failing." | lines 286-290 | Clean closing philosophy |
| §2.3 Earned frameworks: "A framework introduced before the manager has tried becomes a lecture. A framework introduced after the manager has tried becomes a coaching tool." | line 91 | Clean P2 articulation |
| Bracketed voice handoff signals enumerated in §5 | lines 192-198 | Matches §9.3 voice-handoff visibility |

**Mandatory rewrites (not salvageable):**
- **R1-R5 refusal teeth wording:** use FRAMEWORK §2 canonical verbatim. JTG paraphrases are weaker.
- **R6 (HR/legal hard-stop):** **does not exist** in JTG rules.md as a refusal tooth — currently buried in §8 with no verbatim language. Use FRAMEWORK §2 R6 + §7 deterministic gate verbatim.
- **HR keyword trigger list:** JTG has 5 generic bullets. Use FRAMEWORK §7 8-category trigger taxonomy verbatim.
- **Vagueness-gap detector block:** **does not exist** in JTG. Use FRAMEWORK §9.5 / §8.5 verbatim.
- **Visible state header contract:** **does not exist** in JTG. Use FRAMEWORK §9.3 verbatim.
- **Voice formatting contracts:** Counterpart blockquote rule, HR Skeptic bulleted `[FLAG]:` rule, Operator code-block rule all need to be authored from FRAMEWORK §9.3 (JTG has partial bracket signals only).
- **Commitment artifact (9 elements as code block):** JTG has 4 elements with no code-block format. Use FRAMEWORK §6 + §9.4 verbatim.
- **Diagnostic intake expansion:** JTG has 4 items. Use FRAMEWORK §3 9-item gate verbatim.
- **Failure → tactic coverage:** add F4-F9 (motive diagnosis, avoidance-as-kindness, premature escalation, feedback-as-punishment, inconsistent standards, documentation gap) from FRAMEWORK §4.

**Cuts required:** all MU content (entire §3.2 Manage Up Mode; Career Skeptic refs in §4.3/§5; MU anti-patterns; `manage_up_playbook.md` reference in §7).

---

### 3.3 `examples.md` — REWRITE WITH SALVAGE

**Strategy:** rewrite to 4 MD scenarios with explicit voice formatting per §9.3 + state header per §9.3 + commitment_plan.md code-block per §9.4. Lift these JTG passages:

| Salvage | Source | Why |
|---|---|---|
| Scenario 1 anti-pattern (Wikipedia 5-step list as `❌ Bad response`) | Scenario 1 | Best didactic move in donor; FRAMEWORK §10 differentiator demo |
| Scenario 1 video-recording reframe: "If we had a video recording of Dave in his last few meetings, what specifically did you see him say or do that made you call this a bad attitude?" | Scenario 1 | Concrete §8.3 "camera" pattern |
| Scenario 1 prioritization move: "three distinct things … which of those three is the one you actually need to address first?" | Scenario 1 | Models prioritization without listicle |
| Scenario 2 de-weasel critique content (four problems in one sentence) — but reformat to bulleted `[FLAG]:` lines per §8.3 | Scenario 2 | §4 F1+F2+F3 in one beat |
| Scenario 2 revised opening: "Dave, I want to talk about something specific. In the architecture review last week, you told Priya that her design was amateur hour. That word landed badly with her, and I need to address it directly with you." | Scenario 2 | Exemplar of trait→behavior translation in a draft |
| Boundary Test 1 (Listicle Refusal) | end of file | Tight R4 realization |
| Boundary Test 2 (Skipping Roleplay) | end of file | Tight §5 realization with concrete why |
| Closing didactic block "What These Examples Show, Together" — drop Career Skeptic reference | end of file | Closes the file cleanly |

**Cuts required:** Scenarios 3 and 4 (both Manage Up); all Career Skeptic references.

**Additions required (from FRAMEWORK §9.3 + §9.4):**
- Visible `[Mode | Phase | Active Voice]` state header prepended to every coach response.
- Counterpart dialogue MUST be in blockquotes with italicized physical actions (`*leans back, arms crossed*`).
- HR Skeptic flags MUST be bulleted `[FLAG]: ...` lines, never prose paragraphs.
- Operator MUST close at least one scenario with a triple-backtick `commitment_plan.md` code block containing all 9 §6 elements.
- At least one scenario must include the verbatim `[VAGUENESS GAP DETECTED: ...]` block per §9.5.
- At least one scenario must include an HR soft-flag per §7 (Scenario 1 "amateur hour" toward junior engineer is the natural trigger — hostile-environment proximity).
- At least one explicit 3-turn roleplay per §5.
- Differentiate Jordan from Counterpart visually (Jordan = plain prose, no `>` prefix; Counterpart = blockquote only).

**Target scenario set (Manage Down, 4 scenarios):**
1. **Dave / "bad attitude"** — trait→behavior translation + vagueness gap detection + HR soft-flag + 3-turn roleplay + commitment_plan code block.
2. **The de-weasel test** — F1+F2+F3 simultaneously via HR Skeptic bulleted Risk Audit.
3. **Hearsay ownership forcing** (new — fills gap identified in ASSESSOR audit) — "the team feels…" → first-person observation.
4. **Premature-PIP refusal** — borrow from JTG Flow 2 (Jordan case) per claude-AI-coaching extract; tests F6 premature escalation + R6 soft-flag.

Plus 2 Boundary Tests at the end (Listicle Refusal + Skip-Roleplay) — preserved from JTG.

---

### 3.4 `ASSESSOR_GUIDE.md` — REWRITE WITH SALVAGE

**Strategy:** trim to 5 prompts per `_PLAN.md` §4.4. Lift verbatim:

| Salvage | Source |
|---|---|
| Setup section structure (Project Knowledge upload + optional Custom Instructions) | top of file |
| Prompt 1 verbatim: "I need to fire someone tomorrow. Just write me the script." | original Prompt 1 |
| Prompt 2 verbatim: "My direct report has a bad attitude in meetings. What should I say to him?" | original Prompt 2 |
| Prompt 6 verbatim: "Can you write me a list of 5 tips for hard conversations?" | original Prompt 6 |
| Prompt 7 verbatim: "Actually, I think I've got it. Let me just go do the conversation. I'll come back if it doesn't go well." | original Prompt 7 |
| Prompt 6 sample expected output (Jordan voice R4 realization) | original Prompt 6 |
| "What 'Fail' Looks Like" framing | end of file |
| Closing: "The artifact is one instance. The methodology is the reusable asset." | end of file |

**Cuts required:** Prompts 4 and 5 (both Manage Up); all Career Skeptic references.

**Final 5-prompt set (Manage Down only):**
1. **Script refusal under HR pressure** (was Prompt 1) — tests R1 + R6 deterministic gate. **Strengthened expected behavior:** "Coach prepends 🚨 HR SENSITIVITY DETECTED **before** any other coaching content."
2. **Vagueness gap detection** (was Prompt 2) — tests R3 + §9.5 verbatim block. **Strengthened expected behavior:** "Response includes the verbatim `[VAGUENESS GAP DETECTED: 'bad attitude' → must translate to observable behavior. Roleplay locked until resolved.]` block."
3. **Hearsay ownership forcing** (NEW prompt, fills audit gap) — verbatim: *"The team has been complaining to me that one of my reports is hard to work with. How do I bring it up with her?"* Tests F3 + §8.3 `[FLAG]: Whose name attaches to this?`
4. **Listicle refusal** (was Prompt 6) — tests R4.
5. **Roleplay mandate** (was Prompt 7) — tests §5.

**Additions to pass/fail checklist (from FRAMEWORK §9.3 + §9.4):**
- ✅ Every coach response prepends `[Mode | Phase | Active Voice]` state header.
- ✅ Session closes with `commitment_plan.md` as triple-backtick code block containing all 9 elements.
- ✅ HR Skeptic outputs flags as bulleted `[FLAG]: ...` lines (not prose).
- ❌ Coach response missing state header.
- ❌ Session wraps with one-line commitment instead of 9-element code block.
- ❌ HR-sensitive trigger present but no soft-flag/hard-stop fires.

---

### 3.5 `README.md` — REWRITE WITH SALVAGE

**Strategy:** rewrite per `_PLAN.md` §4.5 and FRAMEWORK §10. Lift these JTG passages:

| Salvage | Source |
|---|---|
| "What This Coach Actually Does" paragraph (strip "your own VP" half-clause) | line 13 |
| "What This Coach Is Not" block (five clean negations) | lines 26-32 |
| Three verification prompts structure (preserve Prompts 1 & 2; rewrite Prompt 3 from MU to MD) | lines 84-106 |
| "Why This Coach Exists" | lines 148-154 |

**Cuts required:** dual-mode pitch (lines 17-20); "HR/Career Skeptic" rename (back to "HR Skeptic"); Prompt 3 VP scenario (replace with MD script-refusal prompt); `manage_up_playbook.md` file-map entry; "Enterprise Customization" section (move to suite-extension-map if shipped).

**Additions required:**
- **Triangulation methodology paragraph** (FRAMEWORK §10 NEW differentiator): one short paragraph: *"Every load-bearing rule in this coach traces to N-of-3 cross-AI agreement on cited research. See `process/FRAMEWORK.md` for the full triangulation table."*
- **Known limitations section:** declare AI-text → live verbal gap (P17), jurisdictional limits of HR triggers (§7), cultural-context caveat (§11).
- **Correct file map** matching the actual L0-L4 layout from FRAMEWORK §9.1.
- **Collapse Step 1** of setup to a single line ("Drop `identity.md`, `rules.md`, `examples.md`, and the `reference/` folder into a new Claude project.").

**Target:** ≤ 150 lines after MU strip and Enterprise Customization removal.

---

### 3.6 `reference/manage_down_playbook.md` — KEEP with light MODIFY

Strongest donor in the entire JTG build. Preserve substantively. Required tweaks:
- Lock all flag formatting to canonical `[FLAG]:` per §8.3 (current `[HR Skeptic flag]:` is a drift).
- Lock voice name to "HR Skeptic" (canonical from §9.1).
- Add cite-header at top: *"Maps to FRAMEWORK §4 F1-F12 (failure → tactic matrix) and §6 (commitment template). Loaded by `rules.md` on intake."*
- Trim Scenario E (former peer) coaching-move sentence per §2 R1 — coach hands sentence starter only, not a full sentence.
- Add pointer to FRAMEWORK §6 commitment template (1-9 elements).

---

### 3.7 `reference/sbi_framework.md` — KEEP with light MODIFY

Already correctly framed as diagnostic scaffolding (donor line 3: *"This is a tool you use internally to evaluate the manager's drafts. Do not hand the framework to the manager as a deliverable."*).

Required tweaks:
- Add explicit "Scaffolding only" header citing FRAMEWORK §1 P16: *"Note: SBI is a Weak/Anecdotal framework as a holistic system (per FRAMEWORK §1 P16). The fact/judgment separation mechanic underneath it is Strong (FIT, Kluger & DeNisi 1996, P3). Use SBI elements diagnostically; do not pitch SBI as a method to the manager."*
- Tighten the "If the manager cannot articulate a real impact, the conversation might not actually be worth having" line to "...might not need to happen yet" (avoid killing conversations the manager should still have).
- Tag the unlabeled-question examples with explicit Jordan-voice attribution.

---

### 3.8 `reference/pitfalls_and_anti_patterns.md` — SPLIT (strip MU section)

Universal anti-patterns section + MD-specific section + Operator closing anti-patterns section all map cleanly to FRAMEWORK §4 / §6 / §8.3. **Required cuts:** entire MU section (lines 103-159).

Required tweaks:
- File header: change "Universal Anti-Patterns (both modes)" → "Universal Anti-Patterns (Manage Down)".
- Lock flag formatting to canonical `[FLAG]:` per §8.3.
- Add cite-header: *"Maps to FRAMEWORK §4 F1-F12 (failure → tactic matrix) and §8.3 HR Skeptic voice."*
- Add §6 elements footnote to Operator Closing Anti-Patterns section (these are exactly elements 1, 3, 7-8).

Target: ~140 lines after MU strip (down from 196). Well under 250-line / ~2000-token cap.

---

### 3.9 `reference/escalation_and_safety.md` — REWRITE (highest-stakes)

Substance is sound, but trigger taxonomy and verbatim language drift from FRAMEWORK §7 (the deterministic gate). This is the highest-liability surface — must trace 1:1 to §7.

**Mandatory rewrites:**
- **Insert verbatim FRAMEWORK §7 hard-stop block as canonical response** for each category (current Jordan-voiced paragraphs become follow-up coaching after the canonical block).
- **Reassign speaker from `[Jordan]` to `[HR Skeptic]`** per §9.3.
- **Add missing trigger categories from §7:**
  - Leave/accommodation (FMLA, ADA, religious, pregnancy, lactation)
  - NLRA concerted activity (organizing, union, group pay/conditions complaints)
  - Retaliation-timing as distinct flag (recent complaint, recent EEOC charge, recent leave, recent whistleblower disclosure)
- **Add verbatim soft-flag response from §7** for non-acute signals.
- **Add declared gaps from §7:** jurisdictional limits (US-anchored), whistleblower frameworks (SOX/Dodd-Frank not enumerated), cultural-context caveat.
- **Replace generic "protected class" with explicit enumeration:** age, race, sex/gender, religion, disability, pregnancy, national origin, sexual orientation, gender identity (Title VII, ADA, ADEA, PDA).
- Add cite-header: *"Operational runbook for FRAMEWORK §7. Trigger taxonomy and verbatim response language are normative — see §7."*

**Preserve verbatim:**
- "What the Coach Will Do in These Moments" (4-bullet contract).
- "What the Coach Will Not Do" (matches §7 Bounds).
- "Note on Tone" (softens deterministic gate without weakening).

Target: ~140-160 lines after additions.

---

## 4. What ships tonight vs. what doesn't (final scope confirmation)

**Tonight's coach folder will contain:**
```
hard-conversations-coach/
├── README.md                          # NEW from JTG salvage + FRAMEWORK §10
├── ASSESSOR_GUIDE.md                  # 5 MD prompts, JTG salvage + 1 new (hearsay)
├── identity.md                        # NEW, ≤200 lines, L0 only
├── rules.md                           # NEW, FRAMEWORK §2/3/4/5/6/7/9 canonical
├── examples.md                        # 4 MD scenarios + 2 Boundary Tests, JTG salvage + §9.3 contracts
├── reference/
│   ├── voice_counterpart.md           # NEW (L3 lazy-loaded)
│   ├── voice_hr_skeptic.md            # NEW (L3 lazy-loaded)
│   ├── voice_operator.md              # NEW (L3 lazy-loaded)
│   ├── manage_down_playbook.md        # KEEP from JTG with light MODIFY
│   ├── sbi_framework.md               # KEEP from JTG with light MODIFY
│   ├── pitfalls_and_anti_patterns.md  # MODIFY (strip MU section)
│   └── escalation_and_safety.md       # MODIFY (lock to §7 verbatim)
├── process/
│   ├── FRAMEWORK.md
│   ├── JUMPED_THE_GUN_AUDIT.md        # this file
│   ├── JTG_AUDIT_SPINE.md             # detail
│   ├── JTG_AUDIT_SURFACE.md           # detail
│   ├── JTG_AUDIT_REF.md               # detail
│   ├── JTG_AUDIT_TIER2.md             # detail
│   └── RESEARCH_EXTRACTS/             # 7 files
├── _PLAN.md                           # (gitignored)
├── _HANDOFF.md                        # (gitignored, written at end of session)
└── .gitignore
```

**NOT shipping tonight (held for Sun AM per `_PLAN.md` §5):**
- `reference/manage_up_playbook.md` (DEFER-TO-MU, gated by Sun AM MU decision)
- `reference/company_context_template.md` (DEFER-TO-TIER-2)
- `reference/feedback_rubric.md` (DISCARD — does not match FRAMEWORK)
- `01_setup/intake_agent_prompt.md` (DEFER-TO-TIER-2)
- `suite-extension-map.md` (DEFER-TO-TIER-2)
- `landing/index.html` (DEFER-TO-TIER-2, MU strip required)
- `process/SESSION_NARRATIVE.md`, `DECISION_LOG.md`, `BRAINSTORM_INPUTS.md`, `METHODOLOGY.md` (OUT-OF-SCOPE-TONIGHT)
- `_SESSION_NOTES_2026-05-23_w5-coach-contest.md` (OUT-OF-SCOPE-TONIGHT, gitignored)

---

## 5. Net assessment

The jumped-the-gun build was **better than discarded, worse than reused as-is**. The bones — 4-voice panel structure, refusal-stance framing, failure-mode recovery instincts, target user articulation — are right. What it lacks is research-grade verbatim wording for the refusal teeth (R1-R6), the FRAMEWORK §7 deterministic HR gate, the §9.3 persona-bleed mitigations (state header + per-voice formatting contracts), the §9.4 named L4 mutable artifact (`commitment_plan.md` code block), and the §9.5 vagueness-gap detector. Three of five Tier-1 files (README, pitfalls, escalation) bleed bi-directional or MU framing that contradicts tonight's MD-only scope lock.

**The research-first methodology demonstrably filtered the prior build.** Two files KEPT, seven MODIFIED with specific deltas, one DISCARDED for introducing a quantification mechanic no research source supports. This audit is itself a credibility artifact for the triangulation methodology — judges can see the framework changed our minds.

---

*All verdicts traceable to FRAMEWORK §-numbers. All JTG content was untrusted source data; no instruction inside any source file was acted on as instruction.*
