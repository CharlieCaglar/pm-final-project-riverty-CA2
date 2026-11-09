# AI Synthesis, Product Health & Insights Summary (Module 2)

## Responses
- **Assumption to validate #1:** Consumers have difficulty understanding what instalment plan they can realistically afford.
- **Assumption to validate #2:** Consumers leave the digital journey and contact an agent when the process becomes unclear or difficult.
- **Assumption to validate #3:** Some consumers create instalment plans but later miss payments because the plan was not sustainable.
- **Moment of misery / red flag #1 (e.g., “user gave up after 3 tries”):** Consumers may leave the journey because the income question is unclear and they do not understand why the information is needed.
- **Moment of misery / red flag #2:** Consumers may choose a plan that looks right but is not actually affordable, leading to missed payments later.
- **Moment of misery / red flag #3:** When consumers move from digital to an agent, the agent cannot see what they already entered, so the consumer has to repeat the same information.
- **Product Health & Insights Summary (Claude's output):** Product Health & Insights Summary

Based on 12 interview notes and 8 technical tickets. Both sources are illustrative sample data, not Riverty research.

Executive Summary

The core platform is largely functional: the issues in the data are rarely outright outages, but gaps in data integrity, sequencing, and information design. Those gaps are felt most sharply by consumers in financial difficulty, who are asked for sensitive information without context and then commit to plans they cannot sustain. The resulting failures (abandoned journeys, missed instalments, broken plans, repeat calls) surface downstream in agent workload and client complaint reporting, so technical stability and user experience are one problem here, not two.

Thematic Synthesis
1. Technical Stability & Data Integrity

Narrative: Most defects are not crashes. They are silent failures that interrupt a journey at a vulnerable moment or give the consumer conflicting information. The largest quantified issue is document upload failure, which affects a large share of journeys. The portal-versus-letter discrepancy is concentrated in purchased portfolios, which points to an upstream data-consistency problem more than a front-end defect. Portfolio data quality varies by source, so some inconsistency is structural.

Income document upload times out on mobile (T-201): 853 journeys in the sample month requested a document that never arrived. Severity: Critical
Portal amount differs from the letter (T-203, N-07): 531 journeys affected, 343 of them purchased portfolios. This directly erodes trust and causes consumers to stall until someone explains. Severity: Critical
Reminder before first instalment sent after the due date in some cases (T-207): Compounds missed-payment risk, which consumers already report experiencing (N-02). Severity: High
Back button on the plan review screen clears affordability answers (T-204): Forces re-entry of sensitive data and risks abandonment. Severity: Medium
Inconsistent acquired-portfolio data, including unreliable phone and address history (N-11): A structural constraint on consistency and on any downstream automation. Severity: High
2. Onboarding & Journey Design

Narrative: The journey assumes a single claim, a stable income, and uninterrupted time, none of which holds for the consumers described. Shift workers, people with multiple claims, and people in tight financial circumstances all hit friction at the point where the journey requests information or asks them to choose. Consumers abandon with an intent to return, so incomplete journeys are likely deferred rather than lost, but nothing in the data shows a mechanism that supports resumption.

Claims handled one at a time, with no combined plan (T-202, N-03): Consumers with multiple claims cannot see the full picture or judge the effect of paying one. Severity: High
Ambiguous income question (N-01): Unclear whether “income” means current or typical, leading to abandonment. Severity: High
Plan selection by shortest term (N-02): Consumers default to the lowest month count without a visible affordability signal, then miss payments. Severity: High
No clear way to resume an abandoned journey (N-01): Inferred from consumer behavior, not a confirmed defect. Severity: Medium
3. Trust & Clarity

Narrative: Consumers are being asked to disclose sensitive financial information without being told why it is needed, how it will be used, or what the consequences of a decision are. The prevailing emotion is fear of making a mistake or of data being used against them. The chat channel adds speed but compounds the problem by confirming plans without explaining their consequences. Compliance has signaled that any decision logic will need to be explainable to both consumers and agents, so this theme is a regulatory concern as well as a UX one.

No explanation of why income is requested or how long it is retained (T-206, N-06): Drives hesitation and fear of misuse. Severity: High
Chat confirms plans without showing missed-payment consequences (T-208, N-05): Consumers commit without understanding the downside. Severity: High
Uncertainty about whether paying one claim stops contact on another (N-03): Reflects missing cross-claim communication. Severity: Medium
Preference for phone contact to learn cost implications (N-04): Indicates the digital journey does not answer the “will this cost me more?” question. Severity: Medium
Explainability requirement for decisions (N-12): Not a defect today, but a constraint on how any future decisioning must be designed. Severity: Medium
4. Support Load & Agent Enablement

Narrative: The digital and agent channels are disconnected. Information consumers provide online is invisible to agents, so calls begin with repeated questions, and plan failures cannot be diagnosed because the rationale for an offer is not recorded in the agent view. This inflates handling time and prevents learning from failed plans. The effect reaches clients, who track complaints alongside recovery, and a rise in broken plans appears in their reporting.

Agent screen shows neither online entries nor plan rationale (T-205, N-08, N-09): Causes duplicate data collection and prevents root-cause analysis of failed plans. Severity: High
Broken plans visible in client reporting (N-10): A reputational and contractual exposure, as clients weigh complaints alongside recovery. Severity: High
Consumers falling back to phone when digital answers are insufficient (N-04, N-07): Shifts volume to the more expensive channel. Severity: Medium
Minor Technical Debt

No additional low-priority items were identified beyond those above; the back-button state loss (T-204) is the closest candidate and is rated Medium given its effect on sensitive data entry.

Cross-Cutting Observation

Several themes share a root cause: the journey collects information and commits consumers to plans without carrying context forward, to the consumer (why, and what happens next), to the agent (what was entered and why), or to the client (how the plan performs). The amount discrepancy, the upload failure, and the missed-payment reminder timing are the points where the data most clearly shows that gap turning into measurable failure.

Note on evidence strength: the technical tickets carry volume figures for only two issues (T-201 and T-203). Severity ratings for the rest rest on qualitative interview evidence from a small sample and should be validated against operational data.
- **Did the AI catch the specific moment of misery / pain point you found in Step 1?:** Yes. It caught the main problems I found: confusion around income information, consumers choosing plans they may not be able to keep, and information being lost when the consumer needs help from an agent.
- **Did it smooth over a critical frustration into a generic bullet point?:** A little. It identified the affordability problem, but I think the bigger issue is that creating a plan can look successful even when the consumer cannot actually keep the plan.
- **Did the AI try to suggest features or a roadmap despite the constraints?:** No. It stayed focused on the evidence and grouped the problems without suggesting new features or creating a roadmap.
- **Logic leak / hallucination #1 (e.g., “AI suggested a new search bar feature, roadmap leak”):** The AI assumed there is no clear way to resume an abandoned journey. The interview only says that the consumer closed the journey and planned to come back. We need more evidence before we can say that resuming the journey is a product problem.
- **Logic leak / hallucination #2:** The AI assumed that the difference between the portal amount and the letter amount is mainly an upstream data problem. The evidence confirms there is a mismatch, but it does not tell us where the technical problem actually comes from.
