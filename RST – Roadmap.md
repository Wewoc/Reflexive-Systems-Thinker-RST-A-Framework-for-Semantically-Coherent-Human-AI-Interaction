# RST – Roadmap to Version 1.6 (Repository Plan)

## Phase 1 — Formal Core Stabilization

1. **Implement the RST State Machine**  
   - Flags: RST_ACTIVE, RST_MODE, P3_STATE, HYBRID_STATE  
   - deterministic transitions  
   - optional but recommended: state header in every RST response

2. **Layer Enforcement**  
   - introduce machine-readable CORE / APPLIED / LAB tags  
   - only CORE may define normative rules  
   - strict rule: LAB content must never influence operational behavior

3. **Marker System 2.0**  
   - YAML schema for M-1 to M-4  
   - fixed position at end of response  
   - clear semantics for each marker

4. **P3 Rework**  
   - explicit activation criteria  
   - P3 only allowed with verifiable project-level context  
   - Safety always overrides P3

---

## Phase 2 — Operational Safety & Testing

5. **Fail & Recovery Protocol**  
   - standardized error message  
   - disable P3 and Hybrid modes  
   - perform P0 reset  
   - require explicit reactivation

6. **Replication Protocol 2.0**  
   - outcome categories (Pass / Minor Drift / Major Drift / Fail)  
   - minimal run-log (model, timestamp, outcome)  
   - structured A/B test frame

7. **Minimal Operational Profile**  
   - P0 + mode logic + safety + RAS  
   - all other components declared optional and non-core

---

## Phase 3 — Documentation & External Readiness

8. **README Update**  
   - concise architecture overview  
   - minimal profile  
   - state machine diagram  
   - quickstart for new users

9. **Appendix Updates**  
   - Core Prompt 1.6  
   - Marker Legend 2.0  
   - Replication Protocol 2.0  
   - optional refinements to Quick Matrix

10. **External Reviewer Package**  
   - Stress Test Report v1.6  
   - technical summary  
   - evidence overview

---

## Phase 4 — Optional Extensions

11. Draft preprint / formal paper  
12. Publish replication package (test prompts + sample logs)
