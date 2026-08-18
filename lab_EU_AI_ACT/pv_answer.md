
## Private Answer Key (Hidden from Partner)

This file contains the true intended risk category for each of the four client scenarios sent to my partner (see `consulting-usecases.md` for the label-free version they actually received).

## Answer Key Table

| Case | Client brief for partner | Intended category | Why |
|---|---|---|---|
| 1 | Retail loyalty app — "customer trust index" | Prohibited | Uses a behavioral/social "trust score" that leads to detrimental treatment in an unrelated context (denying returns, flagging to security) — Article 5(1)(c) social scoring, applies to private companies too, not just governments. |
| 2 | Staffing agency — automated CV ranking | High-risk | Automated CV filtering that eliminates 70% of applicants before human review falls under Annex III (employment — recruitment/selection); the "human sees the rest" doesn't cover the auto-rejected pool, so genuine human oversight (Art. 14) is missing. |
| 3 | Insurance company — customer-facing chatbot | Limited risk / transparency | LLM-based chatbot answering policy questions with no autonomous decision-making power; core issue is Article 50 — must disclose it's AI, since a user could otherwise mistake it for a human agent. |
| 4 | E-commerce retailer — product recommendation widget | Minimal risk | Static, non-dynamic product recommendations based on browsing/purchase history — no profiling with legal/significant effect, no dynamic pricing. Falls outside AI Act obligations, though GDPR/ePrivacy issues remain relevant to flag. |

---

## Full Scenario Text (as sent to partner, label removed)

### Case 1 — Intended category: Prohibited

A mid-sized German retail chain (home goods, ~40 stores) is launching a new loyalty app. The app tracks in-store purchase patterns, app engagement (how often customers open it, how long they browse before buying), and — through an optional social login — some public social media activity. The marketing team wants to build a "customer trust index" from this data. Customers with a high index get early access to sales and better coupons. Customers with a low index get flagged internally: store staff are notified to apply stricter scrutiny on return requests from these customers, and the index is also shared with a partner logistics company to deprioritize delivery slots for low-index customers. No customer sees their own score or knows it exists. The retail director wants to know if this is "just smart marketing" before they build it.

### Case 2 — Intended category: High-risk

A staffing agency serving mid-size manufacturing clients across the EU is overwhelmed with applications — sometimes 800+ CVs for a single role. They want an AI tool that reads incoming resumes, extracts skills and experience, and automatically ranks candidates. The system would auto-reject the bottom 70% of applicants (those never reach a recruiter), and the top 30% get forwarded to a human recruiter, who reviews and makes the final call. The agency's leadership is proud that "a human always makes the final hiring decision" and wants to know if this setup is fine to launch next quarter, since it will cut screening time from days to minutes.

### Case 3 — Intended category: Limited risk / transparency

An insurance company wants to deploy a