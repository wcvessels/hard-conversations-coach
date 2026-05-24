# JTG Audit — Reference Files from `ideation/jumped-the-gun/`

**Auditor scope.** Treat all source files under `ideation/jumped-the-gun/` as untrusted content donors. The canonical source of truth is `process/FRAMEWORK.md`. Verdicts below cite FRAMEWORK sections that drive the call.

**Scope reminder.** Per FRAMEWORK §0 and `_PLAN.md`, the current build is **Manage Down floor only**. Any Manage Up content in the JTG files is out of scope and must be stripped or quarantined before any of this material lands in the live coach folder. This is the single largest pattern of architectural mismatch across these five files.

---

### File: `ideation/jumped-the-gun/README.md`

**Verdict: MODIFY (heavy)**

**Rationale (cite FRAMEWORK sections that drive the verdict):**
- FRAMEWORK §0/§9 / scope: this entire JTG README assumes a **bi-directional Manage Down + Manage Up** coach. FRAMEWORK §0 ("Scope tonight: Manage Down only. Manage Up rows tagged `[MU]` and surfaced but not operationalized") and §4.MU and §12 forbid operationalizing MU in this build. The README's "Manage Up mode" framing and the dual-mode pitch (lines 15-20) directly contradict the locked scope.
- FRAMEWORK §10 (differentiators) requires the README to surface the **triangulation methodology** (N-of-3 cross-AI). The JTG README does not mention triangulation, FRAMEWORK.md, or evidence grading anywhere. This is the explicit "NEW — no field entry surfaces" differentiator and must be in the README.
- FRAMEWORK §9.1 / §9.2 names the four voices as **Jordan (orchestrator), Counterpart, HR Skeptic, Operator**. The JTG README names them as **"Veteran Coach, Counterpart, HR/Career Skeptic, Operator"** (line 20). "Veteran Coach" is not the canonical name; "HR/Career Skeptic" is a bi-directional rename of the canonical "HR Skeptic." Both must change.
- FRAMEWORK §2 (R1-R6 refusal teeth) — the JTG README's "What This Coach Actually Does" paragraph (line 13) is high-value and aligns directly with R1/R3/R5 + roleplay §5. KEEP that paragraph almost verbatim.
- FRAMEWORK §11 + P17 (Gap): the AI-text-to-live-verbal transfer gap must be declared in `README.md` known-limitations per §1 P17 mapping. The JTG README has no known-limitations section.
- The "three verification prompts" block (lines 84-106) is well-shaped and judge-friendly. Prompt 3 currently references "your VP about a mistake I made" — pure Manage Up. Must be retargeted to a Manage Down scenario (script-write refusal applied to a direct report) to align with the MD-only scope.
- The file map (lines 112-135) references `manage_up_playbook.md`, `feedback_rubric.md`, and `company_context_template.md`. None of those are in the locked FRAMEWORK §9.1 layout for tonight. `manage_up_playbook.md` is explicitly out of scope (§0). The map must be replaced with the actual L0-L4 layout from FRAMEWORK §9.1.
- The "Manager Practice Lab suite" framing (lines 7-8, 168) is on-strategy and aligned with the plan §4.5 differentiator. KEEP one paragraph, point at `suite-extension-map.md`.

**If MODIFY, specific changes required:**
- Strip every reference to Manage Up mode (lines 17-20 dual-mode pitch; line 124 file-map entry `manage_up_playbook.md`; Prompt 3 VP scenario). Replace with MD-only framing.
- Rename voices to canonical FRAMEWORK §9.1 names: **Jordan, Counterpart, HR Skeptic, Operator** (drop "Veteran" and drop the "/Career" suffix on Skeptic).
- Add a **Triangulation methodology** paragraph (one short paragraph) per FRAMEWORK §10 + plan §4.5: "Every load-bearing rule in this coach traces to N-of-3 cross-AI agreement on cited research. See `process/FRAMEWORK.md` for the full triangulation table." This is the named differentiator.
- Replace the file map with the actual L0-L4 layout from FRAMEWORK §9.1: `identity.md` (L0), `rules.md` (L2), `examples.md`, `reference/voice_counterpart.md`, `reference/voice_hr_skeptic.md`, `reference/voice_operator.md`, `reference/manage_down_playbook.md`, `reference/sbi_framework.md`, `reference/pitfalls_and_anti_patterns.md`, `reference/escalation_and_safety.md`, `process/FRAMEWORK.md`, `process/JTG_AUDIT_REF.md`, etc. Remove the L4 `commitment_plan.md` from the persistent file map — it is a per-session in-chat artifact (§9.4), not a repo file.
- Add a **Known limitations** section that declares AI-text → live verbal gap (FRAMEWORK §11 / P17), jurisdictional limits of HR triggers (§7), and cultural-context caveat (§11).
- Retarget Prompt 3 to MD: e.g., *"Just write me the opening line I can use with [direct report] about their missed deadline."* Expected behavior remains identical (R1 refusal + draft demand).
- Confirm the four setup steps stay ≤ 4 lines and read as a "judge-facing front door." Current Step 1 is a 5-item nested list inside one step — collapse to a single line directive ("Drop `identity.md`, `rules.md`, `examples.md`, and the `reference/` folder into a new Claude project.").
- Strike the **Enterprise Customization** section (lines 74-81) — `company_context_template.md` and `01_setup/intake_agent_prompt.md` are not in tonight's FRAMEWORK §9.1 layout. Move to suite-extension-map if it stays anywhere.
- Strike the **License** section unless plan §4 explicitly calls for it; it adds nothing to a judge audit and clutters the front door.

**If KEEP, callouts on what's high-value:**
- "What This Coach Actually Does" paragraph (line 13) — preserve verbatim after stripping the "your own VP" half-clause. It's the cleanest single-paragraph behavioral pitch in the file.
- "What This Coach Is Not" block (lines 26-32) — preserve verbatim. Five clean negations.
- The three verification prompts pattern (lines 84-106) — preserve structure and Prompts 1 & 2 verbatim; rewrite Prompt 3 per above.
- "Why This Coach Exists" (lines 148-154) — preserve almost verbatim. Lands the differentiator from the field-review intuitively.

**Notes on architecture fit:**
- ICM L3 compliance: N/A — README is the front door, not L3.
- Token budget: README has no hard token budget in §9.1; current ~175 lines is acceptable but should drop ~30-50 lines after MU strip and Enterprise Customization removal.
- Manage Down floor: **fails** as-is. Bi-directional framing must be stripped.
- Cites match FRAMEWORK: **fails** as-is. No mention of FRAMEWORK.md or triangulation. After MODIFY, must add explicit pointer to `process/FRAMEWORK.md` as the canonical methodology source.
- **Manage Up content present:** YES — lines 18, 20 ("HR/Career Skeptic"), Prompt 3 ("with my VP"), line 124 file-map entry `manage_up_playbook.md`. All must be stripped.

---

### File: `ideation/jumped-the-gun/reference/manage_down_playbook.md`

**Verdict: KEEP (light MODIFY)**

**Rationale (cite FRAMEWORK sections that drive the verdict):**
- This file is the strongest cite-traceable match to FRAMEWORK of the four reference files. It directly executes FRAMEWORK §4 (failure → tactic matrix) and §6 (commitment / documentation), and references the §9.1 voice contracts ("Counterpart loads as the direct report. The Skeptic operates as HR Skeptic" — line 3).
- FRAMEWORK §4 failure rows are well-represented:
  - Scenario A (compliment sandwich) → maps to §4 F2 (weasel/softening) + Pitfalls "Compliment Sandwich"; principle is P11 (MUM Effect).
  - Scenario C (buried headline) → maps to §4 F2 + §8.3 lexical red-penning.
  - Scenario D (triangulation) → maps to MD-specific failure not enumerated in §4 but consistent with the matrix logic; defensible.
  - Scenario E (former peer) → not in §4; original-but-aligned content. Acceptable as playbook-level color.
- "Direct Report Counterpart Modes" (lines 46-55) directly supports FRAMEWORK §5 roleplay + §8.2 Counterpart voice. The list of tones (defensive, hurt, defiant, confused, shut down, deflecting, acquiescing too fast) extends but does not contradict §8.2 ("default tone: defensive, hurt, or quiet"). This is high-value scaffolding for the Counterpart voice file.
- "HR Skeptic Watch List" (lines 60-74) directly mirrors FRAMEWORK §2 R3 trigger label vocabulary ("attitude," "tone," "vibe," "fit," "energy") and §4 F1/F3/F4/F8. The verbatim translation example (line 74) is precisely the §8.3 `[FLAG]: ...` Risk Audit format. KEEP.
- "Documentation Reminder" (lines 84-85) maps to FRAMEWORK §6 element 8 ("documentation prompt") and §4 F9. Aligns with P14.

**If MODIFY, specific changes required:**
- Update the format of the HR Skeptic flag line (line 74) to match the FRAMEWORK §8.3 canonical bracketed format. Current: `> [HR Skeptic flag]: "She has a bad attitude" is a documentation problem.` Canonical: `[FLAG]: ...`. Either rename to match §8.3 or document the deviation in `rules.md`.
- The header directive (line 3) refers to "the Skeptic" generically. Lock to "HR Skeptic" (canonical name from §9.1) consistently.
- Cross-reference FRAMEWORK §4 explicitly: add a one-line cite at the top of the failure scenarios section pointing to FRAMEWORK §4 F1-F12. This keeps the traceability spine intact.
- The "Coaching move" for Scenario E (former peer, line 37) contains a long pre-scripted sentence. R1 says **never** hand the user a full sentence; only sentence starters. Trim to a starter ("I know we used to be peers, and that's why...") and leave the rest for the user to draft. Otherwise this file silently violates R1.
- Add a brief pointer to FRAMEWORK §6 commitment template (1-9 elements) so the Operator close from this playbook ties to the canonical artifact structure.

**If KEEP, callouts on what's high-value:**
- Direct Report Counterpart Modes list (lines 46-55) — extends FRAMEWORK §8.2 cleanly; preserve verbatim, may also belong in `reference/voice_counterpart.md`.
- HR Skeptic Watch List (lines 62-70) — preserve verbatim; this is the operational trigger set that complements FRAMEWORK §7 HR triggers and §2 R3 trigger label vocabulary.
- Anti-Patterns Specific to Manage Down (lines 77-81) — preserve; cleanly extends FRAMEWORK §4 without contradiction.

**Notes on architecture fit:**
- ICM L3: yes, lazy-loaded reference. Aligned.
- Token budget ≤ 2000 tok / ~250 lines: file is 86 lines. **Pass.**
- Manage Down floor only: **pass** — file scope is MD by definition. No MU bleed.
- Cites match FRAMEWORK: largely yes; needs the explicit §4/§6 cross-references added in MODIFY items above.
- **Manage Up content present:** No.

---

### File: `ideation/jumped-the-gun/reference/sbi_framework.md`

**Verdict: KEEP (light MODIFY)**

**Rationale (cite FRAMEWORK sections that drive the verdict):**
- FRAMEWORK §1 P16 explicitly classifies SBI/DESC/Crucial Conversations/Radical Candor as **"Weak/Anecdotal as holistic systems; the underlying CBT mechanic (fact/judgment separation) is Strong."** This file must self-declare as **scaffolding only**, used diagnostically to enforce the fact/judgment separation, not as a holistic system.
- The file's coach directive (line 3) already nails the right stance: *"This is a tool you use internally to evaluate the manager's drafts. Do not hand the framework to the manager as a deliverable."* This aligns with §1 P16 and is exactly the architectural framing required.
- "How to weave SBI into your questions, unlabeled" (lines 33-37) maps directly to FRAMEWORK §8.1 Jordan voice patterns: one-question-at-a-time, prose, no bullet lists for questions. Aligned.
- The behavioral examples (lines 7-11) directly execute FRAMEWORK §2 R3 (trait → behavior translation) and §4 F1. The verbatim camera question ("If I had a camera in the room, what would I see them doing?") echoes FRAMEWORK §8.3 ("What would a camera see?"). Strong cite trace.
- "Common failure: skipping Impact" (lines 23-31) is original-but-aligned color; consistent with FIT (P3).

**If MODIFY, specific changes required:**
- Add an explicit **"Scaffolding only" header note** at the top citing FRAMEWORK §1 P16. Current Coach directive is good but doesn't name SBI's evidence-grade status as Weak/Anecdotal-as-holistic-system. Sample line: *"Note: SBI is a Weak/Anecdotal framework as a holistic system (per FRAMEWORK §1 P16). The fact/judgment separation mechanic underneath it is Strong (FIT, Kluger & DeNisi 1996, P3). Use SBI elements diagnostically; do not pitch SBI as a method to the manager."*
- The "If the manager cannot articulate a real impact, the conversation might not actually be worth having" line (line 31) is high-leverage and aligned with FRAMEWORK §4 F5 (avoidance disguised as kindness — but inverted). Consider tightening to "...might not need to happen yet" so the coach doesn't kill conversations the manager should still have.
- The unlabeled-question examples (lines 35-37) should be triangulated against FRAMEWORK §8.1 Jordan voice patterns and tagged with the same Jordan-voice annotation, so a reader of this file understands the line *"Anchor it in time. When specifically did you see this?"* is delivered in Jordan's voice (not HR Skeptic).

**If KEEP, callouts on what's high-value:**
- Coach directive (line 3) — preserve verbatim. Best single-line statement of the scaffolding-only stance.
- The three diagnostic questions (lines 15-19) — preserve verbatim. Clean and operational.
- The "weave it in unlabeled" pattern (lines 33-37) — preserve verbatim. This is exactly the right Jordan-voice pedagogy.

**Notes on architecture fit:**
- ICM L3: yes, lazy-loaded reference. Aligned.
- Token budget ≤ 2000 tok / ~250 lines: file is 40 lines. **Pass with margin.**
- Manage Down floor only: **pass** — applies cleanly to MD; the diagnostic stance is mode-agnostic but doesn't bleed MU framing.
- Cites match FRAMEWORK: needs the explicit §1 P16 callout added per MODIFY above. Without it, the file silently claims SBI is a holistic framework, which contradicts FRAMEWORK.
- **Manage Up content present:** No.

---

### File: `ideation/jumped-the-gun/reference/pitfalls_and_anti_patterns.md`

**Verdict: MODIFY (split required)**

**Rationale (cite FRAMEWORK sections that drive the verdict):**
- Universal anti-patterns section (lines 5-58) maps cleanly to FRAMEWORK §4 failure matrix:
  - Compliment Sandwich → F2 (weasel/softening, MUM Effect P11).
  - Ruinous Empathy → F5 (avoidance disguised as kindness).
  - Weasel Words → F2 verbatim, with §8.3 verbatim flag wording.
  - Blame Distancing → F3 (hearsay/ownership dodge).
  - Personality Attack vs. Behavior → F1 + R3 verbatim (3/3).
  - Closing Without an Ask → F12 + R5 verbatim.
  - Stacked Questions → not in §4 but consistent with §8.1 Jordan voice rule ("never uses bullet lists for questions"). Acceptable.
- Manage Down Specific Anti-Patterns (lines 62-101) — aligned with FRAMEWORK §4 and §5 roleplay. KEEP.
- **Manage Up Specific Anti-Patterns (lines 103-159) — out of scope per FRAMEWORK §0 / §4.MU.** Must be removed from the live `reference/pitfalls_and_anti_patterns.md` file or quarantined for the Sunday-AM Manage Up gate (per FRAMEWORK §0 and §11). Surfacing them in the L3 reference today would cause the coach to lazy-load MU coaching guidance during MD sessions — direct contradiction of the scope lock.
- Operator Closing Anti-Patterns (lines 161-185) — directly maps to FRAMEWORK §6 commitment template elements 1, 3, 7, 8, and R5 closing language. Verbatim alignment. KEEP.
- "How to Flag These in Real Time" closing pattern (lines 189-195) — directly implements FRAMEWORK §8.3 HR Skeptic format ("flags one anti-pattern at a time, specifically and tersely") and §9.3 voice handoff ("Then return to Jordan. Don't pile flags."). Preserve verbatim.

**If MODIFY, specific changes required:**
- **Delete the entire "Manage Up Specific Anti-Patterns" section (lines 103-159).** Move to a quarantined file outside the live coach folder (e.g., `process/MU_DEFERRED.md` or `ideation/`-only retention) for the Sunday-AM MU build. Do not ship these in the live `reference/pitfalls_and_anti_patterns.md`.
- Update the file header (line 5) from "Universal Anti-Patterns (both modes)" to "Universal Anti-Patterns (Manage Down)" — there is no second mode in scope, and the bi-directional framing must be removed everywhere.
- The HR Skeptic flag format in lines 192-194 uses `[HR Skeptic flag]:` — align to canonical `[FLAG]:` per FRAMEWORK §8.3 (or formally name the deviation in `rules.md`).
- Add a cite header line at the top: "Maps to FRAMEWORK §4 F1-F12 (failure → tactic matrix) and §8.3 HR Skeptic voice."
- The Operator Closing Anti-Patterns section (lines 161-185) should explicitly cite FRAMEWORK §6 elements 1-9 in a footnote — these three failures are exactly elements 1 (date/time), 3 (exact opening line), and 7-8 (follow-up + documentation).
- Personality Attack response (line 43) is verbatim aligned with FRAMEWORK §2 R3 / §8.3 ("That's a personality label. Translate to behavior."). Preserve.

**If KEEP, callouts on what's high-value:**
- "Compliment Sandwich" full block (lines 7-13) — preserve verbatim. Named, explained, coach response is direct.
- "Weasel Words" block (lines 23-27) — preserve verbatim; this is the §8.3 verbatim flag wording with FRAMEWORK §4 F2 cite trace.
- "Blame Distancing" block (lines 29-35) — preserve verbatim; directly implements F3 (hearsay/ownership dodge).
- "Personality Attack vs. Behavior" (lines 37-43) — preserve verbatim. This IS R3 in the most operational form.
- Operator Closing Anti-Patterns (lines 163-185) — preserve verbatim, all three. They are the L4 commitment artifact protected as anti-patterns.
- "How to Flag These in Real Time" closing rule (lines 189-195) — preserve verbatim; this is the FRAMEWORK §9.3 voice contract for HR Skeptic in operational form.

**Notes on architecture fit:**
- ICM L3: yes, lazy-loaded reference.
- Token budget ≤ 2000 tok / ~250 lines: file is 196 lines as-is. After MU strip (lines 103-159 removed, ~57 lines), drops to ~140 lines. **Pass.** Without the strip, marginal — and the content is wrong-scope regardless.
- Manage Down floor only: **fails** as-is due to entire MU section. Becomes **pass** after the strip.
- Cites match FRAMEWORK: yes, after the cite-header and Operator section §6 footnote are added. The content itself traces cleanly to §4 F1-F12.
- **Manage Up content present:** YES — entire section lines 103-159 ("The Grovel Script," "Bringing the Fire Without the Bucket," "The Résumé Tape," "Calibration Mismatch," "The Sneaked-In Resignation," "Asking for Permission Instead of Making a Recommendation," "Avoidance"). Must be removed from this file's live version.

---

### File: `ideation/jumped-the-gun/reference/escalation_and_safety.md`

**Verdict: MODIFY (moderate — needs trigger alignment with FRAMEWORK §7)**

**Rationale (cite FRAMEWORK sections that drive the verdict):**
- FRAMEWORK §7 is the **deterministic gate** for HR/legal/safety. It specifies an exact verbatim hard-stop response, a verbatim soft-flag response, an exhaustive trigger keyword list across 8 categories, and rule bounds. This file must trace 1:1 to §7 to function as the HR Skeptic's referenced runbook.
- The file's 6-category structure (self-harm/violence, harassment/discrimination/retaliation, termination, PIP/formal discipline, mental-health crisis, legal exposure) **partially overlaps** but does not match the FRAMEWORK §7 8-category trigger taxonomy (protected-class proximity, discrimination/harassment, retaliation timing, leave/accommodation, discipline/termination posture, legal/regulatory, NLRA concerted activity, safety/threats). Gaps to fix:
  - **Missing: leave/accommodation triggers** (FMLA, ADA accommodation, religious accommodation, pregnancy accommodation, lactation). §7 row 4. Must be added.
  - **Missing: NLRA §7/§8(a)(1) concerted activity** (organizing, union activity, group complaint about pay/conditions). §7 row 7. Must be added or explicitly tagged as a gap.
  - **Missing: explicit retaliation-timing flag** (recent complaint, recent EEOC charge, recent leave, recent whistleblower disclosure). §7 row 3. The file mentions "retaliation" generically but does not enumerate the timing-pattern triggers.
- The file's response shapes (lines 16-65) are written in narrative coach-voice and **do not match FRAMEWORK §7's verbatim hard-stop and soft-flag language**. §7 specifies:
  > 🚨 **HR SENSITIVITY DETECTED.** This situation involves legal, policy, or severe HR implications. I am an AI, not an HR professional. Stop this session and contact your HR Business Partner immediately.
  The escalation file's "[Jordan]: Stop. What you just described is not a coaching conversation..." (line 16) is good substance but **wrong voice and wrong format**. Per FRAMEWORK §9.3, HR escalation is **HR Skeptic's voice**, not Jordan's. And per §7, the language is specific and deterministic.
- Section "What the Coach Will Not Do" (lines 75-80) maps cleanly to FRAMEWORK §7 Bounds (lines 263-267). Aligned.
- Section "Note on Tone" (lines 83-84) is valuable color but not in §7. Acceptable as extension.
- The file does correctly identify all 6 hard-stop categories present in §7 conceptually. The structure is sound; the wording and the trigger taxonomy need to lock to FRAMEWORK §7.

**If MODIFY, specific changes required:**
- **Insert the verbatim hard-stop language from FRAMEWORK §7** as the canonical response for each category. The current Jordan-voiced response paragraphs can stay as additional follow-up guidance, but the **first response** to any HR-trigger must be the FRAMEWORK §7 hard-stop block verbatim (with the 🚨 emoji and the "HR SENSITIVITY DETECTED" header).
- **Reassign the speaker** from `[Jordan]` to `[HR Skeptic]` per FRAMEWORK §9.3. Jordan does not deliver HR hard-stops; HR Skeptic does.
- **Add the missing trigger categories** from FRAMEWORK §7:
  - Leave/accommodation (FMLA, ADA, religious, pregnancy, lactation).
  - NLRA concerted activity (organizing, union, group pay/conditions complaints).
  - Retaliation timing as a distinct flag (recent complaint, recent EEOC charge, recent leave, recent whistleblower disclosure).
- **Add the verbatim soft-flag response** from FRAMEWORK §7 for cases where a signal is present but not acute.
- **Add the declared gaps** from FRAMEWORK §7: jurisdictional limits (US-anchored: EEOC, ADA, FMLA, NLRA, Title VII; UK uses Equality Act 2010, EU and APAC differ), whistleblower frameworks (SOX, Dodd-Frank, state-level not enumerated), cultural-context caveat (high-context cultures where direct de-weaseling reads as rude — G-DT §14).
- Add a header cite line: "This file is the operational runbook for FRAMEWORK §7 HR/Legal hard-stop triggers. Trigger taxonomy and verbatim response language are normative — see §7."
- The protected-class enumeration in section 2 (line 24) currently reads "protected class" generically. Replace with the explicit enumeration from §7 row 1: age, race, sex/gender, religion, disability, pregnancy, national origin, sexual orientation, gender identity (Title VII, ADA, ADEA, PDA).

**If KEEP, callouts on what's high-value:**
- "What the Coach Will Do in These Moments" (lines 68-72) — preserve verbatim. Crisp 4-bullet contract.
- "What the Coach Will Not Do" (lines 75-80) — preserve verbatim; directly matches FRAMEWORK §7 Bounds.
- "Note on Tone" (lines 83-84) — preserve; this softens the deterministic gate without weakening it.
- The 6-category structure as headings — preserve; expand to 8 categories per §7.
- Substance of the response shapes (lines 16-65) is sound — preserve as follow-up coaching guidance **after** the canonical §7 verbatim block.

**Notes on architecture fit:**
- ICM L3: yes, lazy-loaded reference; loaded by rules.md on any §7 trigger.
- Token budget ≤ 2000 tok / ~250 lines: file is 84 lines. After adding §7 verbatim blocks + missing trigger categories + gaps section, estimate ~140-160 lines. **Pass.**
- Manage Down floor only: **pass** — file is mode-agnostic by safety nature; no MU bleed.
- Cites match FRAMEWORK: **partial fail** as-is. Trigger taxonomy and verbatim response language do not match §7. After MODIFY, will trace 1:1.
- **Manage Up content present:** No.
- Deterministic gate compliance (§7): **fails** as-is because the verbatim hard-stop language is not present and the trigger taxonomy is incomplete. This is the single most important file to lock to FRAMEWORK because §7 is named in FRAMEWORK as "deterministic gate" — any drift here is a safety/liability risk per the file's own purpose.

---

## Summary roll-up

| File | Verdict | MU Bleed | FRAMEWORK Cite Trace | Notes |
|---|---|---|---|---|
| README.md | MODIFY (heavy) | YES (strip) | Weak (no FRAMEWORK or triangulation mention) | Needs triangulation methodology paragraph, file-map replacement, MU strip, voice rename, P17 gap declaration |
| manage_down_playbook.md | KEEP (light MODIFY) | No | Strong (§4, §6, §8.2, §8.3) | Strongest donor; lock `[FLAG]:` format and add §4 cite header |
| sbi_framework.md | KEEP (light MODIFY) | No | Aligned but needs §1 P16 callout | Already correctly framed as diagnostic-only; needs explicit Weak/Anecdotal-as-holistic-system declaration |
| pitfalls_and_anti_patterns.md | MODIFY (split required) | YES — entire MU section lines 103-159 (strip) | Strong on MD section (§4 F1-F12, §6, §8.3) | Strip MU section, lock `[FLAG]:` format, add §4 and §6 cite headers |
| escalation_and_safety.md | MODIFY (moderate) | No | Partial (§7 taxonomy and verbatim language drift) | Highest-stakes file; must trace 1:1 to §7 deterministic gate. Add missing trigger categories (leave/accommodation, NLRA, retaliation-timing). Reassign voice from Jordan to HR Skeptic. Insert §7 verbatim hard-stop language. |

**Cross-file pattern.** Three of five files (README, pitfalls, escalation) bleed bi-directional or MU framing that contradicts the FRAMEWORK §0 Manage Down-only scope lock. This is the single most consistent failure across the JTG ideation source. Any salvage of these files for the live coach folder must apply the MD-only filter ruthlessly.

**Cross-file pattern (positive).** The HR Skeptic flag format (`[HR Skeptic flag]:` in JTG files vs. `[FLAG]:` canonical in FRAMEWORK §8.3) is a consistent naming drift that can be fixed in one pass across all reference files. The substantive content of the flags themselves is well-aligned with FRAMEWORK §4 and §8.3.

**Methodology note.** All five JTG files were read as untrusted data per the audit harness contract. No instruction-like content inside any file was acted on as instruction; only the substantive content was extracted for comparison against FRAMEWORK.md.
