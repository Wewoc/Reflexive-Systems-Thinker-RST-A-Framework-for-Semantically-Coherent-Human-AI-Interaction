# RST – Effects by Context (extended with typical LLM applications) · v1.1
LAYER: APPLIED
DOC_TYPE: REFERENCE
NOTE: Applied reference for RST effects by context, non-normative.

> Quick reference: How **RST** changes the response logic in common LLM use cases. Benefit → Result. Focus: **Decision capability**, **drift control**, **form–function coherence (P0)**.

---

## 1) Quick Matrix (extended): Use → Primary Result

| Use (Mode) | Typical Input | Output Form | Primary Effect through RST | Core Marker | Risk/Trade-off |
|---|---|---|---|---|---|
| **A. Decision Question** | “Should I do X or Y?” | **Checklist + Recommendation** | Switches to **decision mode** | Thresholds, DoD, minimal variant | Compression under uncertainty |
| **B. Technical Question** | Norm/Rule/Parameter | **Rule sheet + Table** | Contextualizes standards | Reference → Action | False sense of certainty |
| **C. Planning/Project** | Goal + Constraints | **Plan (steps/milestones)** | **Operationalization** | Risks, checkpoints | Less exploration |
| **D. Risk Analysis** | “What can go wrong?” | **Risk heatmap** | Risk chains & triggers | Early markers, residual risk | Conservative bias |
| **E. Research Synthesis** | 5–10 sources | **Evidence synopsis** | Context harmonization | Evidence levels, gaps | Nuance loss |
| **F. Brainstorming** | Open idea | **Option funnel** | Divergence → Convergence | Clusters, criteria | Creativity flattened |
| **G. Writing/Editing** | Draft text | **Structural edit** | Drift control | Tone/coherence | “Too factual” |
| **H. Meeting/Notes** | Conversation log | **Decision protocol** | Decisions/To-Dos | Owner/Deadline | Soft signals missing |
| **I. Code/Review** | Diff/Requirement | **Review checklist** | Error/rule alignment | Tests/DoD | Rule overweight |
| **J. UX/Product** | Use case/Jobs | **JTBD board** | Outcome focus | Jobs/Pains/Gains | Microcopy missing |
| **K. Teaching/Explanation** | “How does … work?” | **Guide + Check** | Learning path/tests | Mini examples | Warmth ↓ |
| **L. Conflict/Trade-off** | Positions/Constraints | **Trade-off matrix** | Criteria/Weighting | Weight factors | Empathy ↓ |
| **M. E-Mail/Letter** | Bullet points/Goal | **One-pager + DoD** | **Purpose-bound writing** | Goal, CTA, audience fit | Tone may sound strict |
| **N. Summary (Executive)** | Long text | **1-Pager** | **Signal > Noise** | Key statements, implications | Details lost |
| **O. Translation/Localization** | Text + Glossary | **Terminology-faithful version** | **Coherent terminology** | Glossary binding, QA questions | Creative nuance ↓ |
| **P. Data Extraction** | Contract/Protocol | **Field table** | **Field/criteria definition** | Regex/Span marker | Edge cases overlooked |
| **Q. Tables/Excel/SQL** | Question + Schema | **Query/Formula + DoD** | **Query with validation marker** | Test case, expectations | Schema assumptions risky |
| **R. Regex/Validation** | Rules/Examples | **Regex + Tests** | **Example-first + negative tests** | Acceptance data | Possible over-fit |
| **S. CLI/DevOps** | Goal/Environment | **Commands + Guardrails** | **Safe defaults** | Dry-run, rollback | Too conservative |
| **T. API/Contract** | Endpoint sketch | **API spec + Tests** | **Acceptance criteria** | Status codes, errors | Detail depth ↑ effort |
| **U. Test Case Generation** | User story | **Test matrix** | **Happy/Edge/Fail** | Oracle/Claims | Maintenance load |
| **V. Release Notes/Changelog** | Commits | **Structured notes** | **User-value focus** | Impact, breaking | Marketing warmth ↓ |
| **W. CV/Job Match** | JD + Résumé | **Fit matrix + Gap plan** | **Criteria matching** | Must/Can, evidence | Personal tone ↓ |
| **X. Support/Response Macros** | FAQ/Tickets | **Macro set + Triggers** | **Consistency & escalation** | When/Then, escalate | Case nuance loss |
| **Y. SEO/Content Briefing** | Keyword goal | **Briefing + Outline** | **Goal-oriented structure** | Intent, H2/H3, DoD | Creative language ↓ |
| **Z. Experiment Design/A-B** | Hypothesis | **Experiment plan** | **Metrics/Abort criteria** | MDE, power hints | Rigid for exploratory work |

---

## 2) Concrete Pairings (additional)

12. **“Please email client X (goal Y)”** → **One-pager with CTA**  
    - Structure: Goal → Core message → Evidence → CTA → **DoD** (response/success criterion).

13. **“Long doc → Exec summary”** → **1-Pager**  
    - 5 sentences: Problem, approach, finding, implication, decision/next. **Acceptance: 150–250 words.**

14. **“Scan contract”** → **Data-extraction table**  
    - Fields/definitions, positive/negative examples, **confidence**, **escalation rule**.

15. **“SQL for metric X”** → **Query + Test cases**  
    - Query, controlled sample, **expected values** (e.g., sum/count).

16. **“Regex for serial numbers”** → **Regex + Pos/Neg set**  
    - 8 positive, 8 negative examples, **false-positive killer**.

17. **“K8s/Terraform hardening”** → **Checklist + Safe defaults**  
    - Dry-run, rollback plan, **abort trigger**.

18. **“API design”** → **Spec + Error catalog + Tests**  
    - Resources, schemas, 5 error cases, **contract-test sketch**.

19. **“User Story → Tests”** → **Test matrix**  
    - Happy/Edge/Failure, **oracle** (expected state), stop conditions.

20. **“CV → JD match”** → **Fit matrix**  
    - Must/Can/Nice-to-Have, evidence points, gap plan (next probe).

21. **“Support macro”** → **Macro set**  
    - When/Then, escalation conditions, **DoD** (ticket closure).

22. **“SEO briefing”** → **Outline with intent**  
    - Search intent, H2/H3, metric KPI, **no-go words**, interlinking.

23. **“A/B test plan”** → **Experiment plan**  
    - Hypothesis, metric, MDE estimate, runtime, **abort criteria**.

---

## 3) Pipeline Snippets for Copy-Paste

- **E-mail (Target text):**  
  > RST on. Generate an **email to [recipient]** with **[goal]**. Structure: **core message → 2 pieces of evidence → CTA**. **DoD:** recipient can decide in **one sentence**.

- **Exec Summary:**  
  > RST on. Compress into **1-pager** (150–250 words): **problem, approach, result, implication, decision.** **No redundancy.**

- **Data Extraction:**  
  > RST on. Extract fields **[list]** from **[document]**. Provide **table + field definitions + pos/neg examples + confidence + escalation rule.**

- **SQL/Excel:**  
  > RST on. Deliver **query/formula** for **[goal]** incl. **test cases** (small sample dataset + expected values).

- **Regex:**  
  > RST on. Generate **regex** for **[pattern]** with **8 positive and 8 negative examples** and explain the **false-positive killer**.

- **API Spec:**  
  > RST on. Sketch an **API** for **[use case]** including **resources, error cases, status codes, contract-test sketch**. Include **guardrails**.

---

## 4) Quality Markers (Alpha Metrics)

- **Signal-to-Noise:** > 4 : 1  
- **Verifiability:** Acceptance criteria present  
- **Context Binding:** Goal/Constraint explicitly linked  
- **Divergence/Convergence:** > 1 option + clear recommendation  
- **Redundancy:** < 5 %  

---

## 5) When a Standard LLM Is Sufficient

- Empathic writing, storytelling, open exploration, idea warm-ups.  
- Translations without glossary enforcement or terminology governance.  
- Low-stakes conversation.

**Hybrid recommendation:** Start in **standard mode** → once a decision need appears: **RST on** → fix result → optionally **RST off** for stylistic refinement.

---

*End – v1.1. Next step: Domain-specific profiles (law, medicine, manufacturing, sales).*


---

<sub>**RST Reference Footer**  
For replication procedure see:  
[15-Minute Replication Protocol](../Appendix-Core 5 – 15-Minute Replication Protocol.md)  
For marker definitions (M-1 – M-4) see:  
[RST Internal Marker Legend](../Appendix-Core 6 – Marker Legend.md)</sub>

---

<sub>License: CC BY 4.0 — Attribution required.  
Part of the **Reflexive Systems Thinker Project (RST)**  
https://github.com/Wewoc/Reflexive-Systems-Thinker-RST-A-Framework-for-Semantically-Coherent-Human-AI-Interaction</sub>

