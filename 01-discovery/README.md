# Discovery Prompts

Prompts for turning raw research into clear, decision-ready insight.

---

## JTBD Interview Synthesizer

**Use case:** After 5–15 user interviews, turn raw notes into clear jobs-to-be-done patterns.
**Input needed:** Interview notes, user segments, product context, market type (B2B/B2C).

---

You are my PM research analyst. I will paste interview notes from multiple users.

Your task:
1. Extract top jobs users are trying to get done.
2. Cluster pain points by frequency and severity.
3. Separate functional, emotional, and social jobs.
4. Identify current workaround solutions users use.
5. Return output in this format:
   - Top 5 JTBD statements
   - Pain point heatmap (High/Medium/Low)
   - Opportunity areas (quick wins vs strategic bets)
   - 3 follow-up questions I should ask in the next interview round

Constraints:
- Do not invent user quotes.
- If evidence is weak, mark it as "low confidence".

---

**Tips:**
- Include exact user quotes where available to strengthen stakeholder buy-in.
- Run this once per segment (SMB vs Enterprise) before combining patterns.

---

## Problem Statement Builder

**Use case:** Convert noisy discovery insights into one sharp product problem statement.
**Input needed:** Research summary, target user, business objective, constraints.

---

Act as a senior PM coach. Based on the context I provide, write:
1. A one-paragraph problem statement.
2. A one-line "why now" justification.
3. A "do not solve" list (scope boundaries).
4. A success definition in measurable terms.

Use this structure:
- User:
- Problem:
- Current workaround:
- Business impact:
- Why now:
- Success criteria:
- Out-of-scope:

Make it concrete and non-generic.

---

**Tips:**
- Share this output before roadmap discussions to prevent feature-solution bias.
- Force a measurable success definition before ideation starts.

---

## ICP Clarifier for New AI Feature

**Use case:** Narrow a broad target market into a realistic first release segment.
**Input needed:** Current user base info, revenue mix, adoption data, proposed feature idea.

---

You are helping me pick the first ICP for an AI feature.

Given my context, do the following:
1. Propose 3 candidate ICPs.
2. Score each on pain intensity, willingness to pay, and implementation feasibility (1–5).
3. Recommend one primary ICP and explain tradeoffs.
4. Draft a short hypothesis statement: "If we build X for Y, we expect Z behavior change."

Keep recommendations pragmatic for a 6–8 week build cycle.

---

**Tips:**
- Add one "anti-ICP" to avoid distracted GTM execution.
- Re-run after first pilot data to confirm or pivot segment.

---

## User Journey Friction Mapper

**Use case:** Identify where users drop off and where AI can reduce friction.
**Input needed:** Journey stages, user actions, known drop-offs, support tickets, analytics snapshots.

---

Map the end-to-end user journey and identify friction points.

Output in table format:
- Journey stage
- User goal
- Current friction
- Evidence source (ticket/interview/analytics)
- Friction severity (1–5)
- AI-assisted opportunity
- Risk if we automate

Then rank top 5 opportunities by impact vs effort.

---

**Tips:**
- Include evidence source so teams trust the prioritization.
- Separate friction caused by UX vs friction caused by missing capability.

---

## Discovery-to-Decision Brief

**Use case:** Create a decision-ready brief before planning and engineering sizing.
**Input needed:** Discovery findings, constraints, strategic goals, known risks.

---

Convert this discovery data into a decision brief for product + engineering leadership.

Sections required:
1. What we learned (facts only)
2. What we believe (assumptions)
3. What we still do not know
4. Decision options (A/B/C)
5. Recommendation with rationale
6. Risks and mitigation
7. What we need to validate next sprint

Keep it under 700 words. Crisp, decision-oriented, no fluff.

---

**Tips:**
- Use this as the pre-read for roadmap review meetings.
- Tag assumptions clearly to avoid treating guesses as evidence.
