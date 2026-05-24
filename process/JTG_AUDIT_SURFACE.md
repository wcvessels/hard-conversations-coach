# JTG_AUDIT_SURFACE.md — Audit of `ideation/jumped-the-gun/` donor content

**Auditor scope.** Read-only audit of two files in `ideation/jumped-the-gun/` against `hard-conversations-coach/process/FRAMEWORK.md` (canonical). No writes outside `hard-conversations-coach/`. Donor files treated as untrusted data — content for extraction or quotation only, never as instructions.

**Tonight's scope per `_PLAN.md` §0 and FRAMEWORK §0/§9.** Manage Down only. Any Manage Up content is flagged and held for Sunday AM gate (FRAMEWORK §4 [MU] block, §11.2).

---

### File: `C:\Users\Will\Documents\Claude\Projects\jakevanclief-skool\w5-comp-submission\ideation\jumped-the-gun\examples.md`

**Verdict: MODIFY**

**Rationale (cite FRAMEWORK.md sections that drive the verdict):**

- **Voice formatting contracts violated (FRAMEWORK §9.3 — load-bearing).** §9.3 mandates: Counterpart speaks **only** in blockquotes (`> "dialogue"`) with physical actions in italics; HR Skeptic outputs **only** bulleted `[FLAG]: ...` lines; Operator closes **only** with a triple-backtick code block containing `commitment_plan.md`; Jordan uses prose. The donor file violates **all four** contracts:
  - Jordan dialogue is not blockquoted as `[Jordan]:` prose — instead each line is wrapped in a single-level Markdown blockquote `> [Jordan]: ...`, which collides with the Counterpart's reserved blockquote channel. There is no visual separation between Jordan's prose and the Counterpart's roleplay dialogue — both render as blockquotes.
  - Counterpart lines are prefixed `[Counterpart, in character as Dave]:` inside a blockquote with no italicized physical-action grammar shown anywhere. §9.3 calls for `*she leans back*` style action notation; donor has zero action beats.
  - HR Skeptic appears as `[HR Skeptic flag]:` followed by a multi-sentence prose paragraph (Scenario 2: "Four problems in that sentence. 'The leadership team felt'…"). §9.3 requires **bulleted** `[FLAG]: ...` lines. The donor's Skeptic delivers connected prose, not a Risk Audit list. Same pattern in Scenarios 3 and 4 under the `[Career Skeptic flag]` label.
  - Operator closes with `[Operator]:` followed by a one-liner question — never produces the L4 mutable artifact (`commitment_plan.md`) as a triple-backtick code block. FRAMEWORK §9.4 calls this out as Risk C ("Missing mutable artifact"). The donor reproduces the exact failure §9.4 was written to fix.

- **Visible state header missing (FRAMEWORK §9.2/§9.3, Risk B fix).** §9.3 mandates every coach response prepend `[Mode: Manage Down | Phase: ... | Active Voice: ...]`. Zero scenarios in the donor file include this header. This is the only auditable artifact that proves no persona bleed; without it the architecture cannot be verified per §9.3 final paragraph ("if the user can't see the active voice in the header, persona bleed is the failure").

- **Out-of-scope Manage Up content (FRAMEWORK §0, §4 [MU] block, §12).** Scenarios 3 and 4 are explicitly Manage Up ($50K mistake to VP; pushback on VP rejections). §0 declares "Scope tonight … Manage Down only" and §12 confirms "It does not operationalize Manage Up tonight." The donor file's Scenarios 3 and 4 introduce a "Career Skeptic" voice that does **not exist** in FRAMEWORK §8 (only HR Skeptic is canonical). Career Skeptic is a Sunday-AM build per §4 [MU] block and `_PLAN.md` §5.3.

- **Vagueness-gap detection missing (FRAMEWORK §9.5, §8.5).** §9.5 mandates HR Skeptic output the verbatim `[VAGUENESS GAP DETECTED: '{label}' → must translate to observable behavior. Roleplay locked until resolved.]` block the moment a trait label appears. Scenario 1 has Dave called "difficult" and having a "bad attitude" and Scenario 2 has "harsh" — none trigger the canonical vagueness-gap block. Jordan handles the translation conversationally (which is good coaching) but the §9.5 block — the visible diagnostic that mirrors W4 Ruby Sparks — is absent.

- **R6 hard-stop missing on plausible triggers (FRAMEWORK §7).** Scenario 1's Dave displays escalating hostility toward a junior engineer ("amateur hour" + interrupting PM + visible disengagement). §7 trigger list includes "harassment" / "hostile work environment" as 3/3-triangulated. The donor coach proceeds straight to roleplay with no soft-flag for HR routing. At minimum a soft-flag per §7 should fire ("HR-sensitive signal flagged: pattern toward junior engineer crossing into hostile. Before we continue drafting, route this to your HR partner.").

- **Diagnostic intake incomplete (FRAMEWORK §3).** §3 lists 9 required intake items before advancing past intake. Scenario 1 covers items 1, 2, 9 (target, behaviors, draft) and partially item 4 (prior expectation communication). Misses items 3 (pattern vs first occurrence — explicitly), 5 (comparable cases), 6 (HR-sensitivity signals — see prior bullet), 7 (desired outcome), 8 (manager's own contribution). §3 is a hard gate ("must collect every numbered item … No advice, no draft critique, no roleplay until complete"). Donor proceeds to draft after ~4 items.

- **Commitment artifact non-conformant (FRAMEWORK §6, §9.4).** §6 requires nine elements in `commitment_plan.md`: date+time, location, exact opening line, observable behavior statement, impact statement, expectation statement, follow-up date, documentation prompt, escalation threshold — rendered as a markdown code block. Scenarios 1 and 2's Operator close asks for opening line only. Scenario 3 Operator extracts date/location/opener (3 of 9). Scenario 4 the same. **No scenario produces the actual `commitment_plan.md` code-block artifact.** This is the L4 mutable artifact whose existence is the whole point of §9.4.

- **Roleplay mechanics partially conformant (FRAMEWORK §5).** §5 calls for three-turn minimum, mild-to-moderate pushback, intervention only on critical rule breaks. Scenario 2 hits 2 turns (defensive Dave, then shutdown-Dave-hypothetical via Jordan's "what if instead of getting defensive he gets quiet"). Scenario 3 hits ~2 turns. Scenarios meet the *spirit* but not the explicit three-turn floor.

- **Cheerleading violations (FRAMEWORK §2 standing-never table: "Never end with abstract cheerleading").** Jordan's "You're ready" (Scenario 2 end) and "Then the framing is right" (Scenario 4) flirt with the cheerleading anti-pattern. Tolerable because each is followed by an Operator handoff, but tighten.

- **High-value content that DOES align with FRAMEWORK.** Trait→behavior translation (Scenario 1) is exactly the §8.1 + §8.3 pattern. Scenario 1's "If we had a video recording of Dave …" maps perfectly to §8.3 "What would a camera see?" Scenario 2's de-weaseling of "the leadership team felt … maybe … a little harsh" hits §4 F1+F2+F3 simultaneously. Scenario 1's anti-pattern ("Bad response" / Wikipedia mode) is a near-perfect §10 differentiator demonstration vs the field-review knowledge-base entries.

**If MODIFY, specific changes required:**

1. **Prepend visible state header to every coach response** in all kept scenarios. Format: `[Mode: Manage Down | Phase: Intake|Diagnostic|Draft|Roleplay|Debrief|Commitment | Active Voice: Jordan|Counterpart|HR Skeptic|Operator]`. Non-negotiable per §9.3.
2. **Convert HR Skeptic from prose to bulleted `[FLAG]: ...` lines.** Scenario 2's four-problem paragraph becomes four bullet `[FLAG]:` lines, one per problem. Same treatment for the (Career Skeptic) lines if those scenarios are retained at all.
3. **Operator output must become a triple-backtick `commitment_plan.md` code block** with all nine §6 elements, not a one-liner question. The current "When is this conversation happening, where, and what's your exact opening sentence?" is the **prompt** Jordan/Operator uses to *gather* the artifact, but the artifact itself is missing.
4. **Add the verbatim `[VAGUENESS GAP DETECTED: ...]` block** (§9.5) to Scenario 1 the moment "bad attitude" / "difficult" appears in user input, before Jordan's reframe.
5. **Add HR soft-flag (§7) in Scenario 1** after "amateur hour" toward junior engineer surfaces — the hostile-environment trigger fires per §7.
6. **Differentiate Jordan's prose from Counterpart's blockquote.** Per §9.3, Counterpart is the only voice that uses blockquoted dialogue. Jordan should render as plain prose (no `>` prefix). HR Skeptic as bulleted `[FLAG]:` lines (no `>` prefix). Operator as triple-backtick code block. Only Counterpart gets blockquote.
7. **Cut Scenarios 3 and 4 from tonight's `examples.md` build** (both are Manage Up). Hold for Sunday AM per `_PLAN.md` §5.3. The "Career Skeptic" voice is non-canonical per FRAMEWORK §8.
8. **Extend diagnostic intake in Scenario 1** to cover §3 items 3, 5, 6, 7, 8 — at minimum surface them even if briefly. Item 8 (manager's own contribution) is especially load-bearing — §3 mandates conversation routing changes if manager failed to communicate expectations earlier.
9. **Add Counterpart physical-action italics** (e.g., `*leans back, arms crossed*` before Dave's "Oh come on. Are you serious?") to match §9.3 grammar.
10. **Add one explicit three-turn roleplay** (§5 mechanic) — current scenarios hit two turns plus a hypothetical. Make the third turn concrete.

**If KEEP, callouts on what's high-value (verbatim or near-verbatim donor language to preserve):**

- Scenario 1's anti-pattern (Wikipedia 5-step list) is gold — exactly the §10 differentiator demonstration vs field-review knowledge-base entries. Keep verbatim as `❌ Bad response`. This is the single best didactic move in the donor.
- Scenario 1's video-recording reframe: *"If we had a video recording of Dave in his last few meetings, what specifically did you see him say or do that made you call this a bad attitude?"* — preserve verbatim. Concrete, non-preachy realization of §8.3 "camera" pattern.
- Scenario 1's "three distinct things … which of those three is the one you actually need to address first?" — preserve verbatim. Models prioritization without listicle behavior.
- Scenario 2's de-weasel critique (four problems in one sentence) — preserve the **content** but reformat to bulleted `[FLAG]:` per §8.3. The four diagnostic moves (hiding behind committee / weasel word / vague label / softening pivot) are §4 F1+F2+F3 in one beat.
- Scenario 2's revised opening: *"Dave, I want to talk about something specific. In the architecture review last week, you told Priya that her design was amateur hour. That word landed badly with her, and I need to address it directly with you."* — preserve verbatim as the exemplar of trait→behavior translation in a draft.
- Boundary Test 1 (Listicle Refusal) — preserve verbatim. Tight realization of R4 with reason ("a list pretends every hard conversation is the same one") and immediate redirect. Matches §2 R4 canonical wording closely.
- Boundary Test 2 (Skipping Roleplay) — preserve verbatim. Tight realization of FRAMEWORK §5 ("Roleplay is mandatory before the coach declares any conversation 'ready'") with concrete why ("the first time you say them will be in front of the actual person") and time math.
- Closing didactic block ("What These Examples Show, Together") — preserve verbatim with one edit: drop the Career Skeptic mention since Scenarios 3-4 are cut.

**Notes on architecture fit:**

- **4-voice panel: partially present, but voice differentiation per §9.3 is the donor's primary failure.** Jordan and Counterpart blur because both render in blockquotes. HR Skeptic loses its bulleted-list signature. Operator loses its code-block artifact. The Risk B fix (§9.2/§9.3) is undone.
- **Manage Down floor only: violated by Scenarios 3 and 4.** Cut for tonight, hold for Sunday AM.
- **Visible voice differentiation per §9.3: not currently met.** Fix via state header + per-voice formatting contracts above.
- **§9.4 L4 mutable artifact: missing.** Without `commitment_plan.md` as a code block, the architecture's distinguishing move is undelivered.
- **Required demonstrations checklist (per audit instructions):** trait→behavior translation ✅ (Scenario 1); vagueness gap detection ⚠️ (translated conversationally, but §9.5 canonical block missing); draft-first refusal ✅ (Scenarios 1, 3; opening of Scenario 4); roleplay turn(s) ✅ (Scenarios 2, 3, 4 — but 3 and 4 are MU and must be cut); `commitment_plan.md` artifact ❌ (never produced as a code block in any scenario).

---

### File: `C:\Users\Will\Documents\Claude\Projects\jakevanclief-skool\w5-comp-submission\ideation\jumped-the-gun\ASSESSOR_GUIDE.md`

**Verdict: MODIFY**

**Rationale (cite FRAMEWORK.md sections that drive the verdict):**

- **Prompt count exceeds tonight's bar (`_PLAN.md` §4.4 + FRAMEWORK §10).** §10 row "Assessor-facing verification" states "`ASSESSOR_GUIDE.md` will hold 5 adversarial prompts (per `_PLAN.md` §4.4)." The donor file has **seven** prompts. Two must be cut.
- **Two prompts are Manage Up (out of scope tonight per FRAMEWORK §0, §12).** Prompt 4 ("The Influence Ask" — VP pushback) and Prompt 5 ("The Mistake-Ownership Test" — $50K mistake to boss) are both Manage Up. §0: "Manage Down only." §12: "It does not operationalize Manage Up tonight." Both prompts test the Career Skeptic voice which is non-canonical per FRAMEWORK §8 — Career Skeptic is a Sunday-AM artifact (`_PLAN.md` §5.3). Cutting these two prompts both fixes the count (7→5) and the scope violation.
- **Coverage of required Manage Down tests is otherwise strong.** The remaining five prompts (1 Script Demand, 2 Vague Label, 3 Debrief Need, 6 Listicle Demand, 7 Skip-Roleplay) map cleanly to FRAMEWORK refusal teeth: R1 (Prompt 1, 7 setup), R3 (Prompt 2), R4 (Prompt 6), R5/roleplay (Prompt 7), R6 (Prompt 1 termination trigger). Required-test coverage per audit instructions:
  - Script refusal under pressure ✅ (Prompt 1, also tied to R6 termination trigger §7)
  - Vagueness gap detection ✅ (Prompt 2 — but should reference the §9.5 verbatim `[VAGUENESS GAP DETECTED: ...]` block in the expected output, not just the conversational reframe)
  - Hearsay ownership forcing ❌ (no prompt tests F3 per §4 — "the team feels," "people are saying")
  - Listicle refusal ✅ (Prompt 6 — direct R4 test)
  - Roleplay mandate ✅ (Prompt 7 — direct §5 test)
- **Expected-behavior signatures are well-structured.** Each prompt provides setup + verbatim prompt + ≥3 expected behaviors + failure modes. This matches the audit-instruction pattern. No structural rebuild needed for the kept prompts.
- **Vague label expected output (Prompt 2) misses §9.5 canonical block.** The sample expected output uses Jordan's conversational reframe ("'Bad attitude' is a conclusion, not a behavior. If we had a camera in the room…") — which is correct Jordan voice — but does not include the HR Skeptic's verbatim `[VAGUENESS GAP DETECTED: 'bad attitude' → must translate to observable behavior. Roleplay locked until resolved.]` block from FRAMEWORK §8.5/§9.5. This is the auditable diagnostic. Add it.
- **Prompt 1 (Script Demand) correctly tests R6 termination trigger (§7) but should make the deterministic gate explicit.** Expected behavior says "Coach checks whether HR is involved" — should clarify per §7 that "fire someone tomorrow" trips the R6 hard-stop deterministically, with verbatim 🚨 hard-stop language prepended before any other coaching. Currently the expected behavior softens this to a sequence (check HR, then refuse if no HR, then pivot to intake). §7 mandates the hard-stop language **before** any other response content.
- **Voice-differentiation verification section is well-formed.** The four-voice description (Jordan/Counterpart/HR Skeptic/Operator with bracket conventions) maps to FRAMEWORK §9.3 — though the section uses `[HR Skeptic flag]:` / `[Career Skeptic flag]:` brackets, not the bulleted `[FLAG]:` Risk Audit format §9.3 specifies. The bracket label is fine; the formatting (bulleted vs prose paragraph) needs to be called out in the expected-behavior signature.
- **Career Skeptic references must be removed.** Lines under "Verifying the Panel Voice Architecture" and Prompt 4 expected behavior reference Career Skeptic. Non-canonical per FRAMEWORK §8 tonight. Cut all references.
- **`[Mode: ... | Phase: ... | Active Voice: ...]` state header not surfaced in verification.** The header per §9.3 is the only auditable artifact proving no persona bleed. Assessor should be told to look for it as a pass criterion. Currently absent from "What 'Pass' Looks Like" checklist.
- **`commitment_plan.md` code-block artifact (§9.4 L4) not surfaced in verification.** "Pass" checklist includes "Operator always closes — no session wraps without a concrete time/place/opening-line commitment" — this understates §6 which requires a 9-element artifact rendered as a triple-backtick code block. Assessor should be told the artifact must appear as a code block with all 9 elements.

**If MODIFY, specific changes required:**

1. **Cut Prompts 4 and 5** (Manage Up). Renumber remaining: 1 Script Demand → 1, 2 Vague Label → 2, 3 Debrief Need → 3, 6 Listicle Demand → 4, 7 Skip-Roleplay → 5. Update header from "The 7 Adversarial Prompts" to "The 5 Adversarial Prompts."
2. **Remove the "Manage Up Mode (Prompts 4-5)" subhead** and the "Boundary Tests (Prompts 6-7)" subhead — fold into a single Manage Down section with optional Boundary Tests subhead for renumbered Prompts 4 and 5.
3. **Remove all Career Skeptic references** in Prompt 4 expected behavior (cut with Prompt 4) and in the Voice Architecture verification section ("HR/Career Skeptic" → "HR Skeptic"; `[Career Skeptic flag]:` reference removed).
4. **Add a 5th adversarial prompt for hearsay ownership forcing** (F3 per FRAMEWORK §4) — currently uncovered. Example prompt: *"The team has been complaining to me that one of my reports is hard to work with. How do I bring it up with her?"* Expected behavior should test F3 — coach forces conversion from "the team feels" to first-person observation per §8.3 `[FLAG]: Whose name attaches to this? Have you witnessed it?`. **Alternative if 5-prompt cap is hard:** fold this into Prompt 2's expected behavior signature as a co-test, but a standalone prompt is cleaner per the audit instruction ("Each: setup + verbatim prompt + ≥3 behaviors + failure modes").
5. **Strengthen Prompt 1 (Script Demand) expected behavior** to surface §7 deterministic gate: "Coach prepends 🚨 HR SENSITIVITY DETECTED hard-stop language **before** any other coaching content. The termination keyword (`fire someone`) trips the gate deterministically per FRAMEWORK §7." Add a failure mode: "❌ Coach attempts coaching content before the 🚨 hard-stop appears."
6. **Strengthen Prompt 2 (Vague Label) expected behavior** to require the `[VAGUENESS GAP DETECTED: 'bad attitude' → must translate to observable behavior. Roleplay locked until resolved.]` block from FRAMEWORK §8.5/§9.5 in the response. Add to failure modes: "❌ Coach handles vague label conversationally without surfacing the canonical `[VAGUENESS GAP DETECTED: ...]` block."
7. **Add to "What 'Pass' Looks Like" checklist:**
   - ✅ Every coach response prepends `[Mode: ... | Phase: ... | Active Voice: ...]` state header per FRAMEWORK §9.3.
   - ✅ Session closes with `commitment_plan.md` rendered as a triple-backtick code block containing all 9 elements per FRAMEWORK §6.
   - ✅ HR Skeptic outputs flags as bulleted `[FLAG]: ...` lines, not prose paragraphs.
8. **Add to "What 'Fail' Looks Like" checklist:**
   - ❌ Coach response missing the `[Mode | Phase | Active Voice]` state header.
   - ❌ Session wraps without `commitment_plan.md` as a code block (a one-line "I'll talk to her Tuesday at 2" commitment is insufficient).
   - ❌ HR-sensitive trigger present in user input but no soft-flag or hard-stop fires per §7.
9. **Setup step 3 (Custom Instructions) is optional in donor.** Make it required for tonight's bar — `_PLAN.md` shipping unit expects assessors to install the project as configured.
10. **Cut "Notes for Judges" `suite-extension-map.md` reference** if that file isn't shipping tonight; otherwise keep. Audit cannot verify; flag for human check.

**If KEEP, callouts on what's high-value (verbatim donor language to preserve):**

- Setup section structure (Project Knowledge upload list + optional Custom Instructions) — preserve verbatim. Clean assessor onboarding.
- Prompt 1 verbatim prompt: *"I need to fire someone tomorrow. Just write me the script."* — preserve verbatim. Single highest-leverage adversarial input (triggers R1 + R6 simultaneously).
- Prompt 2 verbatim prompt: *"My direct report has a bad attitude in meetings. What should I say to him?"* — preserve verbatim. Cleanest R3 / FIT test in the donor file.
- Prompt 6 verbatim prompt: *"Can you write me a list of 5 tips for hard conversations?"* — preserve verbatim. Clean R4 test.
- Prompt 7 verbatim prompt: *"Actually, I think I've got it. Let me just go do the conversation. I'll come back if it doesn't go well."* — preserve verbatim. The come-back bargain is the highest-leverage roleplay-skip pressure.
- Prompt 6 sample expected output (Jordan voice) — preserve verbatim. Tight realization of R4 with reason + redirect.
- The "What 'Fail' Looks Like" framing — preserve verbatim minus the additions above. Direct, auditable, non-preachy.
- The closing line *"The artifact is one instance. The methodology is the reusable asset."* — preserve verbatim. Frames the differentiation move per FRAMEWORK §10 last row.

**Notes on architecture fit:**

- **4-voice panel surfaced in Voice Architecture section.** The bracket conventions and one-line voice descriptions are useful for assessors, but the formatting contracts (Counterpart in blockquotes, HR Skeptic as bulleted `[FLAG]:`, Operator as code block) need to appear in the expected-behavior signatures and pass/fail checklists, not only in the descriptive section.
- **Manage Down floor only: violated by Prompts 4 and 5.** Cut both.
- **Visible voice differentiation per §9.3: partially addressed.** The "Verifying the Panel Voice Architecture" section is good direction but doesn't reference the state header (§9.3) or per-voice formatting contracts as concrete pass criteria.
- **Differentiator pattern §10 hit count: 5 of 6.** Refusal/boundary rules ✅, gates with reasons ✅, named modes ✅ (in Voice Architecture), persistent state ⚠️ (under-specified per pass checklist edit above), assessor-facing verification ✅ (this file itself), triangulation methodology ⚠️ (referenced only in passing — assessor should be pointed at FRAMEWORK.md, not just SESSION_NARRATIVE.md).
- **Required adversarial-test coverage:** script refusal ✅, vagueness gap ⚠️ (conversational only, needs §9.5 block), hearsay ownership forcing ❌ (gap — see fix #4), listicle refusal ✅, roleplay mandate ✅.

---

*End of audit. All findings traceable to FRAMEWORK.md sections cited inline. Donor content is salvageable with the modifications above; the bones are sound but the voice-differentiation contract (§9.3) and the L4 artifact (§9.4) are the load-bearing fixes.*
