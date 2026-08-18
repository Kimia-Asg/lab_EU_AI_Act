## Phase 3 — Approval Pack

**Prepared for:** Partner (Client)
**Prepared by:** Kimia Asgari, AI Consultant


---

### Executive Summary

We reviewed four proposed AI use cases spanning credit scoring, clinical triage, customer support, and creative design assistance. The overall risk picture is mixed: one case (loan scoring) cannot launch as designed due to a critical gap in human oversight, even though the underlying use case itself is a legitimate, regulatable one — not a prohibited practice. One case (ER triage) is high-risk but already architected with genuine human oversight, so it can proceed with formal documentation and controls. One case (chatbot) is low-effort to fix — it simply needs a clear AI disclosure. One case (design tool) has no AI Act obligations at all. No case in this batch falls into a prohibited category, but the loan-scoring case is the one requiring a hard stop and redesign before it can move forward.

---

### Case 1 — Loan Applicant Scoring Tool

**Client need:** A retail bank wants faster loan approvals and fewer bad loans by scoring applicants using social media activity and browsing history alongside financial data, auto-rejecting "high risk" applicants with no human review.

**Inferred category:** High-risk (Annex III, point 5(b) — creditworthiness and credit scoring).

**Architecture & role map:** Financial data + social/browsing signals feed a scoring model → model outputs a risk flag → currently, high-risk flags trigger automatic rejection with no human in the loop. The bank is likely the deployer if using a third-party scoring engine, or the provider if the model is built in-house.

**Compliance implications:** Credit scoring is explicitly high-risk under Annex III. The auto-rejection design fails Article 14's human oversight requirement outright — this is not a borderline call. Using social media and browsing data (rather than only financial history) also raises proportionality and potential Article 9 GDPR concerns if any inferred signals touch protected characteristics. A FRIA is mandatory here, since Annex III 5(b) is a named Article 27 trigger.

**Decision: Deny and redesign.**

**Redesign path:** Insert a mandatory human loan officer review step before any rejection is finalized, particularly for borderline or negative scores. Reconsider whether social media data is necessary and proportionate to the purpose (data minimisation), and document a bias-testing and fairness review across demographic groups before re-submission.

---

### Case 2 — ER Triage Priority Tool

**Client need:** A hospital network wants an AI tool to read patient vitals and symptoms and suggest an ER priority level, with a nurse able to override the suggestion before action is taken.

**Inferred category:** High-risk (healthcare use directly affecting patient safety and access to essential services).

**Architecture & role map:** Vitals + symptoms feed the model → model suggests a priority level → nurse reviews and can override → final triage action taken by clinical staff. The hospital is deployer (if using a vendor tool) or provider (if built in-house).

**Compliance implications:** Unlike Case 1, this design already includes a real human-in-the-loop, which is what Article 14 requires — the nurse has genuine authority to override, not just visibility into the output. What remains is formalizing the compliance package: conformity assessment, technical documentation, accuracy/bias testing across patient demographics, and logging.

**Decision: Approve with controls.** Require documented conformity assessment, bias testing, 6-month log retention, and clear written instructions for clinical staff on how and when to override, before go-live.

---

### Case 3 — E-Commerce Support Chatbot

**Client need:** An e-commerce company wants a chatbot to answer order and return questions; some customers currently believe they're speaking to a real person.

**Inferred category:** Limited risk / transparency (Article 50).

**Architecture & role map:** Customer message → LLM (likely third-party API) generates a response → complex cases route to a human agent. The company is a deployer if using a third-party LLM, or provider if the bot is custom-built and delivered under their own name.

**Compliance implications:** The bot makes no binding decisions, so it does not rise to high-risk. However, customers mistaking it for a human is precisely what Article 50 is designed to prevent — an explicit AI disclosure is required.

**Decision: Approve with controls.** Add a clear, visible AI disclosure at the start of the chat or in the bot's introduction. No conformity assessment or registration needed.

---

### Case 4 — Design Palette & Font Suggestion Tool

**Client need:** A small design agency wants a tool that suggests color palettes and font pairings for client mockups, with designers reviewing and approving every suggestion.

**Inferred category:** Minimal risk.

**Architecture & role map:** Client brief/brand parameters → model suggests palette/font options → designer reviews and selects. The agency is a deployer of a likely third-party generative tool.

**Compliance implications:** No profiling, no consequential decision-making about individuals, full human review before any output is used. No AI Act obligations apply.

**Decision: Approve.** Flag one parallel, non-AI-Act item: confirm the licensing/IP terms of the underlying generative tool regarding training data and output ownership, since this affects the agency's ability to deliver cleared work to clients.

---

### Summary Table

| Case | Category | Decision |
|---|---|---|
| 1 — Loan scoring | High-risk | Deny and redesign |
| 2 — ER triage | High-risk | Approve with controls |
| 3 — Support chatbot | Limited risk / transparency | Approve with controls |
| 4 — Design tool | Minimal risk | Approve |
