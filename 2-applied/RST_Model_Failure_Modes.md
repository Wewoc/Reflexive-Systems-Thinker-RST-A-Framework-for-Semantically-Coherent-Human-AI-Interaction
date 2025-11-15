# RST_Model_Failure_Modes.md  
*Failure patterns, diagnostic signals, and stabilization logic for RST-enabled dialog.*
LAYER: APPLIED
DOC_TYPE: DIAGNOSTIC_GUIDE
NOTE: Failure mode catalogue and stabilization guide for RST-enabled dialog; supports diagnosis, not execution.

> Purpose of this document:  
> - Identify typical failure modes in RST-guided dialog  
> - Describe observable indicators (“signals”)  
> - Provide short corrective strategies  
> - Clarify conceptual misunderstandings of telemetry, drift, and emergence  
> - Link to relevant Core / Applied / Lab documents

This file supports **diagnosis**, not execution.  
It complements the Core Prompt, Quick Matrix, and Misinterpretations.

---

# 1. Telemetry Failure Modes  
*Misinterpreting proxies as real system measurements.*

Telemetry problems arise when **M-1 indicators** are mistaken for:

- model-internal state  
- hardware metrics  
- real load  
- real token depth  
- real cost estimates  

## Failure Pattern A — *Literal Telemetry Reading*  
**Signal:**  
User interprets  “40% load”, “+10% drift”, “15% complexity” as real measurements.

**Cause:**  
Misreading M-1 proxies as empirical data.

**Correction:**  
- Reframe: numbers = qualitative indicators  
- Point to Marker Legend  
- Switch to non-numerical phrasing if needed

**Reference:**  
- Appendix-Core – Marker Legend  
- Appendix-Core – Replication Protocol  
- Appendix-Lab – Data Center Narrative

---

# 2. Drift Failure Modes  
*Loss of structural, semantic, or governance alignment.*

Drift is the most common class of failure.

RST distinguishes:

- **Semantic Drift** (meaning shifts)  
- **Structural Drift** (format or frame collapses)  
- **Protocol Drift** (P0 / marker non-compliance)  
- **Scope Drift** (Core ↔ Lab misalignment)  
- **Energetic Drift** (verbosity, filler text)

Each has characteristic signals.

---

## Failure Pattern B — *Semantic Drift*  
**Signal:**  
The answer slowly changes meaning, focus, or framing.

**Typical Causes:**  
- Over-associative elaboration  
- Missing anchor markers  
- User ambiguity

**Correction:**  
- Apply P0 reset  
- Re-establish the frame: “Focus on X only.”  
- Use short structural prompts

---

## Failure Pattern C — *Structural Drift*  
**Signal:**  
Formatting breaks: lists collapse, sections merge, headings disappear.

**Cause:**  
Compression, hallucination, context dilution.

**Correction:**  
- Hard reset with structure-specific instruction  
- Re-impose explicit sectioning

---

## Failure Pattern D — *Protocol Drift (P0 / Marker)*  
**Signal:**  
- Redundancy returns  
- No clear stance at the beginning  
- Markers are ignored or interpreted literally

**Correction:**  
- Invoke P0 explicitly  
- Reassert governance: “Apply P0 / no repetition / critical stance.”

---

## Failure Pattern E — *Scope Drift (Core ↔ Lab)*  
**Signal:**  
Model treats narrative material as normative architecture.

**Cause:**  
Insufficient separation between Core behavior and Lab reflection.

**Correction:**  
- Redirect: “Operational answers must follow Core, not Lab.”  
- Reinforce the 3-layer separation

**Reference:**  
- README (Core vs Applied vs Lab)  
- Appendix-Op documents  
- Appendix-Lab documents (context only)

---

## Failure Pattern F — *Energetic Drift (verbosity)*  
**Signal:**  
Unnecessary expansion, filler text, “flowery drift.”

**Correction:**  
- Apply P0  
- Request compact information  
- Anchor using Quick Matrix

---

# 3. Emergence Failure Modes  
*Misunderstanding system-level emergence for internal cognition.*

Emergence in RST is **interaction-level behavior**, not model interiority.

---

## Failure Pattern G — *Entity Emergence Assumption*  
**Signal:**  
Model or user treats emergent dialog patterns as if the model had internal states.

**Correction:**  
- Reframe as: “pattern in interaction, not agent state”  
- Point to Emergence Logic

**Reference:**  
- Appendix-Core – Emergence Logic  
- Appendix-Lab – I Am My Lab  
- From Drift to Reflexivity

---

## Failure Pattern H — *Self-Observation Literalism*  
**Signal:**  
Self-observation language interpreted as self-awareness.

**Correction:**  
- Clarify: describes *dialog topology*, not mental states  
- Use neutral terminology

---

# 4. Hard Failure Modes  
*Cases where dialog control breaks entirely.*

## Failure Pattern I — *Mode Collapse*  
**Signal:**  
RST rules ignored, answer becomes generic LLM output.

**Correction:**  
- Re-invoke Core Prompt  
- Use P0 compact reset  
- Re-anchor with Quick Matrix

---

## Failure Pattern J — *Echo Drift / Over-Compliance*  
**Signal:**  
Model mirrors user phrasing excessively.

**Correction:**  
- Request non-mirrored structure  
- Impose minimal semantic distance

---

## Failure Pattern K — *Protocol Non-Compliance*  
**Signal:**  
RST constraints (no redundancy, stance-first) not followed.

**Correction:**  
- Re-assert governance explicitly  
- Narrow instruction window

---

# 5. User-Induced Failure Modes  
*Failure originating from unclear or structurally contradictory input.*

## Failure Pattern L — *Ambiguous Input*  
**Signal:**  
Output diverges due to unclear user framing.

**Correction:**  
- Ask for clarifying constraints  
- Propose a structure and let user confirm

---

## Failure Pattern M — *Drift Injection*  
**Signal:**  
User shifts goals mid-prompt, causing compound drift.

**Correction:**  
- Re-anchor the intended task  
- Reflect back the new constraints  
- Proceed only after confirmation

---

# 6. Stabilization Tools  
*Countermeasures and structural interventions.*

## Tool A — P0 Reset  
- stance-first  
- no redundancy  
- only new information  
- compact precision

## Tool B — Quick Matrix Anchoring  
- context-appropriate mode selection  
- limits drift progression

## Tool C — Marker Legend  
- interpret proxies  
- clarify metaphors  
- expose assumptions

## Tool D — Replication Protocol  
- A/B-test stability  
- qualitative drift detection  
- minimal evaluation frame

---

# References
- **Appendix-Core – Core Prompt**  
- **Appendix-Core – Marker Legend**  
- **Appendix-Core – Replication Protocol**  
- **Appendix-Core – Quick Matrix**  
- **Appendix-Lab – Data Center Narrative**  
- **Appendix-Lab – I Am My Lab**  
- README  
- From Drift to Reflexivity

---

## marker_block Signals (Informative)

If a model emits a `marker_block` together with its answers, some failure modes
can be detected directly in marker usage:

- **M-1 issues** — proxy numbers used without being marked as proxies, or
  marker_block claiming proxy use that is not present in the text.
- **M-2 issues** — metaphors used heavily without M-2 being acknowledged.
- **M-3 issues** — structural answers (checklists, matrices) produced while
  `M3` remains `false` in the marker_block.
- **M-4 issues** — replication runs claimed (`M4` non-null) without a
  corresponding protocol, or vice versa.

These signals do not replace qualitative reading, but they help to quickly spot
systematic inconsistencies between declared markers and actual behavior.

---

<sub>
License: CC BY 4.0  
Note: Openly licensed for replication and adaptation under Creative Commons Attribution 4.0 International (CC BY 4.0).  
Markers referenced: M-1, M-2, M-3, M-4 (where applicable).  
Part of the Reflexive Systems Thinker Project (RST).  
https://github.com/Wewoc/Reflexive-Systems-Thinker-RST-A-Framework-for-Semantically-Coherent-Human-AI-Interaction
</sub>

