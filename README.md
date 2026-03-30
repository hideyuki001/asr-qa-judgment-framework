# Reproducible ASR QA Framework  
Reproducible Decision System for ASR Training Data Quality

---

## 🧠 Why this exists

Most ASR failures are not caused by lack of intelligence.

They are caused by **unstable judgment**.

In real-world annotation work, different reviewers often make inconsistent decisions on:

- unclear audio
- overlap handling
- speaker segmentation
- partial reconstruction

This leads to noisy training data and reduced model reliability.

👉 The goal of this framework is simple:

**Turn subjective decisions into a reproducible system.**

---

## 🔧 What makes this different

This is NOT a theory-based guideline.

This system is built from:

- real ASR rework logs (rework19–35)
- repeated error patterns
- stable decision behaviors observed across tasks

Instead of saying:

> "Use your judgment"

This framework defines:

- when to keep
- when to delete
- when to mark as `(unintelligible)`
- when to split speakers

👉 Decisions are not subjective — they are structured and reproducible.

---

## ⚙️ Core Principles

- audio > grammar  
- uncertain → `(unintelligible)`  
- overlap only if simultaneous  
- no hallucination  
- meaning-preserving deletion  

**Key constraint:**

> If it cannot be reproduced from audio, it must not be included.

---

## 🧩 Pattern-Based System

Decisions are not made ad-hoc.

They follow reusable patterns:

- False Overlap Removal  
- True Overlap Preservation  
- Unintelligible Handling  
- Speaker Resegmentation  
- Partial Reconstruction Guardrails  

👉 This transforms QA into a pattern-driven system.

---

## 🧠 Decision Philosophy

This system prioritizes:

- structure over fluency  
- evidence over assumption  
- reproducibility over intuition  

Every decision must be:

- explainable  
- repeatable  
- verifiable from audio  

---

## 🔁 Decision Flow (Reproducible)
'''
audio input
↓
can it be reproduced from audio?
├─ yes → keep
└─ no
↓
can structure be preserved?
├─ yes → (unintelligible)
└─ no → delete
↓
check overlap (simultaneous only)
↓
check speaker segmentation
↓
finalize
'''


👉 No guessing. No completion. Only reproducible output.

---

## ⚠️ Risk Control

Main failure risks:

- hallucination  
- speculative reconstruction  
- incorrect overlap tagging  
- speaker segmentation errors  

Mitigation strategy:

- default to `(unintelligible)`  
- prohibit context-based completion  
- prioritize structure over fluency  

---

## ⚠️ Scope

This framework is designed for:

- ASR training data QA  
- model robustness improvement  

It is NOT intended for:

- subtitle generation  
- user-facing content optimization  

👉 Context-based completion may be acceptable in UX scenarios,  
but is explicitly prohibited here.

---

## 📂 Examples

Real cases from ASR rework logs:

- Example 01 — False Overlap Correction  
- Example 02 — Unintelligible vs Deletion  
- Example 03 — Speaker Resegmentation  

These demonstrate how decisions are applied in practice.

---

## 🎯 Positioning

This is not:

❌ A collection of case logs  

This is:

✅ A reproducible ASR judgment system  

👉 Not smarter — but more stable.

---

## 🚀 Next

This repository is a lightweight public version.

The full system includes:

- complete pattern library  
- QA review manual  
- auto-review prompt system  

---

## 🤝 Use Cases

- ASR annotation teams  
- QA reviewers  
- AI evaluation pipelines  
- human-in-the-loop systems  

---

## 📌 Author

Hideyuki Okabe  
AI Evaluation & QA Architect
