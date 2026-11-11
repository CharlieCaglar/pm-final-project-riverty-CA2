# PRD & Prototype Sprint (Module 4)

## Pick & scope with MoSCoW
- **The “Now” feature I’m scoping (name + one-line core description):** B3 - Affordability check before the plan options: Help consumers understand what they can realistically afford before choosing an instalment plan, so they are more likely to choose a plan they can actually keep.
- **My finalized Must-Haves (after overriding the AI):** 1. Simple affordability form with monthly income and essential costs.
 2. Calculate an affordable monthly payment limit.
 3. Show only plan options within that affordable limit.
 4. Let the consumer edit the information and recalculate.
 5. If no plan fits, clearly offer agent support.
 6. Give a short explanation of why income information is needed.
- **What I demoted from Must → Should/Won’t, and why:** I moved detailed tracking and storing the affordability result out of Must-Have. They are useful for measuring performance, but the consumer can still complete the core journey without them. I want V1 focused on helping the consumer find a plan they can actually keep.

## Generate your Simplified PRD
- **One thing my PRD makes explicit that a vague brief would have missed:** The PRD makes it clear that we should only show plans within the consumer’s affordable limit, and if no plan fits, we should offer agent support instead of showing an unaffordable option.

## Prompt-to-prototype sprint
- **Where did the prototype reveal a gap in my PRD logic? (what I had to update):** The PRD said to calculate an affordable monthly payment limit, but it did not define how the limit should be calculated. Claude had to assume a 70% rule. I need to define this as a configurable or sample rule instead of letting the prototype invent it.
- **My prototype: save Claude's HTML as prototype.html in 04-roadmap/, open it in your browser, and add a screenshot:** https://github.com/CharlieCaglar/pm-final-project-riverty-CA2/blob/main/04-roadmap/prototype.html

https://github.com/CharlieCaglar/pm-final-project-riverty-CA2/blob/main/04-roadmap/Sk%C3%A4rmbild%202026-11-11%20105626.png
