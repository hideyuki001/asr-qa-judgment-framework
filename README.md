# ASR QA Judgment Framework
### Reproducible Decision System for Transcription Quality

---

## 🧠 Why this exists

Most ASR failures are not caused by lack of intelligence.

They come from **unstable judgment**.

In real-world annotation work, different reviewers often make different decisions on:

- unclear audio  
- overlap handling  
- speaker segmentation  
- partial reconstruction  

This framework was built to solve that.

👉 The goal is simple:

**Turn subjective decisions into a reproducible system.**

---

## 🔧 What makes this different

This is NOT a guideline based on theory.

This system is built from:

- Real ASR rework logs (rework19–35)  
- Repeated error patterns  
- Stable decision behaviors observed across tasks  

Instead of saying:

> "Use your judgment"

This framework defines:

- when to keep  
- when to delete  
- when to mark as unintelligible  
- when to split speakers  

👉 Decisions are not subjective — they are structured and reproducible.

---

## ⚙️ Core Principles

- audio > grammar  
- uncertain → unintelligible  
- overlap only if simultaneous  
- no hallucination  
- meaning-preserving deletion  

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

## 🧠 Decision Philosophy

This system prioritizes:

- structure over fluency  
- evidence over assumption  
- reproducibility over intuition  

Every decision must be explainable and repeatable.

---

## 🔁 Decision Flow (Simplified)

```plaintext
audio input
  ↓
detect structure
  ↓
is it meaningful?
  ├─ yes → keep
  └─ no
       ↓
   needed for flow?
     ├─ yes → unintelligible
     └─ no  → delete
  ↓
check overlap
  ↓
check speaker
  ↓
finalize
```
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

- [Example 01 — False Overlap Correction](./examples/example_01_false_overlap.md)
- [Example 02 — Unintelligible vs Deletion](./examples/example_02_unintelligible.md)
- [Example 03 — Speaker Resegmentation](./examples/example_03_speaker_split.md)

These show how decisions are made in practice.

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

Full system includes:

Complete Pattern Library
QA Review Manual
Auto-review Prompt System

---

## 🤝 Use cases
- ASR annotation teams  
- QA reviewers  
- AI evaluation pipelines  
- Human-in-the-loop systems  

---

## 📌 Author

Built from real-world ASR evaluation work.

Focused on:

decision stability
reproducibility
structured QA systems
