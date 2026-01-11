# AI_Tutor

# 🧠 Adaptive AI Tutor (Agentic Learning System)

An adaptive AI-powered tutoring system that evaluates learner understanding checkpoint-by-checkpoint, dynamically generates questions, scores answers, detects weak concepts, and reteaches using the Feynman Technique.

This project showcases agentic AI design, semantic retrieval, and iterative learning loops using modern LLM infrastructure.

---

## 📌 Overview

The system guides a learner through structured checkpoints.

For each checkpoint, it:

- Gathers learning context
- Validates semantic relevance
- Generates adaptive questions
- Evaluates learner answers
- Identifies weak concepts
- Reteaches using simplified explanations
- Reassesses until mastery or retry limit

---

## 🚀 Key Features

- 📚 Checkpoint-based learning architecture
- 🧠 Semantic relevance filtering using embeddings
- 📄 Context ingestion from:
  - User notes
  - Uploaded PDFs
  - Live web search (fallback)
- ✂️ Intelligent text chunking
- 🧬 Temporary in-memory vector store
- ❓ Adaptive question generation with strict constraints
- 📝 Per-question scoring (0–100)
- 🔍 Learner-specific weak concept detection
- 🎓 Feynman Technique remediation
- 🔁 Teach → Test → Reteach loop
- 🧪 Automated evaluation suite
- 📄 Full LLM prompt & response logging to PDF

---

## 🏗️ System Architecture

```text
Checkpoint
↓
Context Gathering
↓
Semantic Validation
↓
Chunking + Embeddings
↓
Question Generation
↓
Answer Evaluation
↓

┌───────────────┐
│ Pass ≥ 70% ✅ │──▶ END
└───────────────┘
│
▼
Feynman Teaching (Weak Concepts)
│
└──────▶ Re-test
