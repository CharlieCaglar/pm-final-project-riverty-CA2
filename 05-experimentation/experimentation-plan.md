# Experimentation Plan (Module 5)

## Get your documents ready
- **From M3, your hypothesis sentence:** Based on qualitative evidence that consumers struggle to create an instalment plan they can realistically keep, and quantitative evidence showing an agreement rate around 46% and a 60-day missed-payment rate of 19%, I believe that making it easier for consumers in collections to create an affordable and sustainable instalment plan will increase the agreement rate by at least 10%. I will protect the 60-day missed-payment rate from increasing and make a go/no-go decision after 3 months.
- **From M3, your primary success metric & guardrail metric:** Primary success metric: Percentage of new instalment agreements with no missed payment within 60 days.
Guardrail metric: Agent contact rate within 7 days.
- **From M4, the feature you scoped in your PRD this is what you're testing:** B3 - Affordability check before the plan options. The consumer enters monthly income and essential monthly costs, the system calculates an affordable monthly payment limit and shows only the plans within that limit. The consumer can edit the numbers and recalculate. If no plan fits, the journey offers agent support instead of an unaffordable plan.

## Define your experiment parameters
- **Feature under test pull from your M4 PRD:** B3 - Affordability check before the plan options
- **Persona pull your M2 persona:** A consumer in collections who cannot pay their outstanding balance in full
- **Expected outcome the behaviour change you expect, from your M3 hypothesis:** Consumers choose plans within what they can afford, so more new instalment agreements are kept without a missed payment
- **Primary success metric the one number that defines success, from M3:** Percentage of new instalment agreements with no missed payment within 60 days
- **Baseline rate today's rate of your primary metric, from your M3 data:** 81.0% of new agreements have no missed payment within 60 days (metric_baselines.csv: 19.0% miss a payment, measured on 3,846 new agreements per month)
- **Guardrail metric & boundary what must not break, and how far it can move before you investigate:** Agent contact rate within 7 days. Baseline 31.0% (metric_baselines.csv, measured on 8,360 journey starters per month). Investigate if it reaches 33.0% (an increase of 2 percentage points)
- **Minimum Detectable Effect (MDE) the smallest improvement worth shipping, your floor:** 3 percentage points (81% to 84%)
- **Sample size per arm use the calculator in the builder, baseline + MDE:** 2,518 agreements per arm (5,036 in total), at baseline 81%, MDE 3 percentage points, 80% power, 5% significance
- **Traffic split & test duration 50/50 standard · cover ≥ 2 weekly cycles:** 50/50 split. Enrol consumers for 6 weeks (about 887 new agreements per week, 5,300 in total, which covers the 5,036 needed), then follow each agreement for 60 days. Read date is day 102.
- **Significance threshold p < 0.05 is standard, explain any deviation:** p < 0.05

## Define your control and variant
- **Control (A) the current experience, reference your M2 moment of misery and M3 funnel/workflow data:** Today's journey. The consumer sees the existing plan terms (3, 6, 12, 18 and 24 months) with no affordability check and no signal of what they can afford. Evidence from M2: N-02 chose the shortest plan because it looked right and missed the second payment. N-04 phoned an agent because only a person could explain the cost.
- **Variant (B) your single change, copy the relevant screens & functional requirements from your M4 PRD:** Control plus one change: the B3 affordability check, copied from the M4 PRD.
Screen 1: explains why income information is needed, then asks for monthly income and essential monthly costs.
Screen 2: shows the calculated affordable monthly limit and only the plans within it, with an option to edit the numbers and recalculate.
Screen 3: confirms the chosen plan, or offers agent support if no plan fits.
Sample rule: affordable limit = 70% of (monthly income minus essential costs). A plan above the limit is never shown.
- **Isolation check, what has NOT changed? list everything identical between arms (app version, eligibility rules, notifications, onboarding). If something changed inadvertently, your test is compromised.:** Identical in both arms: plan terms, prices and fees, eligibility rules (all consumers who start the instalment journey, including those with multiple open claims), outreach and reminders, agent routing and agent tooling, app version, and the payment flow after confirmation. B2 (standalone income explanation) and B6 (payday date picker) are not live in either arm. Consumers are randomised 50/50 when they start the journey.

## Formalize your hypothesis & shipping criteria
- **Your hypothesis (filled in):** I believe that adding an affordability check before the plan options for consumers in collections who cannot pay in full will result in more consumers choosing plans they can keep, as measured by a 3 percentage point increase in the percentage of new agreements with no missed payment within 60 days (81% to 84%), within 102 days (42 days of enrolment plus 60 days of follow-up). We will protect the agent contact rate within 7 days throughout the test.
- **Your shipping criteria (filled in):** We will SHIP if the percentage of new agreements with no missed payment within 60 days improves by at least 3 percentage points at p < 0.05, and the agent contact rate within 7 days does not reach 33.0% after 102 days.

We will ITERATE if direction is positive but lift is below 3 percentage points.

We will KILL if the primary metric shows no improvement or moves negatively.

The read date is fixed at day 102, with no results reviewed before this date.
- **Hardest parameter to define, and did it change your hypothesis? quick debrief:** The hardest parameter was the primary metric. My M3 metric was agreement rate, but the feature only shows affordable plans, so it could lower the number of agreements by design. I switched to the percentage of agreements with no missed payment within 60 days, which measures whether plans are kept. The guardrail was also tricky, because sending consumers with no fitting plan to an agent may raise agent contact by design. I will watch agreement rate as a secondary signal.
