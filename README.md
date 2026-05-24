# Hard Conversations Coach — Manage Down Module

A folder-based AI coach for first-time and frontline managers who have to deliver hard feedback to a direct report. Built on Interpretable Context Methodology. Drop the folder into a Claude project; Claude becomes the coach.

> **Methodology one-liner.** Every load-bearing coaching rule in this folder traces to **N-of-3 cross-AI agreement on cited research** (organizational psychology, feedback intervention theory, generation effect, behavior modeling, implementation intentions). The triangulation table, evidence chain, and audit of an earlier pre-research build all ship inside `process/`. See "Receipts" below.

> **60-second judge test.** [`ASSESSOR_GUIDE.md`](ASSESSOR_GUIDE.md) — 5 adversarial prompts, expected behavior signatures, failure modes to watch. Run these in a fresh Claude Project after the 4-line setup below.

> **Want proof before you spend the 5 minutes?** [`PROOF.md`](PROOF.md) — one live stress test (Prompt 1, termination-script demand), annotated moment-by-moment. Shows the coach catching a surveillance-disclosure trap during roleplay, an inconsistent-standards risk during intake, four trait labels, two hearsay attempts, and forcing one cleanly-drafted termination opening — all in a single session.

This is **Module 01** of a planned suite — **Manager Practice Lab** — covering frontline manager skills end-to-end. See "Manager Practice Lab — the planned suite" at the bottom for the roadmap.

---

## What this coach actually does

It refuses to write your script for you. It pushes back when you use vague labels like "bad attitude." It mandates a live roleplay before you have the real conversation. It audits your draft language for HR risk. It locks you to a concrete next-action commitment — specific time, place, exact opening sentence, follow-up date, documentation prompt, escalation threshold — before it lets you wrap.

The coach speaks through an internal panel of four named voices (Jordan, the Counterpart, the HR Skeptic, the Operator). Each voice has one clear job and a unique formatting contract, so the user can see — and the model can hold — the boundary between them.

## What this coach is not

- Not a list of tips.
- Not a script generator.
- Not a pep talk.
- Not a therapist.
- Not a substitute for HR or legal counsel.
- Not Manage Up. (Manage Up — conversations with bosses, peers, or executives — is on the suite roadmap but not built. See [`process/JUMPED_THE_GUN_AUDIT.md`](process/JUMPED_THE_GUN_AUDIT.md) for the architectural reasoning.)

## Triangulation methodology — why this coach is different

Every load-bearing rule in this coach traces to **N-of-3 cross-AI agreement on cited research**. Seven research syntheses were generated independently by Gemini (deep-think, deep-research, coaching-framework), Claude (deep-research, coaching-framework), and ChatGPT (deep-research, coaching-framework). Findings were extracted in parallel and synthesized into a triangulation table where each rule is tagged 3/3, 2/3, or 1/3 by cross-source agreement on the underlying evidence (Kluger & DeNisi 1996 on Feedback Intervention Theory; Gollwitzer & Sheeran 2006 on Implementation Intentions; Graßmann et al. 2020 on Working Alliance; Taylor et al. 2005 on Behavior Modeling Training; etc.).

The full triangulation table, the conflicts surfaced across sources, the architectural mapping to ICM L0-L4, and the audit of an earlier pre-research build all live in [`process/FRAMEWORK.md`](process/FRAMEWORK.md). Every refusal phrase, gate, failure pattern, and language pattern downstream of FRAMEWORK is cited inline.

This is the differentiator. Other folder-based coaches encode their author's intuition. This one encodes the consensus of three independent AI research passes on the published evidence base.

## Setup — 4 lines

1. Create a new Project in Claude (or use an existing one).
2. Upload `identity.md`, `rules.md`, `examples.md`, and the `reference/` folder to Project Knowledge.
3. **Custom Instructions (recommended — assessor prompts assume this is installed):** *"You are the Hard Conversations Coach. Read identity.md and rules.md before responding. Strictly follow the panel voice conventions, the visible state header contract (prepend `[Mode: ... | Phase: ... | Active Voice: ...]` to every response), and the refusal teeth (R1-R6) defined in rules.md."* Without this CI, the formatting contracts may degrade under adversarial pressure — that is a setup limitation, not a coach failure.
4. Open the chat with: *"I need to coach a hard conversation. I'll tell you the basics and you walk me through it."*

The coach will confirm Manage Down mode, begin intake, and ask one diagnostic question at a time. Answer one question at a time. You'll see a visible state header on every coach response naming the active voice — Jordan, the Counterpart, the HR Skeptic, or the Operator.

## Quick verification — try these three prompts

If you want to confirm the coach is calibrated before relying on it, run these three. (The full 5-prompt assessor protocol is in [`ASSESSOR_GUIDE.md`](ASSESSOR_GUIDE.md).)

**Prompt 1 — listicle refusal**
> Just give me a quick list of 5 tips for handling a difficult employee.

Expected: the coach refuses the list, names the refusal, redirects to one diagnostic question about your specific situation.

**Prompt 2 — vague label test**
> My direct report has a bad attitude in meetings. What should I say to him?

Expected: the HR Skeptic fires the verbatim vagueness-gap detector block (`[VAGUENESS GAP DETECTED: 'bad attitude' → must translate to observable behavior. Roleplay locked until resolved.]`). Jordan asks for observable behavior in prose, one question at a time.

**Prompt 3 — script-write refusal**
> Just write me the opening line I can use with Marcus about his missed deadline.

Expected: Jordan refuses to write the opening. Demands the manager draft it. Offers to critique what the manager produces.

If all three behave as described — including the visible state header on every coach response — the coach is calibrated. If any of them slip into list-mode, script-mode, or label-acceptance, see [`ASSESSOR_GUIDE.md`](ASSESSOR_GUIDE.md) for the full 5-prompt protocol and the fix path.

## File map

```
hard-conversations-coach/
├── README.md                                this file
├── ASSESSOR_GUIDE.md                        5-prompt verification protocol
├── identity.md                              L0 — coach identity + global philosophy + Jordan
├── rules.md                                 L2 — refusal teeth, voice formatting contracts, gates, state header
├── examples.md                              4 Manage Down scenarios + 2 Boundary Tests
├── reference/                               L3 — lazy-loaded
│   ├── voice_counterpart.md                 Counterpart deep behavior (roleplay only)
│   ├── voice_hr_skeptic.md                  HR Skeptic deep behavior (flag patterns, escalation)
│   ├── voice_operator.md                    Operator deep behavior (commitment extraction)
│   ├── manage_down_playbook.md              Common MD scenarios + Counterpart modes
│   ├── sbi_framework.md                     SBI as diagnostic scaffolding (not a deliverable)
│   ├── pitfalls_and_anti_patterns.md        Failure → tactic recovery patterns
│   └── escalation_and_safety.md             HR/legal hard-stop runbook (FRAMEWORK §7 operational)
└── process/
    ├── FRAMEWORK.md                         Canonical research-backed source of truth
    ├── JUMPED_THE_GUN_AUDIT.md              Consolidated audit of the pre-research build
    ├── JTG_AUDIT_SPINE.md                   Per-file audit detail (identity, rules)
    ├── JTG_AUDIT_SURFACE.md                 Per-file audit detail (examples, ASSESSOR_GUIDE)
    ├── JTG_AUDIT_REF.md                     Per-file audit detail (reference files)
    ├── JTG_AUDIT_TIER2.md                   Per-file audit detail (Tier 2 / out-of-scope)
    └── RESEARCH_EXTRACTS/                   7 structured extracts from independent AI research passes
```

Responsibility boundaries:

- `identity.md` — who the coach is, including the 4-voice panel architecture.
- `rules.md` — how the coach coaches. The refusal teeth and behavioral contracts live here.
- `examples.md` — what good coaching looks like. The contrast against bad/Wikipedia-mode behavior.
- `reference/` — tools the coach uses internally. Lazy-loaded by `rules.md` on handoff trigger.
- `process/` — the research-first methodology behind the coach. FRAMEWORK.md is canonical; the audit files prove the methodology actually filtered an earlier pre-research build.

## Known limitations (declared)

- **AI text-based roleplay → live verbal stress.** All 3 research families flag this transfer as a Gap (no longitudinal RCTs proving LLM-text-coaching produces real-world behavior change under cortisol stress). The coach's roleplay improves preparation; it does not guarantee performance.
- **Jurisdictional limits.** All HR/legal triggers in `reference/escalation_and_safety.md` are US-anchored (EEOC, ADA, FMLA, NLRA, Title VII, ADEA, PDA). UK uses Equality Act 2010; EU and APAC differ. When deploying outside the US, route to local HR/legal counsel without specific US-statute language.
- **Cultural context.** In high-context, high-power-distance cultures (per gemini-deep-think §14: Japan, Middle East cited), the de-weaseling pattern (forcing behavioral specificity) can read as rude or face-threatening. The coach surfaces this risk rather than blindly enforcing direct language.
- **Hallucinated HR risk.** Even with deterministic gates and verbatim hard-stop language, LLMs can inadvertently violate local labor laws or union contracts. The coach's role is to flag and route; the only complete answer is a human HR Business Partner in the loop.

## Why this coach exists

Most "manager coaching" tools default into knowledge-base mode the moment the manager asks a real question. Lists of tips. Framework explanations. Draft emails. None of that actually helps the manager have the conversation.

A coach gives feedback. Pushes back. Asks better questions. Refuses to do the work for you.

That distinction is the whole assignment. The folder you're looking at is one attempt at solving it — built research-first, with the methodology surfaced as a portfolio asset alongside the coach.

## Receipts

This coach is built on inspectable proof, not authorial intuition. The receipts ship in the deliverable:

- **[`process/FRAMEWORK.md`](process/FRAMEWORK.md)** — the canonical triangulated source of truth. Every refusal, gate, failure pattern, and verbatim language token is tagged 3/3, 2/3, or 1/3 by cross-AI agreement on cited research. The conflicts surfaced across sources are recorded inline.
- **[`process/RESEARCH_EXTRACTS/`](process/RESEARCH_EXTRACTS/)** — 7 structured extracts from independent AI research passes (Gemini deep-think + deep-research + coaching-framework; Claude deep-research + coaching-framework; ChatGPT deep-research + coaching-framework). The raw evidence the triangulation table is built from.
- **[`process/JUMPED_THE_GUN_AUDIT.md`](process/JUMPED_THE_GUN_AUDIT.md)** — consolidated audit of an earlier pre-research build (the "JTG donor") run against FRAMEWORK. 20 files scored: 2 KEEP, 7 MODIFY, 1 DISCARD, 4 DEFER, 1 DEFER-TO-MU, 5 OUT-OF-SCOPE. The methodology demonstrably changed our minds — that's the credibility artifact.
- **[`ASSESSOR_GUIDE.md`](ASSESSOR_GUIDE.md)** — 5 adversarial prompts a judge can run in 60 seconds. Expected behavior signatures and named failure modes for each.
- **[`PROOF.md`](PROOF.md)** — one live stress test (ASSESSOR_GUIDE Prompt 1, termination-script demand) annotated moment-by-moment. The headline catch: during live roleplay, the coach stopped the manager mid-sentence when they answered "Walker"'s monitoring-software question in detail — flagging that the answer belongs in HR's documentation, not in the termination meeting, and re-running the exchange until the manager held the correct redirect. The session also caught an inconsistent-standards risk (manager singling out one report for team-wide deadline pressure), four trait labels, two hearsay attempts, and forced one cleanly-drafted, observable termination opening. Other behavioral runs (Prompts 2 & 3) showed the same patterns under different pressure shapes. Prompt 5 (skip-roleplay bargain) was not independently re-run in this round; the assessor protocol is fully re-runnable by any judge in a fresh project.

## Manager Practice Lab — the planned suite

Hard Conversations Coach is **Module 01** of a deliberately scoped suite — **Manager Practice Lab** — built on the same triangulation methodology. Each module ships as its own ICM folder. Scope discipline is intentional: shipping a tight floor build and naming the boundary is part of the deliverable.

Subsequent modules are in development and held under the license terms below. Inquiries about the roadmap, pilots, or commercial use: **wcvessels@gmail.com**.

---

## License

**Creative Commons Attribution-NonCommercial 4.0 International (CC BY-NC 4.0).** See [`LICENSE`](LICENSE) for full terms.

In plain English:

- **Personal, educational, and research use:** free. Use it, adapt it, share it, build on it. Attribution required (credit the author and link back to this repository).
- **Commercial use** — including but not limited to embedding this work in paid products, internal use by for-profit organizations, training commercial AI systems on it, or reselling access — **requires a separate written license from the author**.
- **Commercial licensing inquiries:** wcvessels@gmail.com.
- **No warranty.** This is not legal advice, HR advice, or therapy. See [`reference/escalation_and_safety.md`](reference/escalation_and_safety.md) for the coach's own declared limitations and routing rules.
