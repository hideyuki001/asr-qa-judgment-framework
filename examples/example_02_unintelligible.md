# Example 02 — Unintelligible vs Deletion

## Case A — Low Information Noise

### Input
Unclear audio with no meaningful contribution.

### Decision
Delete

### Reasoning
- No impact on sentence meaning  
- No structural dependency  
- Removing improves clarity  

---

## Case B — Meaning-Critical Uncertainty

### Input
Unclear audio affecting sentence meaning.

### Decision
(unintelligible)

### Reasoning
- Affects interpretation  
- Cannot be reliably reconstructed  
- Required to preserve structure  

---

## Key Insight
Unclear audio should not always be preserved.
It should be evaluated based on its impact on meaning and structure.

---

## Decision Rule
- If meaning required → keep as (unintelligible)  
- If not → delete  

---

## Decision Trace

### Case A
- Audio clarity: low  
- Meaning impact: none  
- Structural role: none  
→ Action: delete  

### Case B
- Audio clarity: low  
- Meaning impact: high  
- Structural role: required  
→ Action: (unintelligible)  

---

## Outcome
- Noise reduced without loss of meaning  
- Critical uncertainty preserved without hallucination  
