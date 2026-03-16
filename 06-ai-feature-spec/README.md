# AI Feature Specs Prompts

The highest-signal category. Prompts for speccing, evaluating, pricing, and shipping AI features with production discipline.

---

## AI Feature Spec Builder

**Use case:** Draft a complete spec for a new AI capability.
**Input needed:** User problem, context window/data sources, UX flow, constraints, business goals.

---

You are a senior AI PM + staff engineer hybrid. Draft an AI feature spec with:
1. User problem and target segment
2. Inputs and outputs (structured examples)
3. System behavior (happy path + edge cases)
4. Prompt/system instruction design principles
5. Model strategy (primary, fallback, escalation)
6. Context and retrieval strategy
7. Safety and policy controls
8. Evaluation plan (offline + online)
9. Observability and logging requirements
10. Rollout and guardrail plan
11. Cost and latency budget
12. Open questions

Output should be implementation-ready for product + engineering kickoff.

---

**Tips:**
- Include explicit fallback behavior when model confidence is low.
- Define quality thresholds before coding starts.

---

## Prompt Contract Specifier

**Use case:** Define a stable prompt contract so teams can iterate safely.
**Input needed:** Use case, required output format, failure risks, policy constraints.

---

Create a prompt contract for this AI feature.

Required sections:
- Objective
- Required context inputs
- Output schema (strict)
- Constraints and forbidden behaviors
- Few-shot examples
- Failure handling rules
- Versioning and rollback rules

Return both human-readable rules and JSON-style output schema.

---

**Tips:**
- Treat prompt changes like API changes with version control.
- Add schema validation in production to catch silent regressions.

---

## Failure Mode & Recovery Designer

**Use case:** Anticipate and handle AI failure paths before launch.
**Input needed:** Intended behavior, known model weaknesses, user impact sensitivity.

---

Generate a failure-mode design for this AI feature.

Deliver:
1. Top 10 failure modes
2. User impact severity per mode
3. Detection signal per mode
4. Recovery behavior per mode
5. Escalation path to human/manual fallback

Include specific UX copy suggestions for failure states.

---

**Tips:**
- Prioritize silent-failure detection over obvious failure handling.
- Define a hard stop for high-risk outputs.

---

## Eval Suite Planner for AI Feature

**Use case:** Design a practical eval plan aligned to product outcomes.
**Input needed:** Feature objective, output examples, user segments, risk tolerance.

---

Design an eval suite for this AI feature.

Include:
- Evaluation rubric (scored dimensions)
- Golden dataset plan
- Adversarial test cases
- Human review workflow
- Pass/fail thresholds by release stage (alpha, beta, GA)
- Regression monitoring plan

Keep this grounded for a PM-led team with limited ML bandwidth.

---

**Tips:**
- Start with a small but representative golden set and expand continuously.
- Track failure categories, not just aggregate quality scores.

---

## AI Cost-Latency-Quality Tradeoff Prompt

**Use case:** Decide model and architecture tradeoffs for production.
**Input needed:** Traffic estimates, SLA targets, budget constraints, quality bar.

---

Analyze tradeoffs for this AI feature across cost, latency, and quality.

Output:
1. 3 architecture options (premium, balanced, cost-efficient)
2. Expected quality/cost/latency profile for each
3. Risks and mitigations
4. Recommendation by product tier (free/pro/enterprise)
5. Trigger conditions for switching strategy at runtime

Use practical assumptions and show where uncertainty is high.

---

**Tips:**
- Separate first-token latency from full completion latency for UX decisions.
- Consider tiered model routing based on task complexity.

---

## Go/No-Go Release Gate for AI Feature

**Use case:** Run a final release decision when evals, safety, reliability, and business goals conflict.
**Input needed:** Eval results, incident history, SLA status, cost metrics, stakeholder constraints.

---

You are an AI PM release board advisor. Evaluate whether this AI feature should move from [alpha/beta] to [beta/GA].

Use this decision framework:
1. Quality gate: check rubric scores and regression results.
2. Safety gate: check policy violations and unresolved high-severity risks.
3. Reliability gate: check latency, error rates, and rollback readiness.
4. Business gate: check expected impact vs operating cost.
5. Support gate: check support readiness and escalation coverage.

Output format:
- Gate scorecard (Pass / Conditional / Fail for each gate)
- Overall decision (Go / Conditional Go / No-Go)
- Required conditions before re-review
- Stakeholder message draft (short)

Rules:
- If any critical safety gate fails, default to No-Go.
- Mark missing evidence explicitly.

---

**Tips:**
- Use this in every stage transition meeting to avoid subjective launch calls.
- Archive each scorecard so future incidents can be traced to decisions.

---

## AI Feature Pricing & Packaging Simulator

**Use case:** Decide pricing and plan packaging for AI features with variable model costs.
**Input needed:** Cost per request, usage patterns, value metric, current pricing tiers, margin targets.

---

Act as a PM + pricing strategist. Build 3 pricing/packaging options for this AI feature.

For each option include:
1. Packaging model (included quota / add-on / usage-based / hybrid).
2. Unit economics estimate (best/base/worst case).
3. User behavior risks (overuse, underuse, churn triggers).
4. Recommended guardrails (rate limits, fair-use caps, tier routing).
5. GTM messaging angle.

Then recommend one option with rationale and a 30-day validation test plan.

Constraints:
- Prioritize margin durability and perceived fairness.
- Avoid pricing complexity users cannot understand.

---

**Tips:**
- Test packaging with 2–3 customer segments before broad launch.
- Pair with telemetry alerts so margin issues are caught in week one.

---

## AI Incident Triage & User Comms Commander

**Use case:** Handle live AI feature incidents — quality drop, hallucinations, latency spikes — with clear execution and communication.
**Input needed:** Incident symptoms, scope, impacted users, known root-cause hypotheses, current mitigations.

---

You are my incident commander for an AI product incident.

Generate:
1. 60-minute action plan (containment first).
2. Triage checklist by function (Product, Engineering, Support, Comms).
3. User-impact severity classification.
4. Internal status update template (exec + cross-functional).
5. External user update template (transparent but safe).
6. Recovery criteria and post-incident follow-up actions.

Rules:
- Prioritize user harm reduction over feature availability.
- If cause is unknown, communicate uncertainty clearly with next update time.

---

**Tips:**
- Pre-fill this prompt in your runbook so it can be used under pressure.
- Always include the next update timestamp in public incident messages.
