# Hi, I'm Alimoudine Idrissou 👋

### AI Researcher · Applied AI Engineer · Open-Source Builder

I build **multimodal, agentic AI systems** that turn frontier models into useful, reliable products.

My work sits at the intersection of **LLM engineering, mathematical reasoning, retrieval, multimodal AI, and full-stack product development**. I enjoy taking ambiguous problems from first principles → prototype → evaluation → production.

Currently, I work as an **AI Researcher at Turing**, where I design mathematical evaluations that probe the reasoning limits of frontier AI models.

<p>
  <a href="https://github.com/ialim0">
    <img src="https://img.shields.io/badge/GitHub-ialim0-181717?style=flat-square&logo=github" alt="GitHub" />
  </a>
  <a href="https://www.linkedin.com/in/ialim">
    <img src="https://img.shields.io/badge/LinkedIn-Alimoudine%20Idrissou-0A66C2?style=flat-square&logo=linkedin" alt="LinkedIn" />
  </a>
  <a href="mailto:alimoudineidrissou@gmail.com">
    <img src="https://img.shields.io/badge/Email-Contact%20me-EA4335?style=flat-square&logo=gmail" alt="Email" />
  </a>
</p>

---

## What I'm building

### [open-cvbaba](https://github.com/ialim0/open-cvbaba)

**Open-source, local-first multimodal AI document creator powered natively by the Mistral AI ecosystem.**

The project started in **2024** from a simple frustration: while writing in Overleaf, I wanted the AI generation layer and the document compiler to live in the same interface.

I first built a **LaTeX generation + compilation workflow**, then created a data-annotation platform for CVs and model responses. I generated and validated **50+ LaTeX/PDF examples** and experimented with model training because general-purpose models at the time were not consistently producing the document quality I needed.

The experiment worked technically, but exposed a deeper product problem: **LaTeX was too computationally expensive and too rigid for a great end-user editing experience**.

So I switched the core representation to **HTML/CSS**.

CVs became the ideal proving ground for a larger idea: **agentic document generation**. They are small enough to evaluate cheaply, dynamic enough to stress layout reasoning, and quality-sensitive enough that spacing, overflow, hierarchy, pagination, and wording all matter.

Today, open-cvbaba supports:

- **Mistral Large** for reasoning and document planning
- **Codestral** for HTML/CSS generation
- **Mistral OCR** for PDF/image understanding
- **Voxtral** for real-time voice input over WebSockets
- **SSE streaming** for live document generation
- **Shadow DOM WYSIWYG editing**
- **A4 pagination, snapshots, and version rollback**
- **PDF export with WeasyPrint**
- **Editable Word (.docx) export**
- **FastAPI + Next.js + PostgreSQL + Docker**

The broader problem I am exploring is:

> **intent → content → code → rendered artifact → evaluation → correction**

with AI handling the parts that require reasoning, and deterministic software providing the guarantees around it.

The project generated **3,000+ views in under 24 hours** through organic distribution and led to inbound interest from a UK-based VC director to discuss the product and potential acquisition.

**Stack:** `Python` `FastAPI` `Next.js` `TypeScript` `PostgreSQL` `Mistral AI` `Codestral` `Voxtral` `OCR` `Docker`

---

### [open-vidlib](https://github.com/ialim0/open-vidlib)

**An open-source AI tutor for educational videos.**

open-vidlib began at the **AIMS Scientific Innovation Hackathon** as a browser-only prototype. After the hackathon, I rebuilt it into a full-stack AI platform for searching, understanding, and translating educational videos.

The retrieval pipeline combines:

```text
captions
   ↓
sentence-aware overlapping windows
   ↓
mistral-embed + pgvector
   ↓
vector retrieval + lexical retrieval
   ↓
Reciprocal Rank Fusion
   ↓
deduplication
   ↓
evidence window
   ↓
Mistral Large
   ↓
grounded answer + [MM:SS] citations
```

Students can:

- Search concepts inside long educational videos
- Ask questions grounded strictly in transcript evidence
- Jump directly to the supporting `[MM:SS]` timestamp
- Follow synchronized word-level captions
- Translate lessons
- Generate cached dubbed audio with Voxtral TTS
- Use core functionality even when AI services are unavailable through graceful fallbacks

The project won **1,000,000 XOF** at the **AIMS Scientific Innovation Hackathon, December 2025**.

**Stack:** `FastAPI` `Next.js` `PostgreSQL` `pgvector` `Mistral Embed` `Mistral Large` `Voxtral` `BM25` `RRF` `Docker`

---

## Research

At **Turing**, I work on AI reasoning and evaluation.

I design adversarial mathematical problems and benchmarks intended to expose where frontier models fail under genuine reasoning pressure rather than retrieval or pattern matching.

My work focuses on failure modes such as:

- reasoning collapse
- hallucinated proofs
- false confidence
- hidden logical errors
- weaknesses in self-verifying code
- limits of mathematical generalization

I am especially interested in the boundary between **what models appear to understand and what they can actually reason through reliably**.

---

## Engineering principles

A few ideas increasingly shape how I build AI systems:

- **The model call is rarely the hardest part.** Retrieval, context, orchestration, evaluation, fallbacks, and UX usually determine whether the product is reliable.
- **Use AI where intelligence is needed; keep guarantees deterministic.**
- **Fine-tuning is a tool, not a default.** I prefer to first understand whether the bottleneck is data, prompting, retrieval, model choice, orchestration, or product architecture.
- **Prototype fast, but measure the failure modes early.**
- **Graceful degradation matters.** AI features should not necessarily make the entire product unusable when a model or API is unavailable.
- **I learn best by building.**

---

## Tech I work with

### AI / LLM

![Mistral AI](https://img.shields.io/badge/Mistral_AI-FF7000?style=flat-square)
![RAG](https://img.shields.io/badge/RAG-111827?style=flat-square)
![Agents](https://img.shields.io/badge/Agentic_AI-111827?style=flat-square)
![Multimodal AI](https://img.shields.io/badge/Multimodal_AI-111827?style=flat-square)
![pgvector](https://img.shields.io/badge/pgvector-336791?style=flat-square)
![Evaluation](https://img.shields.io/badge/LLM_Evaluation-111827?style=flat-square)

`Mistral Large` · `Codestral` · `Voxtral` · `Mistral OCR` · `Embeddings` · `Hybrid RAG` · `BM25` · `RRF` · `Function Calling` · `LLM Evaluation`

### Engineering

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=nextdotjs&logoColor=white)
![React](https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Rust](https://img.shields.io/badge/Rust-000000?style=flat-square&logo=rust&logoColor=white)
![Go](https://img.shields.io/badge/Go-00ADD8?style=flat-square&logo=go&logoColor=white)

---

## Background

My path into AI has not been linear, and I consider that an advantage.

- **AI Researcher — Turing**
- **Master's in Digital Transformation — ESMT Dakar, 2023**
- **Bachelor's in Pure Mathematics — Université d'Abomey-Calavi, 2021**
- **Bachelor's in Planning — ENEAM, Université d'Abomey-Calavi, 2021**
- Former **mathematics teacher**
- Software engineering background across **Python, TypeScript, Rust, Go, and JavaScript**

I am particularly interested in environments where **research, engineering, and real-world product problems meet**.

---

## Selected recognition

- 🏆 **AIMS Scientific Innovation Hackathon — 1,000,000 XOF Prize, Dec 2025**  
  Project: **open-vidlib**

- 🏆 **Mastercard Foundation-supported Entrepreneurship Award — $5,000, 2024**  
  Project: **open-cvbaba** · selected among **1,000+ applicants across Senegal**

- 🎓 **Benin Government International Scholarship — ESMT Dakar**

- 🎓 **Benin Government National Scholarship — Faculty of Science & Technology**

---

## What I'm interested in

I am currently most excited by:

- **Agentic systems**
- **Multimodal AI**
- **LLM reasoning and evaluation**
- **RAG and retrieval systems**
- **AI-native developer/product experiences**
- **Document intelligence**
- **AI for education and accessibility**
- **Systems that connect research ideas to real-world products**

---

## Let's connect

If you are working on difficult problems around **AI agents, multimodal systems, reasoning, RAG, evaluation, or AI-native products**, I would be happy to connect.

- GitHub: [github.com/ialim0](https://github.com/ialim0)
- LinkedIn: [linkedin.com/in/ialim](https://www.linkedin.com/in/ialim)
- Email: [alimoudineidrissou@gmail.com](mailto:alimoudineidrissou@gmail.com)

---

<p align="center">
  <i>Build fast. Understand deeply. Keep raising the difficulty of the problems you can solve.</i>
</p>
