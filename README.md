These principles are consistently validated across all logs.

They are derived from real-world ASR evaluation and rework processes.

---

## 🧩 Pattern-Based System

Decisions are not made ad-hoc.

They follow reusable patterns:

- False Overlap Removal  
- True Overlap Preservation  
- Unintelligible Handling  
- Speaker Resegmentation  
- Partial Reconstruction Guardrails  

👉 This transforms QA into a **pattern-driven system**.

---

## 🔁 Decision Flow (Simplified)


audio input
↓
detect structure
↓
is it meaningful?
↓ yes → keep
↓ no
↓ needed for flow?
↓ yes → unintelligible
↓ no → delete
↓
check overlap
↓
check speaker
↓
finalize


---

## ⚠️ Risk Control

### Main failure risks:
- hallucination  
- false reconstruction  
- incorrect speaker segmentation  

### Mitigation strategy:
- default to unintelligible  
- avoid speculative completion  
- prioritize structure over fluency  

---

## 📂 Examples

👉 Real cases from ASR rework logs:
