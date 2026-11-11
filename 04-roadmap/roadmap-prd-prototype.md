# Roadmap, PRD & Prototype (Module 4)

## Your strategic anchors
- **Persona (M2), who are you solving for?:** A consumer in collections who cannot pay their outstanding balance in full.
- **Primary success metric (M3), your leading indicator:** Percentage of new instalment agreements with no missed payment within 60 days.
- **Moment of misery (M2), the specific friction blocking the goal:** The consumer struggles to find an instalment plan that fits their financial situation and may abandon the process or agree to a plan they cannot maintain.
- **Guardrail metric (M3), what must not drop or break:** Agent contact rate within 7 days

## Scan the backlog & set a human baseline
- **My instinctive “quick wins” before touching the AI (2 to 3 feature IDs + why):** B2, B4 and B6. B2 looks like a quick win because it can reduce confusion around why income information is needed with relatively low effort. B4 can improve the handoff to an agent and avoid consumers repeating the same information. B6 can help consumers choose a payment date that better fits their income timing and may help them keep the plan.

## Audit, override & decide
- **Where did you override the AI? (feature + old vs. new score + why):** I changed B1 from Value 3 to Value 4 because our M3 data showed that consumers with multiple open claims have lower agreement rates, so I think this problem is more important than the AI originally suggested.
- **Did the AI over-value a Sales/Eng request your M2 interviews don’t support?:** B8, the chat assistant on every portal page, does not have strong evidence that it solves our main affordability problem, so I decided to cut it.
- **Did it underweight something your M3 cohort/funnel data strongly supports?:** Yes. B1 was underweighted because our M3 data showed that consumers with multiple open claims have lower agreement rates. This gives us stronger evidence that the multi-claim journey needs attention.

## Generate your interactive roadmap
- **My “Now” lane (this sprint), the 2 to 3 quick wins I’ll build first:** B2, B3 and B6. First explain clearly why income information is needed, then help consumers choose an affordable plan, and allow them to select a payment date that better fits their income timing.
- **What I cut, and the “no” I’m protecting the scope from:** I cut B7 and B8. B7 can push consumers toward higher monthly payments, which works against our goal of sustainable plans. B8 is a broad solution without strong evidence that it solves our main affordability problem.
- **Prototype/roadmap screenshot link (paste into your deliverables):** https://github.com/CharlieCaglar/pm-final-project-riverty-CA2/tree/main/04-roadmap
