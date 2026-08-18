# EU AI Act Approval Pack — Kimia Asgari

## Overview
This repository contains the deliverable for the EU AI Act consulting lab: a hidden client-scenario exercise where two partners each write four disguised client use cases (one per risk tier), swap them, and produce a full consulting approval pack as if advising a real client.

## Files

| File | Contents |
|---|---|
| `pv_answer.md` | Private answer key — my four hidden client scenarios with the true intended risk category and reasoning for each (kept hidden from my partner during the exercise). |
| `consulting-usecases.md` | The four hidden client use cases as sent to my partner, with all category labels removed — written to look like realistic, slightly messy client discovery-call briefs. |
| `consulting-response.md` | My consulting review as first-pass classifier — analysis of my **teammate's four use cases** (not my own), classifying each into a risk tier, proposing an AI architecture, mapping provider/deployer/vendor roles, and listing required obligations/controls, done without seeing their answer key. |
| `Phase3-EU-AI-ACT-approval.md` | The formal 3-page approval pack based on my analysis of my teammate's use cases: executive summary, per-case architecture and compliance implications, and a final decision (Approve / Approve with controls / Deny and redesign) for each. |
| `Phase4-closing-note.md` | Outcome of the live client discussion with my teammate: comparison of my inferred categories against their private answer key, and a closing reflection on what did or didn't change after the conversation. |

## Lab Workflow

1. **Phase 1 (`pv_answer.md` + `consulting-usecases.md`):** I wrote four hidden client scenarios — one prohibited, one high-risk, one limited-risk/transparency, one minimal-risk — and kept the true categories private.
2. **Phase 2 (`consulting-response.md`):** I received my teammate's four hidden scenarios and produced a first-pass risk classification and architecture recommendation for each, without seeing their answer key.
3. **Phase 3 (`Phase3-EU-AI-ACT-approval.md`):** I turned that analysis into a formal approval pack with role mapping, required controls, and a launch decision per case.
4. **Phase 4 (`Phase4-closing-note.md`):** My teammate and I compared my inferred classifications against their real answer key and discussed the results.

## My Teammate's Use Cases (summarized)
1. Retail bank loan-scoring tool using social media/browsing data, with auto-rejection and no human review
2. Hospital ER triage tool with nurse override before action
3. E-commerce support chatbot that some customers mistake for a human agent
4. Design agency tool suggesting color palettes/font pairings, with full designer review

## Key Takeaway
The most instructive case was the loan-scoring tool: the underlying use case (credit scoring) is legitimate and regulatable under Annex III, but the missing human-oversight step made it non-compliant as designed. Distinguishing "needs a redesign" from "is prohibited" was the core consulting judgment call in this exercise.