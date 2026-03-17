# Data and Metrics Prompts

Prompts for KPI diagnosis, experiments, metric trees, and AI feature quality.

---

## KPI Diagnostic Prompt

**Use case:** Explain why a KPI moved and what to do next.
**Input needed:** KPI trend data, segment cuts, recent releases, external events.

---

Analyze this KPI movement and provide:
1. Most likely drivers
2. Segment-level differences
3. What is correlation vs likely causation
4. Next 3 analyses to run
5. Recommended action this week

Avoid overclaiming causality without evidence.

---

**Tips:**
- Always compare pre/post release windows with control cohorts if possible.
- Add confidence levels to each driver hypothesis.

---

## Experiment Readout Generator

**Use case:** Summarize A/B test results for decision-making.
**Input needed:** Experiment setup, sample sizes, metrics, outcomes, caveats.

---

Create an experiment readout with:
- Hypothesis
- Setup and guardrails
- Primary and secondary metric impact
- Statistical and practical significance
- Decision recommendation (ship/iterate/stop)
- Follow-up experiment ideas

Keep it clear for non-analyst stakeholders.

---

**Tips:**
- Call out practical significance even if p-values look strong.
- Include risk of novelty effects in early uplift.

---

## Metric Tree Builder

**Use case:** Connect company goals to team-level product metrics.
**Input needed:** Business goals, product goals, current KPI set.

---

Build a metric tree from top-level outcomes down to controllable product inputs.

Return:
1. North Star metric
2. Level-1 outcome metrics
3. Level-2 input metrics
4. Owner for each metric
5. Instrumentation gaps

Format as a hierarchy with definitions.

---

**Tips:**
- Assign single-threaded metric ownership to avoid reporting ambiguity.
- Confirm each input metric has a direct action lever.

---

## Retention Drop Investigator

**Use case:** Diagnose declining retention and propose interventions.
**Input needed:** Cohort retention curves, onboarding funnel, behavior events, feature adoption.

---

Investigate retention decline and provide:
1. Where in lifecycle drop worsened
2. Which user cohorts are most affected
3. Likely root causes
4. Top 3 interventions with expected impact
5. Experiment design for each intervention

Focus on behavior-linked reasons, not generic advice.

---

**Tips:**
- Compare retained vs churned cohorts on early activation behaviors.
- Prioritize one intervention per lifecycle stage to keep tests interpretable.

---

## AI Feature Quality Scorecard

**Use case:** Track quality of an AI feature beyond engagement numbers.
**Input needed:** Output samples, rubric, failure modes, cost/latency data, user feedback.

---

Create a quality scorecard for this AI feature.

Include dimensions:
- Task success
- Factual accuracy
- Consistency
- Safety/compliance
- Latency
- Cost per successful task
- User trust signal

For each dimension provide metric definition, current status, and target threshold.

---

**Tips:**
- Pair output quality with cost and latency to avoid "high quality but unusable" outcomes.
- Refresh rubrics monthly as use-cases evolve.

---

## Eval-to-KPI Bridge

**Use case:** Connect AI eval scores to product metrics so teams do not optimize the model in isolation.
**Input needed:** Current eval rubric, user workflow, product KPIs, failure modes, baseline usage data.

---

Help me connect AI quality metrics to product outcomes.

Given the context, produce:
1. A table with these columns:
   - Eval dimension
   - Why users care
   - Product KPI it influences
   - Leading indicator
   - Guardrail metric
2. The 3 eval dimensions most likely to move business outcomes
3. Which eval dimensions are useful for debugging but not for executive reporting
4. A weekly review template for PM + engineering
5. A warning section called "How we could game this"

Constraints:
- Avoid vanity metrics such as raw model usage unless directly tied to value
- Include at least one trust or quality guardrail
- Use plain PM language, not ML jargon

---

**Tips:**
- Use this when stakeholders ask why offline eval improvements are not yet visible in product KPIs.
- Good AI PM reporting usually needs one quality metric, one behavior metric, and one business metric side by side.

---

## Pilot-to-Scale Readiness Scorecard

**Use case:** Decide whether an AI feature is ready to move from pilot to broader rollout.
**Input needed:** Pilot results, support tickets, quality scores, latency/cost data, user feedback, operational constraints.

---

Act as a product review lead. Assess whether this AI feature is ready to scale beyond a pilot.

Return:
1. A readiness scorecard with these categories:
   - User value proof
   - Quality consistency
   - Trust and safety
   - Operational readiness
   - Unit economics
   - Support burden
2. Score each category red/yellow/green with evidence
3. A go / conditional go / no-go recommendation
4. The top 5 blockers to address before wider launch
5. A founder-facing note that explains the decision in plain language

Constraints:
- Do not recommend scaling if trust or economics are red
- Separate "needs more polish" from "not proven valuable"
- Make the recommendation evidence-based, not optimistic

---

**Tips:**
- Use this after every pilot wave so rollout decisions stay disciplined.
- Pair it with a release gate from your eval process so teams do not argue from anecdotes.

---

## AI Pilot Signal Triage

**Use case:** Make sense of messy pilot feedback when usage, quality, and customer sentiment disagree.
**Input needed:** Pilot metrics, customer notes, support tickets, output reviews, launch goals.

---

Help me triage this AI pilot.

Return:
1. A signal table with:
   - Signal
   - Type (usage / quality / sentiment / economics / support)
   - What it suggests
   - Confidence level
2. A section called "real problem vs noise"
3. The 3 most likely reasons the pilot is underperforming or overperforming
4. The next 3 decisions I should make
5. A recommendation:
   - scale
   - extend pilot
   - narrow scope
   - stop

Constraints:
- Do not confuse curiosity usage with durable product value
- Call out when positive usage is hiding weak quality
- If evidence is mixed, explain what additional data would reduce uncertainty

---

**Tips:**
- This works best after the first 1-2 weeks of a pilot, not on day one.
- Make sure at least one of the next decisions is about who to talk to, not only what to build.
