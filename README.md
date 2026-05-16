![Header](https://capsule-render.vercel.app/api?type=venom&color=0,0D1117,0D1117,0D1117&height=200&section=header&text=JOEL%20GIJO&fontSize=80&fontColor=3FB950&fontAlignY=55&animation=fadeIn&desc=muadgijo%20%E2%80%94%20CSE%20%C2%B7%20AMR%20%C2%B7%20ML%20%C2%B7%20Kerala&descSize=15&descAlignY=75&descColor=8B949E)

![Typing SVG](https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=600&size=16&duration=3500&pause=1000&color=3FB950&center=true&vCenter=true&width=750&lines=building+ML+tools+for+antibiotic+resistance+%F0%9F%A7%AC;CSE+undergrad+%7C+bioinformatics+%7C+Kerala%2C+India;half+tweaked+out.+fully+committed+to+the+work.;14+repos+%E2%80%94+one+mission.)

[![LinkedIn](https://img.shields.io/badge/-LinkedIn-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://linkedin.com/in/joel-gijo-41007b359)
[![Gmail](https://img.shields.io/badge/-Email-EA4335?style=flat-square&logo=gmail&logoColor=white)](mailto:joelgijo03@gmail.com)
[![GitHub followers](https://img.shields.io/github/followers/muadgijo?style=flat-square&color=3FB950&label=followers)](https://github.com/muadgijo?tab=followers)
[![Profile Views](https://komarev.com/ghpvc/?username=muadgijo&color=3fb950&style=flat-square)](https://github.com/muadgijo)

---

![divider](https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif)

## `$ whoami`

```python
profile = {
    "name"      : "Joel Gijo",
    "alias"     : "muadgijo",
    "age"       : 22,
    "location"  : "Kerala, India",
    "status"    : "Limbo — undergrad, researcher, builder",
    "focus"     : [
        "Antimicrobial Resistance (AMR)",
        "Machine Learning for Healthcare",
        "Bioinformatics"
    ],
    "current"   : "Building the AMR-X ecosystem",
    "goal"      : "Open-source tools that help track antibiotic resistance",
    "warning"   : "Student research project — not for clinical use"
}
```

> Antimicrobial resistance kills over **1.27 million people a year** and most of the good tooling is either paywalled, brittle, or built for labs with 10 PhDs on staff. I'm building open, honest, ML-powered tools to help close that gap — one model, one pipeline, one repo at a time.

![divider](https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif)

---

## `$ ls ~/projects/amr/`

> The core ecosystem — everything feeds into predicting and tracking antibiotic resistance.

### 🔬 [amrxml](https://github.com/muadgijo/amrxml) — XGBoost AMR Prediction Engine

[![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)](https://github.com/muadgijo/amrxml)
[![XGBoost](https://img.shields.io/badge/XGBoost-337AB7?style=flat-square)](https://github.com/muadgijo/amrxml)
[![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?style=flat-square&logo=streamlit&logoColor=white)](https://github.com/muadgijo/amrxml)
[![Stars](https://img.shields.io/github/stars/muadgijo/amrxml?style=flat-square&color=3FB950)](https://github.com/muadgijo/amrxml/stargazers)

The heart of the AMR-X project. Feed it an **organism + antibiotic pair**, get back a **resistance probability**. Trained on real clinical microbiology data from Hugging Face datasets.

```
Input:  Organism (e.g. E. coli) + Antibiotic (e.g. Ciprofloxacin)
Output: Resistance probability  →  0.87  ⚠️ High resistance likely

Evaluation: ROC-AUC (because raw accuracy on imbalanced clinical
            data is a lie and I know better)
Demo:       Streamlit app for interactive testing
```

**What makes it different:** Most AMR models are stuck in research papers. This one ships with a working demo and honest evaluation metrics.

---

### ⚙️ [amrx-ml-service](https://github.com/muadgijo/amrx-ml-service) — ML Microservice Layer

[![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)](https://github.com/muadgijo/amrx-ml-service)
[![Flask](https://img.shields.io/badge/Flask-000000?style=flat-square&logo=flask&logoColor=white)](https://github.com/muadgijo/amrx-ml-service)
[![Stars](https://img.shields.io/github/stars/muadgijo/amrx-ml-service?style=flat-square&color=3FB950)](https://github.com/muadgijo/amrx-ml-service/stargazers)

Wraps the AMR-XML model into a REST API so the full-stack platform can actually talk to it. This is where research meets engineering — the bridge between a trained model and a real application.

```
amrxml model  →  Flask REST API  →  AMR-X Platform frontend
                      ↑
              [amrx-ml-service]
```

**Status:** Active development · Core service for the AMR-X platform

---

### 📊 [Amr-x-ML](https://github.com/muadgijo/Amr-x-ML) — Notebooks & Experiments

[![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=flat-square&logo=jupyter&logoColor=white)](https://github.com/muadgijo/Amr-x-ML)
[![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)](https://github.com/muadgijo/Amr-x-ML)

The R&D layer. All the experiments, model iterations, data exploration, and dead ends that eventually led to amrxml. Messy by design — this is where the actual thinking happens before it gets cleaned up into production code.

```
Data exploration  →  Feature engineering  →  Model selection
                                                    ↓
                                           amrxml production model
```

---

### 🌐 [AMR-X Platform](https://github.com/ryygeorge/Amr-x) — Full-Stack Surveillance System

[![Flask](https://img.shields.io/badge/Flask-000000?style=flat-square&logo=flask&logoColor=white)](https://github.com/ryygeorge/Amr-x)
[![Firebase](https://img.shields.io/badge/Firebase-FFCA28?style=flat-square&logo=firebase&logoColor=black)](https://github.com/ryygeorge/Amr-x)
[![ChartJS](https://img.shields.io/badge/Chart.js-FF6384?style=flat-square&logo=chart.js&logoColor=white)](https://github.com/ryygeorge/Amr-x)

The full-stack system that ties everything together. Collaborative project with [@ryygeorge](https://github.com/ryygeorge).

```
Architecture:

  Public symptom form  ──▶  Firestore  ──▶  ML prediction  ──▶  Dashboard
                                ▲
                    Pharmacist prescription logs

Features:
  ✦ Symptom submission interface (public-facing)
  ✦ Prescription logging module (pharmacist-facing)
  ✦ Resistance trend dashboards with Chart.js
  ✦ Role-based access control
  ✦ ML predictions via amrx-ml-service
```

**Status:** 🚧 Active development · Academic research project · Not production-ready

---

![divider](https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif)

## `$ ls ~/projects/bioinformatics/`

> Sequence analysis, genomics, and learning the biology layer.

### 🧬 [GeneQuest](https://github.com/muadgijo/GeneQuest) — Gamified Gene Research Platform

[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)](https://github.com/muadgijo/GeneQuest)
[![Stars](https://img.shields.io/github/stars/muadgijo/GeneQuest?style=flat-square&color=3FB950)](https://github.com/muadgijo/GeneQuest/stargazers)

Forked from [@jeffinjk](https://github.com/jeffinjk/GeneQuest) and contributed to. A platform that makes genomics and gene research explorable through a game-like interface. The idea: learning sequences and gene function shouldn't feel like reading a textbook.

```
Gene research  +  Game mechanics  =  Actually learning bioinformatics
```

---

### 🔭 [Bioinformatics-Python-Kaggle](https://github.com/muadgijo/Bioinformatics-Python-Kaggle) — Learning Notebooks

[![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=flat-square&logo=jupyter&logoColor=white)](https://github.com/muadgijo/Bioinformatics-Python-Kaggle)
[![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)](https://github.com/muadgijo/Bioinformatics-Python-Kaggle)

Kaggle-based bioinformatics exercises in Python — sequence alignment, FASTA parsing, genomic analysis with Biopython. The learning log. Every notebook is me getting a little less bad at computational biology.

```
Topics:
  ✦ Sequence alignment (pairwise, multiple)
  ✦ FASTA file parsing and manipulation
  ✦ Basic genomic analysis scripts
  ✦ Biopython workflows
```

---

![divider](https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif)

## `$ ls ~/projects/ai-ml/`

> ML tooling, RAG systems, and applied AI experiments.

### 🤖 [RAGBOT](https://github.com/muadgijo/RAGBOT) — Local RAG System

[![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)](https://github.com/muadgijo/RAGBOT)
[![LangChain](https://img.shields.io/badge/LangChain-1C3C3C?style=flat-square&logo=langchain&logoColor=white)](https://github.com/muadgijo/RAGBOT)
[![HuggingFace](https://img.shields.io/badge/HuggingFace-FFD21E?style=flat-square)](https://github.com/muadgijo/RAGBOT)

A fully local RAG (Retrieval-Augmented Generation) pipeline for AWS Lambda documentation. No cloud APIs, no OpenAI key. Runs entirely on your machine.

```
Pipeline:

  Noisy markdown docs
       ↓
  Cleaning + chunking
       ↓
  ChromaDB vector store  ←  HuggingFace embeddings
       ↓
  Ollama (Phi-3)  →  Local QA responses
       ↓
  Retrieval inspection utilities
```

**Why it exists:** Understanding the retrieval stack from the ground up — not just calling an API and hoping for the best.

---

![divider](https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif)

## `$ ls ~/projects/web/`

> Client work and web projects.

### 🌍 [FutureHygenics](https://github.com/muadgijo/FutureHygenics) — Company Website

[![HTML](https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white)](https://github.com/muadgijo/FutureHygenics)
[![TailwindCSS](https://img.shields.io/badge/Tailwind-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white)](https://github.com/muadgijo/FutureHygenics)
[![Stars](https://img.shields.io/github/stars/muadgijo/FutureHygenics?style=flat-square&color=3FB950)](https://github.com/muadgijo/FutureHygenics/stargazers)

Production-style static site built for FutureHygenics. Mobile-first layout, Tailwind CDN, deploy-ready for Cloudflare Pages or Netlify. Lightweight, fast, no fluff.

```
Stack:  HTML · Tailwind CSS (CDN)
Deploy: Cloudflare Pages / Netlify ready
Type:   Mobile-first, single page
```

---

![divider](https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif)

## `$ cat tech_stack.json`

**Core**

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)

**Machine Learning**

![XGBoost](https://img.shields.io/badge/XGBoost-337AB7?style=for-the-badge)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white)
![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?style=for-the-badge&logo=streamlit&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=for-the-badge&logo=jupyter&logoColor=white)

**RAG & LLM Tooling**

![LangChain](https://img.shields.io/badge/LangChain-1C3C3C?style=for-the-badge&logo=langchain&logoColor=white)
![ChromaDB](https://img.shields.io/badge/ChromaDB-FF6B35?style=for-the-badge)
![Ollama](https://img.shields.io/badge/Ollama-000000?style=for-the-badge)
![HuggingFace](https://img.shields.io/badge/HuggingFace-FFD21E?style=for-the-badge)

**Backend & Databases**

![Flask](https://img.shields.io/badge/Flask-000000?style=for-the-badge&logo=flask&logoColor=white)
![Firebase](https://img.shields.io/badge/Firebase-FFCA28?style=for-the-badge&logo=firebase&logoColor=black)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white)

**Web**

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![TailwindCSS](https://img.shields.io/badge/Tailwind-06B6D4?style=for-the-badge&logo=tailwindcss&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![ChartJS](https://img.shields.io/badge/Chart.js-FF6384?style=for-the-badge&logo=chart.js&logoColor=white)

**Bioinformatics**

![Biopython](https://img.shields.io/badge/Biopython-2FA44F?style=for-the-badge&logo=python&logoColor=white)

**Learning**

![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white)

---

![divider](https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif)

## `$ git log --stat`

| ![GitHub Stats](https://github-readme-stats.vercel.app/api?username=muadgijo&show_icons=true&theme=github_dark&hide_border=true&bg_color=0D1117&title_color=3FB950&icon_color=3FB950&text_color=8B949E) | ![Streak Stats](https://github-readme-streak-stats.herokuapp.com/?user=muadgijo&theme=github-dark-blue&hide_border=true&background=0D1117&ring=3FB950&fire=FF6B35&currStreakLabel=3FB950&sideLabels=8B949E) |
|:-:|:-:|
| ![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=muadgijo&layout=compact&theme=github_dark&hide_border=true&bg_color=0D1117&title_color=3FB950&text_color=8B949E&langs_count=8) | ![Activity Graph](https://github-readme-activity-graph.vercel.app/graph?username=muadgijo&bg_color=0D1117&color=3FB950&line=3FB950&point=FFFFFF&area=true&area_color=3FB95020&hide_border=true) |

---

![divider](https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif)

## `$ cat roadmap.txt`

```
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

  NOW
  ├── AMR-XML model tuning (better features, reduce overfitting)
  ├── RAGBOT retrieval pipeline improvements
  └── FutureHygenics content + deployment

  NEXT
  ├── Deploy AMR-X platform (public beta)
  ├── Mobile-friendly symptom intake form
  ├── Auth layer for AMR-X
  └── Sequence-level resistance classifier

  PLANNING
  ├── Live AMR resistance heatmap by region (D3.js + Flask)
  │     aggregated prescription data, zero PII stored
  ├── AMR-XML research writeup / paper
  └── First open-source contributions outside own repos

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

---

![divider](https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif)

## `$ ping joel`

I'm interested in connecting with people working on:

- 🧬 **Bioinformatics** — sequence analysis, genomics, computational biology
- 🦠 **AMR research** — building surveillance tools or working with clinical micro data
- 🤖 **Healthcare ML** — real applications, not toy demos
- 📊 **Public health informatics** — open data, population-level tooling

**Let's talk if you're building something real.**

[![Let's Connect](https://img.shields.io/badge/Let's_Connect-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/joel-gijo-41007b359)
[![Email Me](https://img.shields.io/badge/Email_Me-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:joelgijo03@gmail.com)
[![All Repos](https://img.shields.io/badge/All_Repos-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/muadgijo?tab=repositories)

---

![Footer](https://capsule-render.vercel.app/api?type=waving&color=0,0D1117,3FB950&height=100&section=footer&reversal=false)

<b><sub>built in Kerala · powered by Python · fueled by the problem · 2026</sub></b>
