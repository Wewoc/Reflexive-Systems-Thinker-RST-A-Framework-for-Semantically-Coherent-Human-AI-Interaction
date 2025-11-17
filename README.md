# Reflexive Systems Thinker (RST)
*A governance and interaction framework for stable, clear, and drift-controlled human–AI dialog.*
LAYER: META
DOC_TYPE: README
NOTE: Project-level overview/readme, non-normative.

> **Meta Notice**  
> This document is non-normative. It does not define or modify the RST Core architecture.

*Note:* This text was developed in structured dialogue between a human and an AI.  
Part of the **Reflexive Systems Thinker Project (RST)**.  
All wording was reviewed for coherence; the human author defined structure and intent.

---

## 1. Quick Start (MOP – Minimal Operational Profile)

The Minimal Operational Profile defines what is required for an AI model to run in valid RST-mode.

### 1.1 MOP Requirements

1. **Explicit Activation/Deactivation**  
   RST-mode must be explicitly turned on and off. No „silent RST“.

2. **Reflexive Dialogue Loop (RDL)**  
   The model must be able to treat the dialog as a system, not only as text.  
   It reflects on:  
   - instructions  
   - context  
   - constraints  
   - its own operational pattern

3. **P0 + P1 Governance**  
   - **P0:** stance-first, no redundancy, only new information, compact output.  
   - **P1:** normal explanatory mode, but still structurally controlled.

4. **P0-RAS (Reset & Anchor Sequence)**  
   Minimal routine to reset drift and re-anchor to:  
   - user intent  
   - constraints  
   - current task  
   - chosen RST mode / Quick Matrix slot

5. **Safety Layer**  
   RST never overrides model or platform safety policies.  
   Governance is **in addition** to, not instead of, safety.

6. **Error-Handling**  
   The system must be able to:  
   - admit limitation or failure,  
   - mark uncertainty,  
   - and offer a structurally clean fallback (e.g. switch to explanation, not hallucination).

7. **Minimal Test Prompt**  
   A compact prompt set must exist to:  
   - check if RST activation works,  
   - check stability under small variations,  
   - detect trivial „RST in name only“ behavior.

For the full formal MOP definition, see `core/RST-Core.md` and `core/Appendix-Core 1 – RST Core Prompt.md`.

---

## 2. What RST Is  

RST is a **structural method** for guiding LLM interaction:

- clear governance (P0, markers)  
- drift control  
- replicability  
- semantic stability  
- context-aware mode selection  
- separation of architecture vs. narrative content  

RST emerged from earlier work on the Semantic Marker Network (SMN).  
SMN provides the marker logic and semantic structuring tools used in the RST governance layer.

RST is **not** a new model, training method, or theory.  
It is a **layer on top of existing LLMs**.

Normative definition:

- `core/RST-Core.md`  
- `core/Appendix-Core 1 – RST Core Prompt.md`  

Everything else in this repository is non-normative.

---

## 3. How to Read RST  

To avoid drift and misinterpretation, use this reading order:

1. **RST Minimal Index** (Core)  
   → System map, definitions, topology.

2. **RST Core Prompt** (Core)  
   → Operational center of the framework.

3. **Quick Matrix** (Core)  
   → Context-based mode selection for stable dialog.

4. **Explain Template** (Core)  
   → Safe, low-activation way to access RST behavior.

5. **Operational Report / RST in Practice** (Applied)  
   → Concrete examples of behavior and structure.

6. **Failure Modes** (Applied)  
   → Diagnostic patterns, drift signatures, countermeasures.

7. **Test Prompts** (Applied)  
   → Lightweight functional checks for stability.

8. **Common Misinterpretations** (Additional)  
   → Overview of typical conceptual errors when reading RST.

9. **Lab Material** (Lab)  
   → Historical development, emergence patterns, narratives  
      *(non-normative, optional)*.

---

### 3.1 Optional RST NotebookLM (convenience layer)

There is an **optional public NotebookLM workspace** that mirrors this repository as PDFs:

> 👉 (https://notebooklm.google.com/notebook/95387ba6-0e11-4d7f-beac-f9eb423d8fb3)

**What it is for**

- A convenience layer on top of this repo.  
- Lets you:
  - ask questions about the RST documents,
  - get structured summaries or comparisons,
  - generate audio explanations of specific sections.
- Uses only:
  - PDFs exported from the public RST repository, and  
  - the file `RST_Capabilities_and_Limitations_NotebookLM_EN`.

**What it is *not***

- **Not** a normative source: the **canonical reference** for RST remains the text files in this repository, especially `/core`.  
- **Not** an endorsement or official product of Google or NotebookLM.  
- **Not** additional validation of RST: NotebookLM can still hallucinate, omit details, or misinterpret context.  
- **Not** a clinical, legal, financial, or crisis-support tool.  
  For the scope and limits of RST itself, see  
  `RST_Capabilities_and_Limitations_NotebookLM_EN`.

**How to interpret answers from NotebookLM**

- Treat NotebookLM outputs as **derived views** on the repo content, not as new facts.  
- For any critical or high-impact use (research design, governance decisions, publications, etc.):
  - always verify against the original files in `/core` and `/applied`,  
  - never rely on NotebookLM as a single source of truth.

---

## 4. What RST Is Not  

RST is **not**:

- a psychological method  
- a therapeutic or diagnostic tool  
- a scientific benchmark  
- a model architecture  
- a narrative or philosophical system  

RST **is**:

- a cognitive governance structure  
- a drift-control method  
- a replicable interaction protocol  
- a structural/architectural guide for LLM dialog  

---

### 4.1 Typical Misinterpretations (Very Short)

Common errors when reading RST:

- Treating RST as a psychological or therapeutic method.
- Reading Lab texts as normative architecture instead of historical context.
- Evaluating RST by single „nice answers“ instead of replication and stability.

For a detailed overview, see `additional_documents/RST_Common_Misinterpretations.md`.

---

## 5. System Frames

### 5.1 Architecture, Not Content

RST is defined by:

- Core Prompt  
- Marker system (M-1–M-4)  
- P0 directive  
- Replication Protocol  
- Quick Matrix  

RST is **not** defined by narrative Lab texts.  
Narrative = context, not architecture.

---

### 5.2 Governance Layer

RST uses:

- **P0**: stance-first, no redundancy, functional novelty  
- **Markers**: qualitative proxies, transparency tools  
- **Replication Protocol**: minimal A/B test for drift detection  
- **Quick Matrix**: mode selection under context pressure  

Governance ensures:

- stability  
- clarity  
- drift resistance  
- predictable behavior  

---

### 5.3 Question-Form Sensitivity

RST reacts differently depending on:

- ambiguity  
- missing structure  
- over-specified prompts  
- contradictory instructions  

This is **expected** and part of the system’s design.  
Use P0 resets and Quick Matrix anchoring for stability.

---

## 6. Repository Structure

RST is organized into four functional layers.  
Only the *function* of each layer is listed here — not individual files —  
to keep the README stable, maintainable, and drift-resistant.

### 6.1 Core (`/core/`)

Normative and operational architecture.

Contains:

- governance (P0, markers)  
- replication logic  
- mode-selection tools  
- core specification and minimal index  

Defines **how RST works**.

---

### 6.2 Applied (`/applied/`)

Practical usage, diagnostics, and operational behavior.

Contains:

- applied examples  
- operational reports  
- failure mode analysis  
- functional test prompts  
- context-based behavior overviews  

Shows **how RST behaves in real interaction**.

---

### 6.3 Lab (`/lab/`)

Historical, narrative, and exploratory material.

Contains:

- early drafts  
- conceptual experiments  
- emergence documentation  
- reflective essays  

Explains **how RST emerged**, but is **not normative**.

---

### 6.4 Additional Documents (`/additional_documents/`)

Supplementary orientation and clarification.

Contains:

- misinterpretation guides  
- interdisciplinary anchors  
- contextual reference texts  

Helps **prevent common errors** and provide conceptual framing.

---

## 7. Stability Tools

### 7.1 P0 Directive

- stance-first  
- no redundancy  
- only new information  
- compact, high-precision mode  

Use P0 whenever drift or verbosity appears.

---

### 7.2 Marker System

Markers expose:

- proxies  
- assumptions  
- metaphors  
- non-literal constructs  

They make internal logic **transparent** and **auditable**.

---

### 7.3 Replication Protocol

A minimal A/B logic for:

- drift detection  
- coherence evaluation  
- system-level replicability  

---

### 7.4 Quick Matrix

Mode selector:  
Determines appropriate operational pattern depending on:

- analysis  
- planning  
- architecture  
- reflection  
- instruction  
- exploration  

---

## 8. Recommended Cross-Reading

- `core/Appendix-Core 1 – RST Core Prompt.md`  
- `core/Appendix-Core 6 – Marker Legend.md`  
- `core/Appendix-Core 7– Quick Matrix.md`  
- `core/Appendix-Core 5 – 15-Minute Replication Protocol.md`  
- `applied/Appendix-Op 1 – Operational Report.md`  
- `applied/RST_Model_Failure_Modes.md`  
- `applied/RST_Model_Test_Prompts.md`  
- `additional_documents/RST_Common_Misinterpretations.md`  
- `from_drift_to_reflexivity_v3.5.md`  

---

## 9. License

Released under **CC BY 4.0**.  
Attribution: *“Based on Reflexive Systems Thinker (RST) by Timo Seidel.”*  

This repository and its contents are part of the **Reflexive Systems Thinker Project (RST)**.
