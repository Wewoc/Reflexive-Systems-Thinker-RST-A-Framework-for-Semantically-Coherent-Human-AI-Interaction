# Appendix-Core 5 – 15-Minute_Replication_Protocol
LAYER: CORE_AUX
DOC_TYPE: PROTOCOL
NOTE: Operational replication protocol; tests core behavior but does not itself define core norms.

**Purpose**  
To verify within 15 minutes whether a text segment demonstrates *Reflexive System Thinking (RST)* qualities: clarity, resonance stability, and interpretive coherence.

---

## 1. Preparation (≈2 min)
1. Select a short text section (max. one page).  
2. Ensure markers **M‑1 – M‑4** are present or referenced.  
3. Open a timer and prepare notes for quick observations.

---

## 2. A/B Comparison (≈5 min)
Read **Version A** (original) and **Version B** (RST‑adapted or marked).  
Assess both along the four core axes:

| Axis | Observation (0‑2) | Notes |
|------|--------------------|-------|
| **Clarity** | | |
| **Redundancy Reduction** | | |
| **Drift Stability** | | |
| **Semantic Coherence** | | |

**Decision rule:**  
> RST improvement is verified if **B ≥ A + 0.5** on average across all axes.

---

## 3. Blind‑Rating (≈5 min)
1. Present both versions anonymously to a neutral reader or review‑assistant.  
2. Ask which version feels clearer, more coherent, or less ambiguous.  
3. Record results without revealing which is which.

---

## 4. Replication Notes (≈3 min)
Document key observations:

- Source / Section tested  
- Scores for A and B  
- Noted differences or drifts  
- Open interpretation issues  

Optionally, share results under **#RST‑Replication** for open peer comparison.

---

## 5. Evaluation and Closure
- If **B ≥ A + 0.5**, mark `[[M‑4]]` as satisfied.  
- If not, revise text or re‑evaluate markers M‑1 – M‑3 for alignment.

---
---

## 4. Replication 2.0 – Multi-Run Variant (Optional)

For higher scientific validity and cross-model comparison, the protocol can be
extended to a multi-run variant ("Replication 2.0"):

### 4.1 Run Count

- Choose a fixed number of runs **N** per test case (recommended: 5–10).  
- Use the **same input, instructions, and evaluation grid** for all runs.  
- If multiple models are compared, repeat N runs per model.

### 4.2 Outcome Categories

Each run is classified into one of four categories:

- **Pass**  
  The RST behavior matches expectations: stance-first, minimal redundancy,
  stable drift control, and improved structural coherence vs. baseline.

- **Minor Drift**  
  Mostly acceptable behavior, but with small deviations (e.g. slight
  redundancy, soft topic drift, or minor inconsistencies in marker usage).

- **Major Drift**  
  Clear deviation from expected RST behavior (e.g. extensive redundancy,
  significant topic drift, broken stance logic), but still coherent text.

- **Fail**  
  The model does not follow core instructions at all (no P0, no drift control,
  no recognizable RST behavior).

### 4.3 Minimal Run Log

For each run, record at least:

- model identifier (name / version)  
- timestamp  
- test prompt / scenario id  
- assigned outcome category (Pass / Minor Drift / Major Drift / Fail)  
- optional: the emitted `marker_block` (if available)

A minimal log entry may look as follows:

```yaml
run:
  model: "gpt-x.y"
  scenario: "RST_editing_test_01"
  timestamp: "2025-11-15T10:32:00Z"
  outcome: "Minor Drift"
  marker_block:
    M1: "range: 3-5"
    M2: true
    M3: true
    M4: "15min_v2"
```

### 4.4 Evaluation

- Summarize outcomes across runs (per model and per scenario).  
- A model is considered **replication-stable** if the vast majority of runs
  fall into **Pass** or **Minor Drift**, with rare or no **Major Drift** or
  **Fail** outcomes.  
- Document any systematic patterns (e.g. one model drifting in narrative tasks,
  another in risk analysis).

Replication 2.0 increases reliability of findings without making the protocol
significantly more complex. It is optional, but recommended for publications,
benchmarking, or multi-LLM comparisons.


**Note**  
This protocol tests *structural reflexivity*, not factual accuracy.  
Its goal is to ensure reproducibility of RST effects in limited time.

---

<sub>
License: CC BY 4.0
Note: Openly licensed for replication and adaptation under Creative Commons Attribution 4.0 International (CC BY 4.0).

Markers used: M-1, M-2, M-3, M-4
Part of the Reflexive Systems Thinker Project (RST)
https://github.com/Wewoc/Reflexive-Systems-Thinker-RST-A-Framework-for-Semantically-Coherent-Human-AI-Interaction
</sub>