![Header](https://capsule-render.vercel.app/api?type=waving&color=0,0D1117,161B22,0D1117&height=180&section=header&text=Joel%20Gijo&fontSize=72&fontColor=3FB950&fontAlignY=55&animation=fadeIn&desc=AI%20Engineer%20%E2%80%94%20RAG%20%C2%B7%20LLM%20APIs%20%C2%B7%20Applied%20ML%20%C2%B7%20Kerala%2C%20India&descSize=14&descAlignY=76&descColor=8B949E)

<div align="center">

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://linkedin.com/in/joelgijo)
[![Gmail](https://img.shields.io/badge/Email-EA4335?style=flat-square&logo=gmail&logoColor=white)](mailto:joelgijo03@gmail.com)
[![GitHub](https://img.shields.io/badge/GitHub-muadgijo-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/muadgijo)
[![Open to Work](https://img.shields.io/badge/Open%20to%20Work-Junior%20AI%20Engineer-3FB950?style=flat-square)](mailto:joelgijo03@gmail.com)

</div>

---

## `$ whoami`

```python
profile = {
    "name"     : "Joel Gijo",
    "role"     : "Junior AI Engineer · GenAI Developer · LLM Application Developer",
    "location" : "Kottayam, Kerala, India · Open to remote and relocation",
    "focus"    : ["RAG pipelines", "LLM APIs", "ML inference", "production APIs"],
    "shipped"  : [
        "Production RAG API — live on Render with RAGAS evaluation",
        "AMR-X ML layer — XGBoost on 1.4M clinical records, 2× IEEE papers",
    ],
    "education": "B.Tech CSE — Amal Jyothi College of Engineering (2026)",
}
```

> B.Tech graduate who builds and ships. Not just notebooks — REST APIs, Docker containers, live endpoints.  
> Two IEEE conference papers. One Best Paper Award. One live RAG system you can hit right now.  

---

## `$ ls ~/projects/`

### 🤖 RAGBOT — Production RAG API
> **[Live API](https://ragbot-9knh.onrender.com/) · [Swagger /docs](https://ragbot-9knh.onrender.com/docs) · [GitHub](https://github.com/muadgijo/RAGBOT)**

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![LangChain](https://img.shields.io/badge/LangChain-1C3C3C?style=flat-square&logo=langchain&logoColor=white)
![ChromaDB](https://img.shields.io/badge/ChromaDB-FF6B35?style=flat-square)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Groq](https://img.shields.io/badge/Groq_LPU-F55036?style=flat-square)

A two-stage RAG pipeline over AWS Lambda documentation, deployed as a FastAPI REST service. The engineering story here is production constraints: the naive approach ballooned to a **3.5 GB Docker image with 1–2 GB RAM at runtime** — unusable on free-tier cloud. Switched from SentenceTransformers to **FastEmbed (ONNX)** to bring the image down to **250 MB** and runtime to **<100 MB RAM**.

```
Architecture
────────────────────────────────────────────────────────────────
Query
  ↓
Stage 1 — Vector similarity search (ChromaDB + HuggingFace / FastEmbed)
Stage 2 — Keyword reranking
  ↓
Dual LLM backend   [env-var switch]
  ├── Local:  Ollama (Phi-3) — no-cost inference
  └── Cloud:  Groq LPU — ~2.4 s avg latency
  ↓
FastAPI REST response — structured JSON + source citations

Deployment: Docker → Render  |  Swagger: /docs  |  Health: /health
────────────────────────────────────────────────────────────────
```

**RAGAS LLM-as-Judge evaluation (independent framework, not self-reported):**

| Metric | Score | Notes |
|---|---|---|
| Avg Answer Relevance | **88%** | Across full test set |
| Avg Faithfulness | **69.5%** | Weighted avg (in/out of corpus) |
| Faithfulness — in-corpus | **89–100%** | Queries the corpus can answer |
| Faithfulness — out-of-corpus | **18%** | Expected, documented, explainable |
| Avg Latency | **~2.4 s** | Groq LPU backend |

> The 18% out-of-corpus score is not a bug — it reflects the system correctly refusing to hallucinate beyond the corpus. This is documented in the evaluation writeup.

---

### 🦠 AMR-X — Antimicrobial Resistance Surveillance Platform
> **[Live Demo](https://github.com/ryygeorge/Amr-x) · [GitHub](https://github.com/muadgijo/amrxml) · 2× IEEE Conference Papers (2026)**

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![XGBoost](https://img.shields.io/badge/XGBoost-337AB7?style=flat-square)
![Flask](https://img.shields.io/badge/Flask-000000?style=flat-square&logo=flask&logoColor=white)
![Scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=flat-square&logo=scikit-learn&logoColor=white)
![Firebase](https://img.shields.io/badge/Firebase-FFCA28?style=flat-square&logo=firebase&logoColor=black)

ML inference layer for a 3-tier antimicrobial resistance surveillance platform. Trained an XGBoost classifier on **1.4M clinical records** and wrapped it in a Flask REST API with input validation and rate limiting, deployed on Render. Collaborative project with [@ryygeorge](https://github.com/ryygeorge).

```
Platform tiers
────────────────────────────────────────────────
Public symptom form  →  Firestore  →  ML inference  →  District dashboards
Pharmacist prescription logs  ────────────────↑
────────────────────────────────────────────────

ML layer (my work):
  ✦ XGBoost classifier — 1.4M clinical records
  ✦ ROC-AUC: 0.81 · Sensitivity: 82%
  ✦ Flask REST API + input validation + rate limiting
  ✦ Deployed on Render

Research output:
  ✦ 2× peer-reviewed IEEE Conference Papers (2026)
  ✦ Best Main Project Award — College Expo 2026
  ✦ Best Paper Award — NACCORE 2024 (GeneQuest)
```

> ⚠️ Student research project — not for clinical use.

---

### 📊 Instagram Follower Analyser — Social Data Analytics Tool
> **[GitHub](https://github.com/muadgijo/instagram-analyser) · 2024**

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?style=flat-square&logo=streamlit&logoColor=white)

Python tool that parses Instagram data export archives, identifies non-reciprocal connections, and tracks follower dynamics across multiple exports. Deployed as a Streamlit app with in-memory processing (no data stored). Includes searchable tables, multi-archive comparison, and CSV export for mutuals/unfollower analysis.

---

## `$ cat tech_stack.json`

**RAG & LLM Tooling**

![LangChain](https://img.shields.io/badge/LangChain-1C3C3C?style=for-the-badge&logo=langchain&logoColor=white)
![ChromaDB](https://img.shields.io/badge/ChromaDB-FF6B35?style=for-the-badge)
![HuggingFace](https://img.shields.io/badge/HuggingFace-FFD21E?style=for-the-badge)
![Ollama](https://img.shields.io/badge/Ollama-000000?style=for-the-badge)
![Groq](https://img.shields.io/badge/Groq_API-F55036?style=for-the-badge)

**ML & Data**

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![XGBoost](https://img.shields.io/badge/XGBoost-337AB7?style=for-the-badge)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white)

**APIs & Backends**

![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white)
![Flask](https://img.shields.io/badge/Flask-000000?style=for-the-badge&logo=flask&logoColor=white)
![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?style=for-the-badge&logo=streamlit&logoColor=white)

**Infrastructure & Storage**

![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black)
![Render](https://img.shields.io/badge/Render-46E3B7?style=for-the-badge&logo=render&logoColor=black)

---

## `$ cat experience.log`

```
Luminar Technolab, Kochi — Data Engineering Trainee  [Jun – Aug 2025]
────────────────────────────────────────────────────────────────────
  ✦ Built Python ETL scripts to extract, clean, and standardize
    structured datasets from multiple sources
  ✦ Designed Pandas transformation pipelines and PostgreSQL queries
    for data preparation and EDA workflows
  ✦ Audited datasets for schema inconsistencies and null-value patterns;
    produced structured quality reports reviewed by senior engineers
```

---

## `$ cat achievements.txt`

```
Papers & Awards
────────────────────────────────────────────────
  [2026]  2× IEEE Conference Papers — AMR-X predictive modeling
  [2026]  Best Main Project Award — College Expo
  [2024]  Best Paper Award — NACCORE (GeneQuest)
  [2024]  Best Department Paper — GeneQuest

Certifications
────────────────────────────────────────────────
  Machine Learning — Andrew Ng (Coursera)
  IBM AI Engineering Fundamentals
  Azure Fundamentals — DataCamp
  NPTEL: Machine Learning, DBMS
```

---

## `$ ping joel`

I'm looking for roles in **AI engineering**, **GenAI development**, and **LLM application development** — anywhere I can build real systems, not just demos. Open to **remote** and **relocation**.

<div align="center">

[![LinkedIn](https://img.shields.io/badge/Let's_Connect-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/joelgijo)
[![Email](https://img.shields.io/badge/Email_Me-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:joelgijo03@gmail.com)
[![Repos](https://img.shields.io/badge/All_Repos-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/muadgijo?tab=repositories)

</div>

---

![Footer](https://capsule-render.vercel.app/api?type=waving&color=0,0D1117,3FB950&height=90&section=footer)

<div align="center"><sub>Kottayam, Kerala · Python · ships things · 2026</sub></div>
