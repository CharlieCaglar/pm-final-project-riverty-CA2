# GTM Strategy & Success Dashboard (Module 6)

## Get your prior work ready
- **The feature you're launching from your M4 PRD, one feature, not a list:** B3 - Affordability check before the plan options. The consumer enters monthly income and essential costs, the journey calculates an affordable monthly limit and shows only the instalment plans within it. If no plan fits, it offers agent support.
- **What your M5 experiment will test your hypothesis, primary metric and ship / iterate rule, the evidence the launch rests on:** Hypothesis: adding an affordability check before the plan options will raise the percentage of new agreements with no missed payment within 60 days by 3 percentage points (81% to 84%). Guardrail: agent contact within 7 days must stay below 33.0%. SHIP if the lift is at least 3 points at p < 0.05 and the guardrail holds. ITERATE if the lift is positive but below 3 points. KILL if there is no improvement. Read date is day 102. Evidence: 19.0% of new agreements miss a payment within 60 days (3,846 agreements per month), and N-02 chose the shortest plan and missed the second payment.
- **Your persona pull your M2 persona, this anchors your audience:** A consumer in collections who cannot pay their outstanding balance in full

## Set your goal, then your audience
- **Primary GTM goal awareness · engagement · conversion, pick one:** Conversion
- **Why this goal? what makes this the right goal for this feature right now:** The feature lives inside the existing instalment journey, so nobody needs to be made aware of it. The goal is to turn started journeys into agreements consumers can keep: 46.0% of started journeys end in an agreement, and 19.0% of new agreements miss a payment within 60 days.
- **Target audience the specific segment your goal implies, be precise:** Consumers who start the instalment journey in the portal: 8,360 per month (22% of 38,000 portal visitors). Existing users only, not new acquisition. 78.5% are on mobile (6,563), so the journey must work well on a phone.

## Size your launch
- **Launch tier S (minimal) · M (targeted) · L (multi-channel) · XL (full GTM):** M (targeted)
- **Justification reach + revenue impact + what silence would risk:** Reach: 8,360 consumers a month, all inside one existing journey. Impact: about 731 of 3,846 new agreements a month fail within 60 days, and a 3-point improvement keeps about 115 more plans a month. Risk of silence: agents would get questions about limited plan options without knowing why. Not L, because no external campaign is needed.
- **Is this a launch or a release? does it need go-to-market, or can it just ship?:** A targeted launch, not a silent release. It changes what every consumer sees in the journey and what agents must be able to explain, so it needs agent enablement and a controlled rollout after the A/B test. It does not need external marketing.

## Choose your top three channels and plan assets
- **Channel 1 owned / earned / paid, and why it reaches your audience:** Owned: the instalment journey in the portal. The consumers are already there, and screen 1 explains why income is asked.
- **Channel 2 owned / earned / paid, and why:** Owned: existing outreach messages (email, SMS, letter) to 100,000 consumers a month. After a SHIP decision, add one line such as "See plans that fit your budget". Outreach stays identical in both test arms.
- **Channel 3 owned / earned / paid, and why:** Earned: client (creditor) reporting and reviews. Clients track broken plans and complaints with recovery, so sharing the plan-kept rate builds their support. No paid channel: the audience is already in the portal, so ads add nothing.
- **Enablement & assets what Sales / CS / Support need, plus the assets to build (one-pager, demo, etc.):** Brief collection agents (assumption: 40 in the pilot team, not in the brief), support, compliance and client managers. Build: (1) one-page agent brief on what changed, how the limit is calculated and what to say when no plan fits; (2) 3-minute demo of the prototype; (3) consumer FAQ on why income is asked and that the result is not financial advice; (4) escalation path for consumers who want a plan above their limit; (5) compliance-approved wording for the income explanation and the 70% rule.

## Make it executable
- **Ownership named owner per key activity, individual, not department:** Caglar Acar (Product Manager) owns the plan, the A/B test and post-launch metrics. Engineering Lead owns the production build and 50/50 randomisation. Collection Operations Manager owns agent training. Compliance Officer approves the wording and the affordability rule. UX Writer owns consumer copy and FAQ. Data Analyst reads results at day 102.
- **Budget & resource gaps what costs extra, and any asset you can't currently build:** Costs extra: engineering time for production and tracking (estimate needed), about 40 hours of agent training (assumption), and compliance review. No paid media budget. Gaps: the real affordability rule is not defined (70% is a sample rule), and agents cannot yet see what the consumer entered online.
- **Timeline Phase 1 beta → Phase 2 launch moment → Phase 3 post-launch:** Weeks -4 to 0: build, compliance review, agent briefing. Phase 1 (beta, A/B test): 6 weeks of enrolment at 50/50, then 60 days of follow-up, read at day 102. Phase 2 (launch moment): if the result is SHIP, roll out to 100% of journey starters, with agents briefed the week before. Phase 3 (post-launch): check the three metrics weekly for 8 weeks, then add the line to outreach messages.

## Define how you'll know it worked
- **Success metrics 2 to 3 metrics that match your GTM goal:** 1. Share of new agreements with no missed payment within 60 days: 81% today, target 84% or more. 2. Share of started journeys that end in an agreement: 46.0% today, must not fall below 43.0%. 3. Agent contact within 7 days: 31.0% today, must stay below 33.0%.
- **Bad signal to watch for e.g. high reach, zero signups = message-market mismatch:** No-missed-payment rate rises but agreement rate drops sharply (the feature only filters people out), or agent contact reaches 33.0%.
- **Most likely post-launch decision double-down · iterate · pivot · deprioritize, and what would trigger it:** Iterate: the 70% rule is only a sample. Trigger: lift positive but below 3 points, or agent contact at 33.0%.
