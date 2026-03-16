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
