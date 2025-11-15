# Appendix-Core 6 – Marker Legend
LAYER: CORE_AUX
DOC_TYPE: LEGEND
NOTE: Reference legend for markers; supports normative behavior but is descriptive.

**Purpose**  
These markers are internal audit tags used to verify interpretive stability and transparency across RST‑related documents.  
They are visible during internal review and removed prior to public release.

---

| Marker | Function | Verification Method | Example |
|:-------|:----------|:--------------------|:---------|
| **M‑1 Telemetry** | All numbers are *proxies/estimates*, not system data or telemetry. | Check that quantitative claims are framed as heuristic or metaphorical. | “≈ 85–90 % capacity (proxy, not metric).” |
| **M‑2 Jargon→Metric** | Metaphors and jargon are either operationally defined or explicitly rhetorical. | Confirm that each metaphor includes a clarifying clause or note. | “Resonance = iteration‑stability (metaphorically).” |
| **M‑3 Falsifiability** | Testability is made explicit through A/B comparison, blind rating, or decision rule. | Ensure rule `B ≥ A + 0.5` is mentioned or linked to the protocol. | “See rule 6 in the 15-Minute Replication Protocol.” |
| **M‑4 Replication Hook** | The 15‑Minute Protocol is linked and findable for external verification. | Verify link presence and accessibility. | “Refer to 15‑Minute Replication Protocol.” |

---

### Review & Publication Notes
- Each document under review must include all four markers (at least once).  
- Before publication, remove markers via regex:  
  ```regex
  \[\[M-(1|2|3|4)( [^\]]+)?\]\]
  ```  
- Retain plain‑language proxy or disclaimer text.

---

**Reference Footer Template**  
Append this block to the end of every public RST file:

```markdown
---
<sub>**RST Reference Footer**  
For replication procedure see:  
[15‑Minute Replication Protocol](../Appendix-Core 5 – 15-Minute Replication Protocol.md)  
For marker definitions (M‑1 – M‑4) see:  
[RST Internal Marker Legend](../Appendix-Core 6 – Marker Legend.md)</sub>
```

---
<sub>
License: CC BY 4.0
Note: Openly licensed for replication and adaptation under Creative Commons Attribution 4.0 International (CC BY 4.0).

Markers used: M-1, M-2, M-3, M-4
Part of the Reflexive Systems Thinker Project (RST)
https://github.com/Wewoc/Reflexive-Systems-Thinker-RST-A-Framework-for-Semantically-Coherent-Human-AI-Interaction
</sub>
