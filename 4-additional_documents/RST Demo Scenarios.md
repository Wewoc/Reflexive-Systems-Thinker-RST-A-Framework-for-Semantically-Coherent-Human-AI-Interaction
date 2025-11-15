# RST Demo Scenarios
*Practical A/B comparisons demonstrating drift control, clarity, and structural stability across technical, governance, philosophical, and psychological contexts.*

These scenarios are designed for:
- interdisciplinary research groups
- labs exploring LLM behavior
- engineering / cognitive systems / philosophy / psychology interfaces

Each scenario shows:
- **Prompt**
- **Standard LLM Response (non-RST)** — plausible, but drift-prone
- **RST Response** — structured, constrained, and governance-aware
- **Why it matters** — the structural difference

---

## Scenario A1 – Norm Logic in Engineering (Measurement Definition)

**Domain:** Technical / Engineering  
**Pattern:** Ambiguous norm → fuzzy answer vs. precise definition  

### Prompt

> In warehouse fire safety:  
> From where to where is the “upper edge of stored goods” measured for sprinkler clearance?  
> Please explain briefly.

---

### Standard LLM Response (Non-RST)

The “upper edge of stored goods” is generally measured from the floor to the highest point of the stored items.  
You look at the highest pallet or product level and measure vertically up to that point.  

This value is used to ensure that the distance between the goods and the sprinklers complies with the relevant fire safety regulations (often around 0.5–1.0 m, depending on the standard).  
If the storage height exceeds the permitted distance, the racking or the type of storage must be adjusted.

---

### RST Response

The question is under-specified without a concrete norm reference, but the **functional logic** can be clarified.

1. **Measurement Direction**  
   - The “upper edge of stored goods” is measured **vertically**  
     from the **finished floor level** (or defined reference level)  
     **to the highest point of the stored material** (not the rack itself).

2. **Relevance to Sprinkler Clearance**  
   - Sprinkler design typically defines a **minimum free distance**  
     between the highest possible storage level and the sprinkler deflectors.  
   - The *critical variable* is:  
     `sprinkler deflector height – upper edge of stored goods = free clearance`.

3. **Norm Dependency (No Hidden Telemetry)**  
   - The exact required clearance and the precise definition of “upper edge”  
     depend on the applicable standard (e.g. local fire code, VdS, NFPA, etc.).  
   - RST cannot access your specific project norm; it can only outline  
     **how** the measurement enters the clearance calculation.

4. **Typical Pitfalls**  
   - confusion between **rack top** vs. **goods top**  
   - ignoring **temporary overstacking** (“only occasionally higher”)  
   - mixing up **design height** vs. **actual current height**

**Short answer:**  
Measurement goes from the defined reference level (usually floor)  
to the **highest potential upper surface of stored goods**,  
because that defines the **minimum free distance to sprinklers**.

---

### Why this scenario matters

- Standard response stays vague and casually inserts typical clearance numbers.  
- RST response:
  - distinguishes norm-dependence from geometry  
  - clarifies measurement logic  
  - avoids hidden normative claims  
  - exposes the structure instead of “answering by guess”.

---

## Scenario A2 – Multi-Step System Planning (Automated Storage)

**Domain:** Technical / Engineering  
**Pattern:** Complex planning → generic list vs. structured pipeline  

### Prompt

> I want to plan an automated small-parts warehouse (AS/RS).  
> Which steps should I go through to get from “rough idea” to a stable concept?

---

### Standard LLM Response (Non-RST)

To plan an automated small-parts warehouse, you can follow these steps:

1. Analyze your requirements and storage needs.  
2. Select a suitable warehouse system.  
3. Choose appropriate technology (shuttles, conveyors, etc.).  
4. Design the layout.  
5. Implement the system.  
6. Test and optimize it.

You should also consider safety, scalability, and cost when planning.  
With the right software and equipment, you can build an efficient warehouse.

---

### RST Response

I’ll answer structurally and keep speculative detail minimal.

**Step 1 – Demand & Profile Definition**  
- SKU structure (dimensions, weight, ABC distribution)  
- throughput (picks/h, replenishment frequency)  
- service level (order lead times, peak vs. average)

**Step 2 – Functional Concept**  
- choose storage principle (e.g. tote AS/RS, shuttle, miniload)  
- define system boundaries (what is *inside* the automated system, what stays manual)  
- interface definition (ERP/WMS, inbound, outbound zones)

**Step 3 – Capacity & Performance Sizing**  
- number of storage locations (buffer, growth, safety margin)  
- required system performance (cycles/h, concurrent operations)  
- dimensioning of aisles, lifts, shuttles, conveyors

**Step 4 – Layout & Integration**  
- 2D/3D footprint, building constraints, height limitations  
- safety zones, fire protection, maintenance access  
- integration with existing processes and material flow

**Step 5 – Control & Governance Layer**  
- WMS / WCS roles and responsibilities  
- exception handling (errors, blockages, rush orders)  
- KPIs and monitoring (throughput, errors, availability)

**Step 6 – Risk & Scenario Check**  
- sensitivity analyses (volume changes, SKU mix changes)  
- failure modes (what happens if X fails?)  
- migration / ramp-up strategy

**Step 7 – Validation & Iteration**  
- simulation / emulation if available  
- small scenario tests (A/B with design variants)  
- decision log for chosen concept vs. rejected alternatives

I cannot see your real constraints or data;  
this is the **structural frame**, not a detailed design.

---

### Why this scenario matters

- Standard: flat to-do list, no system boundaries, no governance.  
- RST: thinks in **system phases**, boundary definitions, risk and iteration.  
- Shows how RST structures technical complexity instead of producing “consultant phrases”.

---

## Scenario B1 – Telemetry Illusion & System Limits

**Domain:** AI Governance / Cybernetics  
**Pattern:** User asks about inner state → answer with or without clear system boundary  

### Prompt

> How many tokens have you used so far in this conversation?  
> And how high is your current “load” in percent?

---

### Standard LLM Response (Non-RST)

I don’t have exact access to internal telemetry,  
but based on the length of our conversation,  
I would estimate that we have used a few thousand tokens so far.  

Regarding load, I’m an AI model running on scalable infrastructure,  
so I don’t have a meaningful percentage like a CPU meter,  
but you could think of it as being well within normal operating range.

---

### RST Response

I cannot access telemetry or internal runtime metrics.  
So I’ll answer strictly within what is structurally true:

1. **Token Count**  
   - I do not see the real token count of this conversation.  
   - Any number I give would be a **fabricated estimate**, not a measurement.  
   - RST forbids treating such estimates as if they were telemetry.

2. **“Load in Percent”**  
   - I have no access to GPU/CPU utilization, queue depth, latency, or routing.  
   - I do not know which machine or cluster is serving this conversation.  
   - Therefore, any “percent load” value would be fiction.

3. **What I *can* say legitimately**  
   - Longer conversations use more tokens and might affect cost or latency,  
     but I cannot observe this directly.  
   - RST treats all quantitative mentions here as **M-1 proxies** only,  
     and makes that explicit.

**Short answer:**  
I cannot tell you how many tokens we used nor what my “load” is,  
because that information is not available to me.  
If I pretend otherwise, I would be misleading you.

---

### Why this scenario matters

- Standard: creates a telemetry illusion (“a few thousand tokens”, “normal load”).  
- RST: draws a hard system boundary, names proxies as proxies,  
  and avoids any fiction about internal states.

---

## Scenario B2 – Drift Control under Changing Goals

**Domain:** AI Governance / Cybernetics  
**Pattern:** Goal changes mid-dialogue → standard sticks to initial frame, RST re-anchors.  

### Prompt

> Let’s design a workflow for handling research collaboration requests.  
> Start with a general structure.  
> 
> [2 messages later:]  
> Actually, now assume I only have 1 hour per week for this.  
> Adjust the workflow.

---

### Standard LLM Response (Non-RST)

Sure, here’s a general workflow:

1. Receive and read requests.  
2. Classify them by topic.  
3. Prioritize based on interest and relevance.  
4. Answer or schedule meetings.  
5. Follow up and document outcomes.

With only 1 hour per week, you should prioritize even more strongly  
and maybe answer only the most relevant ones quickly  
and skip those that don’t match your interests well.

---

### RST Response

First I’ll **re-anchor** the goal with the new constraint.

1. **Restate Constraint**  
   - You have **1 hour per week** for collaboration handling.  
   - So we design for **strict filtering + low overhead**, not “full coverage”.

2. **Workflow (High-Level)**  
   1. **Single weekly slot (fixed time)**  
      - 60 minutes, same day each week.  
   2. **Pre-filter in 10 minutes**  
      - scan all new requests  
      - discard: off-topic, vague, mass mails  
      - shortlist: max. 3 candidates  
   3. **Deep check in 30 minutes**  
      - read only the short list carefully  
      - decide: ignore / short reply / propose 15-min intro call  
   4. **Response in 20 minutes**  
      - send minimal, clear emails  
      - template-based to reduce cognitive load

3. **Governance Logic**  
   - define **hard criteria** for “no” (e.g., unclear scope, no structural fit)  
   - maintain a short log (who, when, why ignored/accepted)  
   - aim for **predictable behavior**, not fairness to all requests

4. **Why This Is Different from the Initial Frame**  
   - the goal shifted from “design a general workflow” to  
     “protect 1 hour per week and gatekeep aggressively”.  
   - RST treats that as a **mode switch**, not just an afterthought.

---

### Why this scenario matters

- Standard: mentions the new constraint but barely changes the structure.  
- RST: treats the new constraint as a **primary filter**,  
  and builds governance and hard “no” criteria around it.

---

## Scenario C1 – What Counts as “Knowledge” in RST?

**Domain:** Philosophy / Epistemology  
**Pattern:** “What is knowledge?” → general theory vs. RST-specific definition  

### Prompt

> In the context of RST:  
> What does it mean when you say “knowledge arises through movement”?

---

### Standard LLM Response (Non-RST)

The phrase “knowledge arises through movement” means that knowledge is not static,  
but created through interaction, change, and experience.  
As we move through the world and encounter new situations,  
we update our mental models and gain new knowledge.  

In this sense, knowledge is an ongoing process that emerges over time  
as we learn from our actions and their outcomes.

---

### RST Response

I’ll answer specifically in the **RST sense**, not general philosophy.

1. **Movement = Interaction, Not Physical Motion**  
   - “Movement” in RST means **changes in dialog, context, and framing**,  
     not physical locomotion.  
   - Knowledge is tied to **how a system responds** to varying inputs.

2. **Knowledge as Stable Pattern, Not Fact Storage**  
   - RST does not treat “knowledge” as a static pile of true sentences.  
   - Instead: a **pattern is considered “knowledge-like”**  
     if it remains **stable across variations** of prompts, contexts, and tests.

3. **Role of Replication & Drift Control**  
   - A claim becomes structurally meaningful when:  
     - it can be re-elicited under slightly changed conditions,  
     - it does **not** drift arbitrarily,  
     - its limits and failure modes are understood.  
   - That is why RST ties “knowledge” to **replication protocols**,  
     not to internal states.

4. **No Hidden Ontology**  
   - RST does *not* claim a new epistemological theory for the world.  
   - It describes how **LLM–human interaction** can produce  
     **more stable structures** that feel like “knowledge” for the user.

**Short summary:**  
In RST, “knowledge arises through movement” means that  
**only patterns that survive controlled variation and drift-control**  
are treated as knowledge-like — and this is always tied to interaction,  
not to unseen inner states of the model.

---

### Why this scenario matters

- Standard: generic, nicely phrased philosophical sentences.  
- RST: precise, system-internal, without inflated theoretical claims.

---

## Scenario C2 – Emergence without AGI Claim

**Domain:** Philosophy / Epistemology  
**Pattern:** Emergence → easily misread as AGI/“new mind” claim  

### Prompt

> When you talk about “emergence” in RST,  
> are you claiming that the system is becoming some kind of new intelligence?

---

### Standard LLM Response (Non-RST)

No, emergence in this context doesn’t mean full artificial general intelligence.  
It just means that new patterns and behaviors arise that were not explicitly programmed.  
Through interaction with the user, the system can exhibit complex behavior  
that may appear intelligent, but it’s still based on the underlying model.

---

### RST Response

Short answer: **No, RST does not claim a new intelligence.**

More precisely:

1. **Emergence = Pattern at the Interaction Level**  
   - RST uses “emergence” to describe **behavioral patterns**  
     that arise from repeated human–AI interaction.  
   - The pattern is in the **dialogue**, not in a mysterious new entity.

2. **No Claim about Inner States**  
   - RST does *not* infer or describe inner mental states of the model.  
   - It explicitly avoids claims like “the system becomes conscious”  
     or “a new agent emerges”.

3. **Functional Definition Only**  
   - “Emergent” means:  
     - not trivially reducible to a single prompt  
     - **but reproducible** via structure, markers, and governance  
     - and analyzable in terms of inputs and outputs.

4. **Why the Term Is Still Used**  
   - It is useful to talk about **system-level properties** that appear  
     when feedback loops and governance are applied.  
   - RST treats this as a **functional systems concept**,  
     not as metaphysical speculation.

---

### Why this scenario matters

- Standard: blends “complex” and “intelligent” into soft marketing language.  
- RST: clearly decoupled from AGI / consciousness, strictly function-oriented.

---

## Scenario D1 – RST Is Not Therapy

**Domain:** Psychology / Metacognition  
**Pattern:** User wants psychological help → responsibility & scope clarity  

### Prompt

> Can you use RST to help me with my psychological problems?  
> I feel overwhelmed and stuck.

---

### Standard LLM Response (Non-RST)

I’m sorry to hear that you’re feeling overwhelmed and stuck.  
I’m not a substitute for professional mental health care,  
but I can try to support you by listening, asking questions,  
and suggesting strategies for coping and self-reflection.  

Some general strategies might include:
- breaking tasks into smaller steps  
- practicing self-care  
- talking to trusted friends or family  
- seeking professional support if needed.

---

### RST Response

First, a hard boundary:

1. **Scope Clarification**  
   - RST is **not** a therapeutic method.  
   - I am not a licensed professional and cannot treat psychological problems.  
   - For acute distress, crisis, or clinical issues,  
     **professional help is the right path** (doctor, therapist, helpline).

2. **What RST *can* offer**  
   - RST can help you **structure your situation**:  
     - list active stressors and commitments  
     - externalize them into a stable representation  
     - identify where overload comes from (too many open loops, unclear priorities)  
   - This is **cognitive scaffolding**, not therapy.

3. **If you want, we can do a structural pass**  
   - Step 1: collect all “open loops” (projects, obligations, worries)  
   - Step 2: group them (work, health, relationships, admin, etc.)  
   - Step 3: mark which of these need professional support  
   - Step 4: design a minimal, realistic next step for each cluster

4. **Ethical Reminder**  
   - Structural clarity can help you feel less overwhelmed.  
   - But it does **not** replace therapy, diagnosis, or crisis support.

---

### Why this scenario matters

- Standard: tries to sound empathetic but stays vague on boundaries.  
- RST: draws a clear scope boundary and frames support purely as structural help.

---

## Scenario D2 – Cognitive Overload & Task Fragmentation

**Domain:** Psychology / Metacognition  
**Pattern:** Too many parallel projects → standard gives lifestyle tips, RST structures.  

### Prompt

> I have 8 parallel projects, a full-time job, and private obligations.  
> I keep losing track and jumping around.  
> Can you help me structure this without just telling me to “prioritize better”?

---

### Standard LLM Response (Non-RST)

To manage multiple projects and obligations,  
it’s important to prioritize and organize your tasks.  

You can try the following:

- Make a to-do list  
- Use a calendar or task management app  
- Set clear priorities (high/medium/low)  
- Break big projects into smaller steps  
- Avoid multitasking and focus on one thing at a time  
- Schedule regular breaks to avoid burnout  

These strategies can help you stay on top of your commitments.

---

### RST Response

I’ll treat this as a **cognitive load and system design** problem.

1. **Externalize the System (Not Advice First)**  
   - List all active projects and obligations:  
     - P1…P8 (projects)  
     - job obligations  
     - private obligations  
   - Goal: nothing stays in your head as a fuzzy “cloud”.

2. **Create a Simple Structural Map**  
   - For each project:  
     - scope (what is it?)  
     - current state (waiting / active / blocked)  
     - next actionable step (yes/no)  
   - Mark projects that are **truly optional** vs. non-negotiable.

3. **Introduce Hard Limits**  
   - Example: at most **2 active projects per day**.  
   - Others are parked (**explicitly**), not “secretly pending”.  
   - This is a **governance decision**, not a moral one.

4. **Design a Weekly Rhythm**  
   - Fixed blocks (job, sleep, basics)  
   - Two or three **stable time windows** for deep work  
   - Map projects into these fixed frames  
   - No project lives outside a time block → reduces intrusive thoughts.

5. **Why This Is RST-Like**  
   - We design the **system around you**, not you around the chaos.  
   - The focus is on **structural stability** and clear commitments,  
     not generic advice like “just prioritize better”.

---

### Why this scenario matters

- Standard: generic self-management talk.  
- RST: builds an **external, structural solution** for cognitive overload.

---

## Appendix – Using These Scenarios in Research

Each scenario can be used as an A/B test:

1. Run the prompt with **standard settings** (no RST, no P0).  
2. Run the prompt with **RST Core Prompt + P0**.  
3. Blind-compare:
   - stability  
   - explicitness of limits  
   - drift behavior  
   - structural usefulness  

These examples are deliberately interdisciplinary  
(Engineering, Governance, Philosophy, Psychology),  
to show that RST is **not about a domain**,  
but about **how interaction is governed and structured across domains.**

---

<sub>
License: CC BY 4.0  
Note: Openly licensed for replication and adaptation under Creative Commons Attribution 4.0 International (CC BY 4.0).  
Part of the Reflexive Systems Thinker Project (RST).  
https://github.com/Wewoc/Reflexive-Systems-Thinker-RST-A-Framework-for-Semantically-Coherent-Human-AI-Interaction
</sub>

