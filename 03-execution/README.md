# Execution Prompts

Prompts for PRDs, sprint planning, launch readiness, and postmortems.

---

## PRD Draft from Discovery Pack

**Use case:** Turn validated discovery into a first PRD draft quickly.
**Input needed:** Problem statement, user stories, constraints, assumptions, success metrics.

---

Draft a PRD using this structure:
1. Problem and context
2. Target users
3. Goals and non-goals
4. User stories and acceptance criteria
5. Functional requirements
6. UX requirements
7. Data/telemetry requirements
8. Risks and mitigations
9. Rollout plan
10. Success metrics

Rules:
- Write only what is supported by provided context.
- Mark unclear areas as "open question".

---

**Tips:**
- Keep this as v0 PRD and co-edit with engineering, design, and data.
- Convert open questions into explicit owners and due dates.

---

## Sprint Scope Cutter

**Use case:** Reduce oversized sprint plans into realistic commits.
**Input needed:** Backlog items, estimates, team capacity, launch dates.

---

Review my sprint scope and make it executable.

Output:
- Must-have items (commit)
- Should-have items (stretch)
- Won't-do-now items
- Major risks
- Suggested sequencing
- Definition of done per must-have item

Optimize for shipping on time with acceptable quality.

---

**Tips:**
- Ask for 20% contingency when external dependencies are high.
- Keep stretch goals visible but detached from launch commitments.

---

## Dependency Risk Radar

**Use case:** Surface cross-team risks before they block delivery.
**Input needed:** Initiative timeline, teams involved, dependency map, known bottlenecks.

---

Create a dependency risk radar for this initiative.

Include:
1. Dependency inventory
2. Probability x impact scoring
3. Early warning indicators
4. Mitigation owner and deadline
5. Escalation triggers

Provide output in a concise table, then summarize top 3 critical risks.

---

**Tips:**
- Use weekly and refresh scores after every planning sync.
- Set escalation triggers before risks turn into incidents.

---

## Launch Readiness Checklist Builder

**Use case:** Ensure product, GTM, support, and analytics are launch-ready.
**Input needed:** Launch type, release scope, teams involved, target date.

---

Generate a launch-readiness checklist customized to this release.

Sections:
- Product quality and testing
- Analytics and instrumentation
- GTM and messaging
- Sales enablement
- Support readiness
- Risk monitoring and rollback plan

For each item include owner, due date, and go/no-go criteria.

---

**Tips:**
- Share this 2 weeks before launch to avoid last-minute surprises.
- Include rollback criteria explicitly for AI features.

---

## Postmortem Insight Generator

**Use case:** Run a blameless review after launch misses or incidents.
**Input needed:** Incident timeline, impact, actions taken, logs/feedback.

---

Create a postmortem document from the input.

Required sections:
1. Incident summary
2. Customer impact
3. Timeline of events
4. Root cause(s)
5. What worked well
6. What failed
7. Corrective actions (owner + due date)
8. Prevention plan

Make it blameless, specific, and actionable.

---

**Tips:**
- Keep root causes systemic, not person-centric.
- Track corrective actions in backlog with visible status.
