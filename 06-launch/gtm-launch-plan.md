# GTM Launch Plan, Riverty BU Collection, A Fair Way Forward

| Field | Value |
|---|---|
| Feature | B3 - Affordability check before the plan options |
| Goal | Conversion |
| Launch tier | M, Targeted |

## Goal & Audience
- **Goal:** Conversion, The feature lives inside the existing instalment journey, so nobody needs to be made aware of it. The goal is to turn started journeys into agreements consumers can keep: 46.0% of started journeys end in an agreement, and 19.0% of new agreements miss a payment within 60 days.
- **Target audience:** Consumers who start the instalment journey in the portal: 8,360 per month (22% of 38,000 portal visitors). Existing users only, not new acquisition. 78.5% are on mobile (6,563), so the journey must work well on a phone.

## Launch Tier
- **M, Targeted**, Reach: 8,360 consumers a month, all inside one existing journey. Impact: about 731 of 3,846 new agreements a month fail within 60 days, and a 3-point improvement keeps about 115 more plans a month. Risk of silence: agents would get questions about limited plan options without knowing why. This is a targeted launch, not a silent release, because every journey starter sees a changed flow and agents need briefing. Not L, because no external campaign is needed.

## Channels
1. **Owned: Instalment journey in the portal: consumers are already there, and screen 1 explains why income is asked.**
2. **Owned: Existing outreach messages (email, SMS, letter) to 100,000 consumers a month: after a SHIP decision, add one line such as "See plans that fit your budget". Outreach stays identical in both test arms.**
3. **Earned: Client (creditor) reporting and reviews: clients track broken plans and complaints with recovery, so sharing the plan-kept rate builds their support. No paid channel: the audience is already in the portal, so ads add nothing.**

## Enablement & Assets
Brief collection agents (assumption: 40 in the pilot team, not in the brief), support, compliance and client managers. Build: (1) one-page agent brief on what changed, how the limit is calculated and what to say when no plan fits; (2) 3-minute demo of the prototype; (3) consumer FAQ on why income is asked and that the result is not financial advice; (4) escalation path for consumers who want a plan above their limit; (5) compliance-approved wording for the income explanation and the 70% rule.

## Ownership, Budget & Timeline
- **Ownership & budget:** Caglar Acar (Product Manager) owns the plan, the A/B test and post-launch metrics. Engineering Lead owns production build and 50/50 randomisation. Collection Operations Manager owns agent training. Compliance Officer approves the wording and the affordability rule. UX Writer owns consumer copy and FAQ. Data Analyst reads results at day 102. Extra cost: engineering time for production and tracking (estimate needed), about 40 hours of agent training (assumption), compliance review. No paid media budget. Gap: the real affordability rule is not defined (70% is a sample).
- **Timeline:** Weeks -4 to 0: build, compliance review, agent briefing. Phase 1 (beta, A/B test): 6 weeks of enrolment at 50/50, then 60 days of follow-up, read at day 102. Phase 2 (launch moment): if the result is SHIP, roll out to 100% of journey starters, with agents briefed the week before. Phase 3 (post-launch): check the three metrics weekly for 8 weeks, then add the line to outreach messages.

## Success Metrics
- **Metrics:** 1. Share of new agreements with no missed payment within 60 days: 81% today, target 84% or more. 2. Share of started journeys that end in an agreement: 46.0% today, must not fall below 43.0%. 3. Agent contact within 7 days: 31.0% today, must stay below 33.0%.
- **Bad signal to watch for:** No-missed-payment rate rises but agreement rate drops sharply (feature only filters people out), or agent contact reaches 33.0%.
- **Likely post-launch decision:** Iterate: the 70% rule is only a sample. Trigger: lift positive but below 3 points, or agent contact at 33.0%.
