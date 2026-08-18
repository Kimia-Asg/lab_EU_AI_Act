# LAB | EU AI Act consulting lab

# Use Cases

Case 1
A mid-sized German retail chain (home goods, ~40 stores) is launching a new loyalty app. The app tracks in-store purchase patterns, app engagement (how often customers open it, how long they browse before buying), and — through an optional social login — some public social media activity. The marketing team wants to build a "customer trust index" from this data. Customers with a high index get early access to sales and better coupons. Customers with a low index get flagged internally: store staff are notified to apply stricter scrutiny on return requests from these customers, and the index is also shared with a partner logistics company to deprioritize delivery slots for low-index customers. No customer sees their own score or knows it exists. The retail director wants to know if this is "just smart marketing" before they build it.

Case 2
A staffing agency serving mid-size manufacturing clients across the EU is overwhelmed with applications — sometimes 800+ CVs for a single role. They want an AI tool that reads incoming resumes, extracts skills and experience, and automatically ranks candidates. The system would auto-reject the bottom 70% of applicants (those never reach a recruiter), and the top 30% get forwarded to a human recruiter, who reviews and makes the final call. The agency's leadership is proud that "a human always makes the final hiring decision" and wants to know if this setup is fine to launch next quarter, since it will cut screening time from days to minutes.

Case 3
An insurance company wants to deploy a customer-facing chatbot on their website, built on top of a third-party LLM API, to answer common questions about policy coverage, claims status, and premium calculations. The bot is scripted to sound warm and conversational, using a first-person tone ("I can help you with that!") and a human-sounding name ("Anna"). It cannot approve claims, change policies, or make binding decisions — it only provides information and routes complex questions to a live agent. The product team likes that customers "don't even realize it's a bot most of the time" because it reduces frustration, and wants to know what, if anything, needs to change before launch.

Case 4
An online home-goods retailer wants to add a "customers who bought this also liked" recommendation widget to their product pages, powered by a lightweight AI model trained on aggregate browsing and purchase history (not tied to named individuals in the front-end display, though the backend does use account-level history for logged-in users). The system doesn't personalize pricing — every customer sees the same price for the same item — it only reorders which products are shown first. The team already has a cookie consent banner in place for analytics and wants to know if this recommendation feature needs any additional sign-off before shipping.
