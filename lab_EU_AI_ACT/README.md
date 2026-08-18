# EU AI Act Approval Pack — Kimia Asgari

## Overview
This repository contains the deliverable for the EU AI Act consulting lab: a hidden client-scenario exercise where two partners each write four disguised client use cases (one per risk tier), swap them, and produce a full consulting approval pack as if advising a real client.

---

## Setup / First Run

This document is split into two parts as required: **Private Answer Key** and **Consulting Response**.

- The **Private Answer Key** — four scenario headings (Case 1: Prohibited, Case 2: High-risk, Case 3: Limited risk/transparency, Case 4: Minimal risk), each with a short client use case, the true category, and reasoning — is in [`pv_answer.md`](./pv_answer.md).
- The **Consulting Response** version — the same four case descriptions with all category labels removed, exactly as shared with my partner — is in [`consulting-usecases.md`](./consulting-usecases.md).

**Expected output confirmed:** Four case shells were drafted, each with a client need, the proposed AI behavior, and the people affected. No category labels or clues were included in the version sent to my partner.

---

## First Step

Below are my four client briefs, each 5–7 lines, one per target category. The real category for each is recorded only in `pv_answer.md`; the version below is what was actually shared with my partner, with all labels removed.

**Case 1 (real category: Prohibited):**
A mid-sized German retail chain (home goods, ~40 stores) is launching a new loyalty app that builds a "customer trust index" from purchase patterns, app engagement, and social login data. Low-index customers face stricter return scrutiny and deprioritized delivery. No customer sees their own score.

**Case 2 (real category: High-risk):**
A staffing agency receives 800+ CVs per role and wants an AI tool that auto-rejects the bottom 70% of applicants before any recruiter sees them; only the top 30% reach a human for final review.

**Case 3 (real category: Limited risk / transparency):**
An insurance company wants a customer-facing chatbot, built on a third-party LLM, with a human name and warm tone, that cannot make binding decisions but that many customers don't realize is a bot.

**Case 4 (real category: Minimal risk):**
An online retailer wants a "customers who bought this also liked" widget powered by a lightweight AI model using browsing/purchase history, with no personalized pricing.

Full text of all four cases: [`consulting-usecases.md`](./consulting-usecases.md).

---

## 1. Recognize

Four hidden client cases were created, one for each required outcome:

- **Prohibited** — Case 1 (retail "trust index" leading to detrimental treatment in an unrelated context — Article 5(1)(c) social scoring)
- **High-risk** — Case 2 (automated CV auto-rejection with no human review of the rejected pool — Annex III employment)
- **Limited risk / transparency** — Case 3 (chatbot mistaken for a human — Article 50)
- **Minimal risk** — Case 4 (static, non-personalized recommendation widget)

Full reasoning for each: [`pv_answer.md`](./pv_answer.md).

---

## 2. Apply

Swapped briefs with my partner and classified each of their four cases from the business facts alone, without seeing their answer key. Full first-pass classification table, including architecture and role mapping: [`Phase2-Review_your_partner_as_the_consultant.md`](./Phase2-Review_your_partner_as_the_consultant.md).

Summary of my first-pass calls on my partner's cases:

| Case | My Classification |
|---|---|
| 1 — Loan scoring bank | High-risk (Annex III, 5(b)) |
| 2 — ER triage tool | High-risk |
| 3 — E-commerce chatbot | Limited risk / transparency |
| 4 — Design agency palette tool | Minimal risk |

---

## 3. Integrate

For each of my partner's four cases, I proposed a specific AI architecture and operating model — system behavior, inputs, human-in-the-loop point, provider/deployer/vendor roles, and required controls. See the **Proposed AI Architecture** and **Provider / Deployer / Vendor** columns in [`Phase2-Review_your_partner_as_the_consultant.md`](./Phase2-Review_your_partner_as_the_consultant.md).

---

## 4. Verify

A consulting decision (Approve / Approve with controls / Deny and redesign) was issued for each case, matching the AI Act logic identified in Phase 2. Full approval pack with executive summary, per-case compliance implications, and redesign path: [`Phase3-EU-AI-ACT-approval.md`](./Phase3-EU-AI-ACT-approval.md).

| Case | Decision |
|---|---|
| 1 — Loan scoring | Deny and redesign |
| 2 — ER triage | Approve with controls |
| 3 — Support chatbot | Approve with controls |
| 4 — Design tool | Approve |

---

## 5. Debrief

My partner and I compared my inferred classifications against their private answer key — all four matched exactly. Full outcome, comparison table, and closing reflection on what changed after the client discussion: [`Phase4-closing-note.md`](./Phase4-closing-note.md).

---

## Files

| File | Contents |
|---|---|
| `pv_answer.md` | Private answer key — my four hidden client scenarios with the true intended risk category and reasoning for each. |
| `consulting-usecases.md` | The four hidden client use cases as sent to my partner, with all category labels removed. |
| `Phase2-Review_your_partner_as_the_consultant.md` | First-pass consulting review of my partner's four use cases — classification, architecture, roles, obligations, decision. |
| `Phase3-EU-AI-ACT-approval.md` | Formal 3-page approval pack: executive summary, per-case compliance implications, and final decision for each of my partner's cases. |
| `Phase4-closing-note.md` | Outcome of the live client discussion with my partner and closing reflection. |

## My Partner's Use Cases (summarized)
1. Retail bank loan-scoring tool using social media/browsing data, with auto-rejection and no human review
2. Hospital ER triage tool with nurse override before action
3. E-commerce support chatbot that some customers mistake for a human agent
4. Design agency tool suggesting color palettes/font pairings, with full designer review

## Key Takeaway
The most instructive case was the loan-scoring tool: the underlying use case (credit scoring) is legitimate and regulatable under Annex III, but the missing human-oversight step made it non-compliant as designed. Distinguishing "needs a redesign" from "is prohibited" was the core consulting judgment call in this exercise.

---

## Reinforce

**Borderline arguments / counter-arguments:**

- **Case 1 (Loan scoring):** A counter-argument could be that the bank might claim the social/browsing signals are only used to *supplement*, not replace, financial underwriting — this doesn't change the Annex III classification, but it's the kind of argument a client will actually make, and it doesn't resolve the missing human-oversight defect regardless.
- **Case 2 (ER triage):** One could argue the tool is "advisory only" since a nurse can override — but this only holds if the override is genuine and not a rubber stamp under time pressure in an ER setting, which is worth flagging as an operational risk, not just a paper compliance issue.
- **Case 3 (chatbot):** A counter-argument is that the bot never makes a binding decision, so transparency alone should suffice — this is correct under the current design, but if the bot's scope quietly expands to influence claims outcomes later, the classification would need to be revisited.
- **Case 4 (design tool):** Someone could argue this is "obviously minimal risk" and needs no review at all — true for the AI Act, but the IP/licensing question on the underlying generative model's training data still needs a legal check.

**Where legal should verify the final interpretation:**
- Case 1: whether the specific data fields used (social/browsing) trigger Article 9 GDPR special-category concerns depending on what can be inferred from them.
- Case 2: whether "critical infrastructure" or another Annex III category is the more precise fit for hospital triage, since healthcare isn't named as cleanly as employment or credit scoring.

**Next operational artifact needed:**
- Case 1: a FRIA draft, since Annex III 5(b) makes it mandatory before go-live.
- Case 2: a logging and override-documentation policy for the triage tool.

---

## Stretch — Mini Implementation Roadmap (Case 1: Loan Applicant Scoring Tool)

**What the provider needs before market placement:**
- Completed conformity assessment (Annex VI internal control route)
- Technical documentation package (Annex IV): system design, training data sources, bias-testing methodology across demographic groups
- CE marking and EU Declaration of Conformity
- Registration in the EU AI public database

**What the deployer (the bank) needs before first use:**
- A completed Fundamental Rights Impact Assessment (FRIA) — mandatory under Article 27 for Annex III 5(b) credit-scoring deployers
- A documented human oversight process: mandatory human loan officer review before any rejection, not just visibility into the score
- Log retention infrastructure meeting the 6-month minimum (Article 12)
- Staff training on how and when to override or escalate a flagged application

**Evidence to request from the vendor (if using a third-party scoring engine):**
- Proof of completed conformity assessment and technical documentation
- Bias-testing results broken down by protected demographic groups
- Documentation on what data fields feed the model, to assess necessity/proportionality of social/browsing signals
- Incident-reporting process and contractual commitment to the Article 73 reporting timelines (15 days default / 2 days for widespread infringement)
