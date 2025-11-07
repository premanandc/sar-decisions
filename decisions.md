---
marp: true
theme: default
paginate: true
class: invert
---

# The Good, the bad and the ugly  

## Facilitating High-Impact Decisions

### SAR - Nov 2025

![bg right:40%](images/compass.png)

<!--
NOTES:
Set the tone: This session is about architecting *decisions*, not just systems.
Say: "As we move from implementing solutions to shaping them, the way we structure and facilitate decisions becomes the core of our role."
-->

---

![bg left:40%](images/bridge.png)

## The Architect’s Core Responsibility

**Not** to make all the decisions.  
**But** to enable decisions that:

- Align with business outcomes  
- Are technically sustainable  
- Are understood and owned by teams  

<!--
NOTES:
Emphasize identity shift. Architects are not bottlenecks. They create conditions for distributed decision-making.
-->

---

![bg right:40%](images/lighthouse.png)

## Why Big Decisions Fail

- Rationale was *implicit*
- Stakeholders lacked shared understanding
- Trade-offs weren't surfaced
- Alignment was forced, not built

**Architects create clarity — not just diagrams.**

<!--
NOTES:
Ask: "Have you seen a 'technically correct' decision fail because alignment was missing?"
Pause. Let recognition surface.
-->

---

![bg left:40%](images/balance-scale.png)

## Three Dimensions of Effective Architecture Decisions

| Dimension | Guiding Question | Architect Role |
|---|---|---|
| Technical | Is it viable and maintainable? | Surface constraints & trade-offs |
| Organizational | Who owns and operates it? | Clarify accountability & boundaries |
| Strategic | How will it evolve? | Consider long-term path & risks |

<!--
NOTES:
Highlight balancing these dimensions as the architectural craft.
-->

---

![bg right:40%](images/discussion-circle.png)

## Architect as Decision Facilitator

Strong architects:

- Create shared understanding **before** debating solutions
- Make trade-offs **explicit**
- Guide groups toward **good-enough** forward decisions
- Capture rationale (lightweight ADRs)

<!--
NOTES:
This is the identity shift: from *answer-giver* to *clarity enabler*.
-->

---

![bg left:40%](images/decision-tree.png)

## Decision Framing Template

1. **Decision** being made  
2. **Options** considered  
3. **Trade-offs** that matter  
4. **Recommendation & why**  
5. **Risks & assumptions** to monitor

We'll use this in the scenarios.

<!--
NOTES:
Encourage participants to *write this down* during breakouts.
-->

---

![bg right:40%](images/flow-channels.png)

## Scenario 1

### From Nightly Batch to Near Real-Time Analytics

**Context:**  
Retail analytics dashboards run nightly. Business wants **<5 min** freshness.

**Current Reality:**  

- Snowflake warehouse  
- Airflow + Python ETL  
- Some stores send **daily CSV uploads**  
- Data engineering team of **4**

<!--
NOTES:
Do not let participants jump to streaming tech.
Ask: "What decision depends on real-time visibility?"
-->

---

### Scenario 1 — Key Decision

**How should the data ingestion architecture evolve?**

Options:

- Micro-batch (1–10 min)
- Introduce streaming pipelines
- Hybrid / phased approach

**Focus:**  
Is real-time worth the cost *now*?

<!--
NOTES:
Look for: clarity on value, minimal-change-first thinking.
-->

---

### Breakout (10 minutes)

Use the decision framing template.

![bg left:40%](images/breakout.png)

<!--
NOTES:
During walkaround, ask: "What is the *smallest* meaningful improvement?"
-->

---

![bg right:40%](images/map-boundaries.png)

## Scenario 2  

### Clarifying Service & Data Boundaries (Fintech)

**Context:**  
Two teams share the **Customer Profile** table.

<style>
table {
  font-size: 0.7em;
}
</style>

| Team | Owns | Writes | Problem |
|---|---|---|---|
| Onboarding | Identity/KYC | Yes | Needs correctness/privacy guarantees |
| Accounts | Account lifecycle | Yes | Needs stable references & updates |

**Regulator requires clear **data stewardship**.

<!--
NOTES:
Key teaching here: Data ownership drives boundaries — not code modules.
-->

---

### Scenario 2 — Key Decision

**Where should the source of truth live, and how do others consume it?**

Likely Patterns:

- One authoritative Profile service
- Other services consume via APIs/events
- Local read models where needed

<!--
NOTES:
Push groups to articulate *transition*, not just end-state.
-->

---

### Breakout 2 (10 minutes)

Use the decision framing template.

![bg left:40%](images/breakout.png)

<!--
NOTES:
Prompt stuck groups: "Who suffers the most if data is wrong?"
-->

---

![bg right:40%](images/building-scaffold.png)

## Scenario 3

### Rewrite vs Incremental Evolution

**Context:**  
SaaS platform performance & maintainability issues → leadership suggests rewrite.

**Realities:**  

- Current system = **90% revenue**
- Competitor advancing
- Mixed engineering skill levels
- Unknown behavior embedded in production

<!--
NOTES:
Core insight: rewrites discard domain knowledge, not just code.
-->

---

### Scenario 3 — Key Decision

Options:

1. Full rewrite  
2. Gradual refactor (Strangler pattern)  
3. Parallel V2 with staged migration  

Evaluation Criteria:

- Risk tolerance
- Migration complexity
- Business continuity risk

<!--
NOTES:
Ask: "Which option fails most gracefully if we are wrong?"
-->

---

### Breakout 3 (10 minutes)

Use the decision framing template.

![bg left:40%](images/breakout.png)

<!--
NOTES:
Listen for migration strategy maturity, not solution shape.
-->

---

## Key Takeaways

| Architects Don’t | Architects Do |
|---|---|
| Chase perfect designs | Enable forward movement with clarity |
| Decide alone | Facilitate shared reasoning |
| Focus only on tech | Consider org + strategy too |
| Hide uncertainty | Make risks & assumptions explicit |

![bg right:40%](images/compass.png)

<!--
NOTES:
Land this patiently. This is the identity shift you want to seed.
-->

---

## Final Thought

Great architects are **not defined by the answers they give**,  
but by the **clarity and alignment they enable when stakes are high.**

<!--
NOTES:
Pause. Let the idea land. Then thank the group.
-->