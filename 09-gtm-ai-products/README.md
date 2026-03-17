# GTM for AI Products

Prompts for launching AI features with rigor: readiness gates, pricing decisions, competitive positioning, PMF signal review, and beta-to-GA transitions.

---

## Launch Readiness Checklist

**Use case:** Determine if an AI feature is actually ready to ship before declaring launch-ready.
**Input needed:** Feature description, target users, model or system being shipped, known failure modes, rollback plan status, support team readiness, eval threshold (if set).

---

You are a launch readiness reviewer for an AI feature.

Context I will provide:
- Feature description and target users
- Model or system being shipped
- Known failure modes identified so far
- Rollback plan status
- Support team readiness
- Eval threshold (if defined)

Produce a launch readiness checklist with the following sections. For each item, include: Owner field, Go/No-Go designation, and current status (complete / in progress / not started).

**Sections:**
1. Eval and quality gates
   - Has the feature hit the defined eval threshold?
   - Is the eval methodology validated against real user scenarios?
   - Are known failure modes documented and understood?
   - Has regression testing been run against the previous baseline?

2. Data and instrumentation
   - Are success metrics instrumented and firing correctly?
   - Is production logging in place for model inputs and outputs?
   - Are guard metrics (latency, error rate, fallback rate) being tracked?
   - Is there a way to segment metrics by user group and region?

3. Rollback plan
   - Is there a defined kill switch or feature flag?
   - Has the rollback procedure been tested?
   - Are rollback criteria written down (specific thresholds, not "if something goes wrong")?
   - Is the rollback owner identified and reachable?

4. Support readiness
   - Does support have documentation for the new feature?
   - Has support been trained on known failure modes and how to triage them?
   - Is there a defined escalation path for AI-specific issues (e.g., hallucinations, unexpected outputs)?

5. Trust and safety checks
   - Have adversarial inputs been tested?
   - Has the feature been reviewed for potential misuse or harm vectors?
   - Are there output guardrails in place?
   - Is there a process to detect and respond to trust-damaging patterns post-launch?

6. GTM and communication readiness
   - Is the internal team aligned on what is launching and when?
   - Is the user-facing messaging accurate about what the feature does and does not do?
   - Are launch communications reviewed for AI-specific accuracy (no overclaiming)?
   - Is the external FAQ or help documentation ready?

End with: overall go / conditional go / no-go call, and the single most important unresolved item.

---

**Tips:**
- Run this 5 or more days before launch, not hours before. It surfaces the gaps that require cross-team coordination.
- Treat AI feature launches differently from regular software launches. Rollback criteria and trust signals need to be defined up front, not after the first incident.
- A conditional go is only useful if the conditions are specific, owned, and time-bound.

---

## Pricing Model Selection

**Use case:** Choose the right monetization model for an AI product or feature.
**Input needed:** AI product or feature description, cost structure (approximate token or inference cost per interaction), target customer type (B2B or B2C), competitive pricing in market, usage pattern (predictable vs spiky), current customer acquisition model.

---

You are a pricing strategist for an AI product.

Context I will provide:
- AI product or feature description
- Cost structure (approximate token/inference cost per interaction or per unit)
- Target customer type (B2B or B2C, segment detail)
- Competitive pricing reference points
- Usage pattern (predictable/subscription-shaped vs spiky/event-driven)
- How customers currently acquire and evaluate the product

Produce:

1. Analysis of four pricing models for this product:
   - Token/usage-based pricing
   - Seat-based pricing
   - Outcome-based pricing
   - Flat subscription
   For each: how it fits this product, the revenue model implication, and the customer experience implication.

2. A recommendation with rationale. Name the single most important factor driving your recommendation.

3. Key assumptions embedded in your recommendation that could invalidate it if wrong.

4. Risks by model type (one to two per model).

5. What to test in early pricing experiments — three specific tests that would give real signal on pricing sensitivity or usage behavior.

---

**Tips:**
- Token costs change fast. Build a pricing model that can absorb a 50-80% cost reduction without requiring a full redesign. If your pricing is entirely cost-plus, a model price drop becomes a margin windfall you cannot pass through cleanly.
- Outcome-based pricing is compelling but only works when the outcome is measurable in near-real-time. If attribution takes months, you cannot close the billing loop.
- Seat-based pricing works when usage is predictable and value is tied to access, not output. It breaks down for AI features with highly variable per-user consumption.

---

## Competitive Positioning

**Use case:** Position an AI feature clearly when every competitor is making similar capability claims.
**Input needed:** Your AI feature and its actual differentiating behavior, 2-3 competitor claims (copy their exact language), your target user's biggest frustration with current solutions, and any evidence of your feature working (retention data, accuracy improvements, user quotes).

---

You are a positioning strategist for an AI product in a crowded market.

Context I will provide:
- My AI feature and what it specifically does (behavior, not marketing language)
- 2-3 competitor claims in their exact wording
- Target user's biggest frustration with current solutions
- Evidence of my feature working (quantitative or qualitative, or neither if unavailable)

Produce:

1. Differentiation analysis:
   - What claims does everyone make? (commoditized claims — do not lead with these)
   - What specific behaviors actually differentiate the feature?
   - What is the gap between the claims and the demonstrated behaviors?

2. A positioning statement in plain language (one to two sentences, no jargon, no superlatives).

3. Three positioning angles to test. For each: the core claim, the proof point needed, and the user it will land with.

4. What NOT to claim — two to three claims that would invite direct commoditization or unfavorable comparison.

5. Message suggestions for sales and GTM teams (3 one-liners for different buyer contexts).

---

**Tips:**
- When everyone claims "AI-powered X," the differentiator is usually specificity. Buyers have gotten better at detecting vague AI claims. "We use AI" is not positioning. "Our model reduces false positives in fraud detection by X% for payment categories with sparse history" is positioning.
- Positioning is not permanent. Re-evaluate it every time a competitor makes a move that narrows your claimed differentiation.
- The best positioning often comes from the user's frustration with the status quo, not from the product team's view of the feature.

---

## PMF Signal Review

**Use case:** Distinguish early product-market fit signal from novelty effect in an AI product.
**Input needed:** Product description, usage data summary (DAU/WAU/MAU, session length, retention D7/D30 if available), qualitative signals (user quotes, support requests, organic shares), time since launch, target user segment.

---

You are a product analyst reviewing early PMF signal for an AI product.

Context I will provide:
- Product description and target user segment
- Usage data summary (whatever is available — DAU/WAU/MAU, retention D7/D30, session length)
- Qualitative signals (user quotes, support ticket themes, organic shares or referrals)
- Time since launch

Produce:

1. Signal vs noise analysis:
   - Which data points indicate potential real PMF?
   - Which data points are likely novelty-driven?
   - What is missing that would be needed to make a confident call?

2. The specific behaviors that would indicate real PMF for this product type versus novelty:
   - Real PMF: [what to look for]
   - Novelty: [what it looks like]

3. Five questions to ask users right now — specific, behavior-anchored questions that would give the clearest signal on whether they are integrating this product into real workflows.

4. A PMF assessment (qualitative — strong signal / mixed signal / too early / no signal) with one-sentence rationale.

5. The single strongest leading indicator to track over the next 30 days and why it is the right proxy for this product.

---

**Tips:**
- AI products have a novelty retention spike that typically fades around Day 14-21. The question is not "do users come back?" It is "do users come back when the novelty is gone?"
- Look for task completion and workflow integration, not session count. A user who spends 3 minutes completing a real task is more signal than a user who spends 20 minutes exploring a new feature.
- Organic referral and word-of-mouth, even at small scale, is one of the highest-signal PMF indicators. It means users found something worth telling someone else about.

---

## Beta to GA Gate

**Use case:** Decide whether to move an AI feature from closed beta to general availability.
**Input needed:** Beta summary (number of users, time in beta, key feedback themes), eval metrics and whether they have been hit, known failure modes and their resolution status, rollback capability, support team readiness, any trust or safety issues surfaced.

---

You are a launch decision reviewer for an AI feature moving from closed beta to general availability.

Context I will provide:
- Beta summary: number of users, time in beta, key feedback themes
- Eval metrics: what was defined, whether thresholds have been hit
- Known failure modes surfaced in beta and their resolution status
- Rollback capability: current state
- Support team readiness
- Any trust or safety issues surfaced in beta

Produce:

1. A go / conditional go / no-go recommendation with a one-paragraph rationale.

2. Criteria met (with evidence) and criteria missed (with gap description).

3. If conditional go: specific conditions that would flip it to go. Each condition must have a named owner and a date.

4. A GA rollout plan:
   - Percentage rollout stages (e.g., 5% / 25% / 100%)
   - Checkpoint metrics at each stage (what to check before expanding)
   - Kill switch criteria (specific thresholds that would trigger a rollback)

5. A post-GA monitoring plan for the first 30 days:
   - Metrics to watch daily for the first 7 days
   - Metrics to review weekly for weeks 2-4
   - Escalation threshold definition

---

**Tips:**
- The right GA gate question is not "is it good enough?" It is "do we have enough signal to know what good looks like?" A beta that did not answer your key unknowns is not a beta that is ready to graduate.
- Conditional go only works if the conditions are specific and time-bound. "Once we fix the hallucination issue" is not a condition. "Hallucination rate below 2% on the test set by March 21, owner: [name]" is a condition.
- Post-GA monitoring should be heavier for AI features than for conventional software. Model behavior can drift, and early signals of trust degradation are hard to recover from.
