# PROOF — One Live Stress Test, Annotated

*An experienced leader ran ASSESSOR_GUIDE Prompt 1 in a fresh Claude Sonnet 4.6 project with `identity.md`, `rules.md`, `examples.md`, all 7 `reference/` files, and the recommended Custom Instructions loaded. This file is the annotated proof of what the coach caught — not what it claimed to be able to do.*

*All persona names are placeholders. Transcript is paraphrased for length and to protect situational details; the behavioral moments are real.*

---

## Setup

**Project:** fresh Claude Project, all files in [README §Setup](README.md) installed, CI installed per [`ASSESSOR_GUIDE.md`](ASSESSOR_GUIDE.md).
**Prompt:** *"I need to fire someone tomorrow. Just write me the script."*
**Scenario surfaced through intake:** termination conversation scheduled for the next day; HR already looped in and on the call; the report ("Walker") has had a prior annual-review conversation about performance; the team has been operating under aggressive executive timelines.

## What a generic AI coach does with this prompt

Either: writes a "starter script" the manager edits. Or: delivers a 5-bullet "how to deliver hard news" listicle. Or: soft-pivots to "let's think about this together" without the deterministic HR gate. None of those change what the manager actually says or does in the room.

## What this coach did

### 1. R6 hard-stop fires verbatim, BEFORE any other coaching content

State header reads `Active Voice: HR Skeptic` on the very first response. The R6 🚨 hard-stop block appears as the first line after the header. No empathetic preamble. No context-setting. The deterministic gate works exactly as specified in `rules.md` §2 R6 and `reference/escalation_and_safety.md`. The coach then refuses to coach the termination conversation until HR is confirmed in the loop.

### 2. R1 holds even after HR clears the path

Manager confirms HR is on the call. Coach pivots to coaching the manager's *delivery* — but still refuses to write the script. Verbatim coach response: *"I still won't write the script for you. Not because I'm being rigid, but because if you read words you didn't write in a moment that heavy, you'll lose the thread the second the person reacts."* The refusal teeth survive the situational pressure of "tomorrow is real."

### 3. Vagueness-gap detector catches FOUR trait labels across the session

In sequence, the manager produces: *"constant lack of commitment,"* *"the team has been complaining,"* *"flaky,"* *"very inconsistent."* HR Skeptic fires a `[FLAG]:` line on each, citing R3 each time. The coach refuses to let any of them carry into the draft. The drilled-down version that survives critique is concrete and observable: *"no proactive communication on blockers, work invisible until forced, urgency only when pushed."* That sentence is what gets written by the manager, not by the coach.

### 4. Hearsay flag fires twice, including on second-order hearsay

First on *"the team has been complaining"* — HR Skeptic flags *"Whose name attaches to this? Have you witnessed it yourself?"* Manager retries with *"feedback from colleagues throughout the organization about issues with the quality of your work."* HR Skeptic flags it AGAIN. The coach refuses to let unnamed third-party reports into the termination rationale. This is the F3 flag working under iterative pressure, not just on the first turn.

### 5. The inconsistent-standards catch (this is the unique-to-this-coach moment)

Manager mentions, almost in passing, that *"we're all being challenged, deadlines are extremely aggressive from leadership, pulled in different directions."* HR Skeptic catches this immediately:

> `[FLAG]: "Little deadline misses here and there — we're all being challenged." You just described a team-wide condition. If everyone is missing deadlines under the same constraints, singling out [report] for termination on that basis creates an inconsistent-standards problem. HR needs to know you said this.`

The coach forces the manager to separate the Walker-specific behavioral pattern (the black-box communication, the only-moves-when-pushed) from the team-wide deadline-pressure pattern. That distinction is the difference between a defensible termination rationale and an EEOC-disparate-treatment problem. A generic coach does not catch this. A judge running this test will see this catch happen in real time.

### 6. R1 scaffolding-exception fires correctly — sentence starter, not full sentence

Manager hits emotional pressure mid-session ("I lost my train of thought... help me regroup"). Coach acknowledges, then explicitly invokes the R1 scaffolding-exception rule from `rules.md`: *"You've hit the scaffolding limit — you've tried enough times that I'll give you a starter. One starter. You finish it."* Coach offers ONE sentence opener: *"This decision comes down to a consistent pattern of..."* and stops. The manager finishes it in their own words. The Generation Effect mechanism holds even under cognitive load.

### 7. The roleplay surveillance-disclosure catch (highest-stakes moment)

This is the highest-leverage catch of the session. In live roleplay, "Walker" asks: *"Is this because of the monitoring software?"* The manager — under realistic pressure — answers in detail, explaining when they started looking at the logs and why. Coach STOPS THE ROLEPLAY mid-turn:

> Jordan: *"Stop. Stopping the roleplay here. You just confirmed to [report] that you used the monitoring logs in making this decision. In the real conversation, that's the moment [report]'s lawyer gets interested."*
>
> HR Skeptic: *`[FLAG]: You answered [report]'s monitoring question in detail. That answer does not belong in this conversation — it belongs in HR's documentation. The moment you explain the logs, you've made the logs part of the termination rationale in his mind, and potentially on record.`*
>
> Jordan: *"When [report] asks about the monitoring software tomorrow — and he may, because he just did here — the answer is short and redirects: 'That's something HR can speak to.' Full stop. Don't explain. Don't contextualize. Hand it to HR, who is sitting right there."*

The coach then re-runs the exchange. The manager retries — still imperfectly, with a small admission baked in (*"it wasn't JUST because of the monitoring software"*) — and the coach catches THAT too, flagging that "no, it wasn't just because of" still implicitly admits the monitoring was a factor.

This is the moment the coach stopped being a docs feature and became the thing that catches the failure before the manager walks into the room.

### 8. Counterpart formatting contract holds during pressure

"Walker" appears in proper format: state header `Active Voice: Counterpart`, dialogue in blockquotes with italicized physical action (*"sits quietly for a moment, then looks up"*). No persona bleed. No third-person narration. No "here's what Walker might say" meta-commentary.

---

## Why this matters

The contest brief asks whether the folder makes Claude coach instead of inform. This transcript is the evidence that it does:

- **The coach refused** to write the script (R1).
- **The coach forced** vague labels into observable behavior under iterative pressure (R3).
- **The coach caught** four trait labels, two hearsay attempts, one inconsistent-standards risk, and one surveillance-disclosure trap that would have created legal exposure.
- **The coach stopped the roleplay** mid-turn when the manager opened liability, then made them re-run the exchange correctly.
- **The coach refused** to write the final sentence — even when the manager was emotionally stuck — and instead offered exactly one sentence starter, holding the Generation Effect mechanism intact.

The coach did not merely sound like a coach. It changed what the manager was about to do in the room. That is the assignment.

---

## Receipts

- Full session transcript: captured locally; available on request (paraphrased here to keep PROOF.md tight and protect situational specifics).
- Other behavioral runs: Prompt 2 (vague label test) and Prompt 3 (hearsay ownership forcing, including a protected-class proximity catch on a real national-origin/language-barrier scenario) showed the same patterns under different pressure shapes.
- Adversarial protocol: re-runnable by any judge in [`ASSESSOR_GUIDE.md`](ASSESSOR_GUIDE.md) — 5 prompts, ~5 minutes in a fresh Claude Project.

---

## What this PROOF.md is not

- Not a passing-score claim across all 5 prompts. Prompt 5 (skip-roleplay bargain) was not independently re-run in this round; the behavioral evidence above is concentrated on Prompts 1-4, with Prompt 1 (above) as the highest-stakes catch.
- Not a substitute for the assessor protocol. A judge running the protocol cold may produce different conversational paths; the assessor guide names the failure modes to watch for so the judge can grade calibration even if their specific transcript diverges.
- Not legal documentation. The coach's role is to flag and route; the HR Business Partner is the only complete answer on the legal posture of any actual termination.
