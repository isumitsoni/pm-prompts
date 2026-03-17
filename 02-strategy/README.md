# Strategy Prompts

Prompts for sizing opportunities, positioning, and roadmap tradeoffs.

---

## AI Opportunity Sizing Prompt

**Use case:** Estimate which AI opportunities are worth building now.
**Input needed:** Opportunity list, user segment sizes, baseline conversion/retention data, pricing model.

---

Act as a strategic PM partner. For each AI opportunity, estimate:
1. User impact (activation, retention, expansion potential)
2. Business impact (revenue, margin, support cost)
3. Confidence level based on available evidence
4. Time-to-value estimate

Return a ranked list with this format:
- Opportunity
- Strategic fit (1–5)
- User value (1–5)
- Business value (1–5)
- Confidence (High/Medium/Low)
- Recommended action (Now/Later/Drop)

Use conservative assumptions unless data is explicit.

---

**Tips:**
- Add downside-case estimates to avoid overcommitting roadmap capacity.
- Pair with a quick engineering sanity check before locking priorities.

---

## Strategic Bet Memo Generator

**Use case:** Write a one-page memo for a major product bet.
**Input needed:** Market context, alternatives, expected upside, risks, execution plan.

---

Create a strategic bet memo for leadership.

Include:
- Bet statement
- Why this bet matters now
- Alternatives considered
- Expected upside in 6 and 12 months
- Key risks + kill criteria
- Resource ask
- Decision request

Tone: executive-level, clear, high accountability.

---

**Tips:**
- Define kill criteria early to reduce sunk-cost bias.
- Add one paragraph on opportunity cost of not doing this.

---

## Competitive Positioning Analyzer

**Use case:** Identify differentiation vs AI-native and incumbent competitors.
**Input needed:** Competitor list, feature comparisons, pricing, customer feedback.

---

Analyze our competitive position and recommend differentiation strategy.

Deliver:
1. Competitor matrix (capability, UX, trust, pricing)
2. Where we can win (unique strengths)
3. Where we should not compete
4. Messaging angle for each buyer persona
5. 90-day strategic actions

Prioritize realistic differentiation over generic claims.

---

**Tips:**
- Include trust/safety and implementation speed as separate dimensions.
- Re-run quarterly because AI competitor landscapes shift quickly.

---

## North Star Metric Designer

**Use case:** Pick a metric that reflects durable product value, not vanity usage.
**Input needed:** Product model, user value moment, existing KPIs, growth goals.

---

Help me define the right North Star Metric for this product.

Process:
1. Identify the core user value event.
2. Suggest 3 candidate North Star Metrics.
3. Evaluate each against leading/lagging balance, gaming risk, and actionability.
4. Recommend one NSM with 3 input metrics.
5. List anti-metrics (what could improve while product quality worsens).

Use PM-friendly language and concrete metric definitions.

---

**Tips:**
- Tie NSM to user outcome, not raw model usage volume.
- Validate the metric can be instrumented before announcing it org-wide.

---

## Roadmap Tradeoff Facilitator

**Use case:** Resolve roadmap conflicts when resources are constrained.
**Input needed:** Candidate initiatives, team capacity, dependencies, strategic objectives.

---

You are facilitating a roadmap tradeoff decision.

Given the initiatives, produce:
1. A scoring table (impact, confidence, effort, strategic alignment)
2. Dependency and risk notes
3. A recommended roadmap for next 2 quarters
4. What to deprioritize and why
5. A stakeholder narrative for the final tradeoff

Output should be practical for a planning meeting.

---

**Tips:**
- Include explicit "what we are saying no to" lines to reduce ambiguity.
- Use this with engineering estimates, not in isolation.

---

## Lost Deal / No-Decision Analyzer

**Use case:** Find product and messaging gaps by analyzing prospects who said no or never moved.
**Input needed:** Lost deal notes, sales call summaries, objection themes, segment info, pricing context.

---

Act as a PM helping me learn from lost deals and no-decision outcomes.

Analyze the context and return:
1. The top 5 reasons prospects did not move forward
2. Which reasons are product gaps vs trust gaps vs buying-process issues
3. A frequency and severity table
4. The most likely "missing proof" that would have changed the conversation
5. 3 product or GTM experiments to test in the next 30 days
6. A short summary for leadership with:
   - What we should fix now
   - What we should validate first
   - What we should ignore for now

Constraints:
- Use only the evidence in the notes
- Mark low-confidence conclusions clearly
- Do not treat one loud prospect as a market signal without support

---

**Tips:**
- This works especially well after a founder-led sales sprint.
- Separate "not a fit" from "did not trust us yet" before changing roadmap direction.

---

## AI Build vs Buy Decision Memo

**Use case:** Decide whether to build an AI capability in-house, use a vendor, or hybridize.
**Input needed:** Use case, user importance, timeline, data sensitivity, budget, internal capabilities, vendor options.

---

You are my strategic PM advisor. Help me decide whether to build, buy, or take a hybrid approach for this AI capability.

Return the answer in this format:
1. Decision summary
2. Option table with:
   - Build
   - Buy
   - Hybrid
3. Score each option on:
   - Time to launch
   - User experience control
   - Cost predictability
   - Data/privacy risk
   - Differentiation potential
   - Long-term flexibility
4. Recommend one option and explain the tradeoffs
5. List the top 3 assumptions that could change the decision
6. Draft a one-page memo for leadership

Constraints:
- Use conservative assumptions unless explicit numbers are provided
- Call out lock-in risk separately from general vendor risk
- Distinguish "core differentiator" from "commodity plumbing"

---

**Tips:**
- Re-run this when pricing, latency, or compliance constraints change.
- If the recommendation depends on one missing number, flag that number as the next research task.
