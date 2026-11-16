# Affordability check before the plan options (B3)

> For consumers who cannot pay their full balance at once, we help them create a clear, affordable instalment plan they can actually keep, with easy access to an agent when needed.

**Caglar Acar · PM Cohort 2** · https://github.com/CharlieCaglar/pm-final-project-riverty-CA2

Prototype: 04-roadmap/prototype.html

---

## Final Project Deliverables

### Slide 5 · Strategy
- **Problem:** Consumers who cannot pay their balance in full are struggling to confidently create sustainable instalment plans digitally, causing avoidable agent contact and putting both recovery performance and Riverty's self-service ambition at risk.
- **Value proposition:** A clear digital instalment journey that helps consumers understand their situation, agree to a plan they can realistically keep, and reach an agent seamlessly when needed. This improves sustainable recovery and reduces avoidable agent contact.
- **Hypothesis:** Evidence: only 22% of portal visitors start the instalment journey, 46% of started journeys end in an agreement, and 19% of new agreements miss a payment within 60 days (22.5% for consumers with variable or shift income). Consumers with 3 or more open claims have only a 27.6% agreement rate. Hypothesis: adding an affordability check before the plan options will raise the share of new agreements with no missed payment within 60 days by 3 percentage points (81% to 84%), while agent contact within 7 days stays below 33.0%.

### Slide 6 · Research
- **Competitive analysis:** Persona: a consumer in financial difficulty who cannot pay the full balance at once and needs an instalment plan. No external tools are supported by the research. The main workaround is calling an agent when the digital journey does not give enough clarity, and 31.0% of journey starters contact an agent within 7 days. Evidence: N-02 chose the shortest plan because it looked right and missed the second payment. N-04 preferred calling because a person could explain the cost. N-08 shows agents have to ask again for information consumers already entered online.
- **Journey map:** Start the digital instalment journey → try to work out what is affordable → unsure why income is asked → guess a plan, leave, or call an agent (moment of misery) → repeat the same information to the agent → agree to a plan that may not be sustainable. Where the solution intervenes: an affordability check before the plan options explains why income is asked and shows only plans the consumer can keep.

### Slide 7 · Blueprint
- **Roadmap:** Persona: a consumer in collections who cannot pay their outstanding balance in full. Primary metric: % of new agreements with no missed payment within 60 days. Guardrail: agent contact within 7 days. I overrode the AI on B1 (multi-claim journey), raising its value from 3 to 4 because consumers with 3+ open claims have only a 27.6% agreement rate. Now lane: B2 (explain why income is asked), B3 (affordability check), B6 (payday-aligned dates). Cut: B7, because it can push consumers toward higher monthly payments, and B8 (chat assistant on every page), because there is no evidence it solves the affordability problem.
- **PRD highlights:** Feature: B3 Affordability check before the plan options. Must-haves: (1) simple form with monthly income and essential costs; (2) calculate an affordable monthly limit; (3) show only plans within the limit; (4) edit the numbers and recalculate; (5) if no plan fits, offer agent support; (6) short explanation of why income is needed. Won't (now): multi-claim plans, open-banking verification, credit scoring, chat assistant, agent tooling. Safety guard: never show a plan above the limit, never present the result as financial advice. Evals: 100% of displayed plans within the limit, plan options reached within 2 minutes, 100% of no-fit cases offer agent support. Prototype: 04-roadmap/prototype.html. The prototype exposed a gap: the PRD did not define how the limit is calculated, so the sample rule is 70% of income minus essential costs.
- **Prototype:** 04-roadmap/prototype.html

### Slide 8 · Validation
Hypothesis: adding an affordability check before the plan options raises the share of new agreements with no missed payment within 60 days by 3 percentage points (81% to 84%). Control: today's journey with the existing plan terms and no affordability signal. Variant: control plus the B3 affordability check, one change only. Primary metric: no missed payment within 60 days, baseline 81%, MDE 3 points. Guardrail: agent contact within 7 days, baseline 31.0%, investigate at 33.0%. Sample: 2,518 agreements per arm, 50/50 split, 6 weeks of enrolment plus 60 days of follow-up, read at day 102, p < 0.05. SHIP if lift is at least 3 points and the guardrail holds. ITERATE if the lift is positive but below 3 points. KILL if there is no improvement.

### Slide 9 · Launch
- **GTM:** Goal: conversion. Audience: consumers who start the instalment journey in the portal, 8,360 per month (22% of 38,000 portal visitors), 78.5% on mobile. Tier: M (targeted), because the feature changes the journey for every starter and agents need briefing, but no external campaign is needed. Channels: (1) owned, the instalment journey in the portal; (2) owned, existing outreach messages to 100,000 consumers a month; (3) earned, client reporting and reviews. Enablement: agent one-pager, 3-minute demo, consumer FAQ, escalation path, compliance-approved wording.
- **Metrics:** Metrics: (1) share of new agreements with no missed payment within 60 days, 81% today, target 84% or more; (2) share of started journeys that end in an agreement, 46.0% today, must not fall below 43.0%; (3) agent contact within 7 days, 31.0% today, must stay below 33.0%. Bad signal: the no-missed-payment rate rises but the agreement rate drops sharply, meaning the feature only filters people out, or agent contact reaches 33.0%. Most likely post-launch decision: iterate, because the 70% rule is only a sample.

### Slide 10 · Story
- **Friction + aha:** The hardest part was that my first idea of success was wrong. In M3 I measured success as the agreement rate, but my feature only shows plans the consumer can afford, so it could lower agreements on purpose. The aha moment came in the experiment brief: the real goal is plans consumers keep, so I switched to the share of new agreements with no missed payment within 60 days. A second friction point was that the prototype crashed on a single apostrophe in the code, which taught me to test a prototype before trusting it.
- **Takeaways / next:** Takeaways: (1) define success as an outcome the consumer benefits from, not a count of sign-ups; (2) a guardrail can be tripped by the feature itself, because sending consumers with no fitting plan to an agent may raise agent contact; (3) a 60-day metric needs a 60-day follow-up, so test length depends on the metric. Next: run the A/B test, replace the sample 70% rule with a compliance-approved affordability rule, test plan ordering so the most comfortable plan appears first, and later add multi-claim support, where agreement is only 27.6%.

---

Submitted to the Product Management Certification learning platform · Product School.
