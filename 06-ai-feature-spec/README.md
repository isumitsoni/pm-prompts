# AI Feature Spec Prompts

The highest-signal category. Prompts for speccing, evaluating, and shipping AI features with production discipline.

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
