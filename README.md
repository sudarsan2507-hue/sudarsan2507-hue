<a href="https://sudarsan2507-hue.github.io/Portfolio/"><img src="assets/banner.svg" alt="Sudarsan Ravichandran — I build AI that learns from its mistakes" width="100%" /></a>

<div align="center">

[![Portfolio](https://img.shields.io/badge/Portfolio-3D_site-22d3ee?style=for-the-badge&logo=githubpages&logoColor=white)](https://sudarsan2507-hue.github.io/Portfolio/)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/sudarsan-ravichandran-82b209391)
[![Kaggle](https://img.shields.io/badge/Kaggle-20BEFF?style=for-the-badge&logo=kaggle&logoColor=white)](https://www.kaggle.com/sudarsan007r)
[![IEEE](https://img.shields.io/badge/IEEE_Xplore-00629B?style=for-the-badge&logo=ieee&logoColor=white)](https://ieeexplore.ieee.org/author/607201746740566)
[![Email](https://img.shields.io/badge/Email-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:sudarsan2507@gmail.com)

</div>

<img src="assets/avatar.png" width="96" align="right" alt="Sudarsan Ravichandran" />

I'm a CSE (AI & ML) student at VIT Chennai. Most of my work asks one question:
**how do you stop a system from repeating a mistake it has already made?**

It began as a retrieval problem during my NLP research internship at NIT Trichy, and it has pulled me into
graph search, the security of LLM-written code, and guardrails for AI agents. I care about evaluation that
reports the flat results too, and I build the backends and hardware to put this work in front of people.

**[→ Explore the 3D portfolio](https://sudarsan2507-hue.github.io/Portfolio/)** &nbsp;·&nbsp; [2-minute version](https://sudarsan2507-hue.github.io/Portfolio/#crisp) &nbsp;·&nbsp; [full tour](https://sudarsan2507-hue.github.io/Portfolio/#detailed)

## Highlights

| | |
|---|---|
| 🏆 **Winner, Hack-N-Droid 2.0** | VIT Chennai, Mar 2026 · [spatialAuth](https://github.com/prayag-1771/spatialAuth/tree/feature/ml-backend): I built the ML authentication backend |
| 🥈 **Finalist, ET AI Hackathon 2026** | [Aegis AI](https://github.com/sudarsan2507-hue/Aegis): I owned the Fraud Shield module |
| 🌍 **Selected for Junction, Europe** | Hand-picked from a global applicant pool |
| 📄 **IEEE publication** | [Interface Trap Charges on Schottky TFET for High-Frequency Application](https://ieeexplore.ieee.org/document/11610552) |
| 🎓 **Research intern, NIT Trichy** | GradeRAG, failure-aware RAG · rated *Excellent* · paper under review |
| 📊 **Kaggle dataset, with DOI** | [ISIC 2019, leakage-free split](https://www.kaggle.com/datasets/sudarsan007r/isic-2019-preprocessed-leakage-free-split): 25,331 images, 0 lesions shared across splits |

## The idea behind my research

```mermaid
flowchart LR
    F["❌ Fail<br/><sub>bad retrieval, dead-end branch,<br/>insecure migration</sub>"] --> D["🔍 Diagnose<br/><sub>name <b>why</b> it failed</sub>"]
    D --> M["🧠 Remember<br/><sub>knowledge graph, memory, gate</sub>"]
    M --> I["✅ Improve<br/><sub>the same mistake is avoided,<br/>and measured</sub>"]
    I -. next question .-> F
    click F "https://github.com/sudarsan2507-hue/GLASS-ARMOR" "Glass Armor"
    click M "https://github.com/sudarsan2507-hue/GradeRAG" "GradeRAG"
    click D "https://github.com/sudarsan2507-hue/DemoSearch" "DemoSearch"
    style F fill:#3b0d1a,stroke:#fb7185,color:#fff
    style D fill:#1e1b4b,stroke:#a78bfa,color:#fff
    style M fill:#082f49,stroke:#22d3ee,color:#fff
    style I fill:#052e2b,stroke:#34d399,color:#fff
```

<img src="assets/results.svg" alt="Animated results: GradeRAG 58% to 87.5%, Glass Armor 0 to 10 repairs, DemoSearch 3.3x repairs" width="100%" />

<details>
<summary><b>🎓 GradeRAG</b>: RAG that remembers its wrong answers · NIT Trichy internship</summary>
<br/>

Standard RAG has no memory of its own errors, so it makes the same retrieval mistake on every similar
question. GradeRAG grades each answer, labels the failure (retrieval or reasoning), stores it in a
**Mistake Knowledge Graph**, and brings similar past mistakes back as warnings. Tested on HotpotQA and
TriviaQA with three LLMs: **+29.5 points** exact match for GPT-4o-mini on HotpotQA, and 5 of 6
model–dataset pairs improved. Qwen2.5-VL on TriviaQA got worse, and the local-model runs were small pilots.

<img src="assets/work/graderag.webp" width="80%" alt="GradeRAG results across models and datasets" />

[Repo](https://github.com/sudarsan2507-hue/GradeRAG) · [interactive mistake graph](https://sudarsan2507-hue.github.io/GradeRAG/mkg-explorer.html)
</details>

<details>
<summary><b>🔐 Glass Armor</b>: LLM-written post-quantum migrations pass the tests but fail security</summary>
<br/>

Teams are moving from RSA and elliptic curves to ML-KEM and ML-DSA, and much of that rewrite will be done
by LLMs and accepted once the tests pass. I built a benchmark of one-flaw variants that pass every test,
ran **400 migrations across 4 models**, and wrote a security gate (Semgrep rules, AST dataflow and live probes).
Tests caught **0 of 71** planted flaws. With the gate's feedback a model repaired **10 of 31** insecure outputs;
with test feedback, **0** (McNemar p = 0.002).

[Repo](https://github.com/sudarsan2507-hue/GLASS-ARMOR)
</details>

<details>
<summary><b>🧭 DemoSearch</b>: when does failure feedback actually help?</summary>
<br/>

A study across synthetic graphs, 295 hard Sudoku puzzles, MetaQA, WebQSP and LLM code repair, with hypotheses
written down before each run. A bare "dead end" changes nothing; a failure that comes with a reason does.
Telling a model *why* a test failed gives **2.5–3.3×** the repairs of a blind retry.

[Repo](https://github.com/sudarsan2507-hue/DemoSearch)
</details>

<details>
<summary><b>🧠 iAudit</b>: is brain-age bias in the model or the scanner?</summary>
<br/>

Two CNNs next to three tabular models on 560 IXI MRI scans, checked again on eNKI and SALD. One scanner site
is the worst for every model, CNN or tabular, so the bias comes from the acquisition, not the architecture.

[Repo](https://github.com/sudarsan2507-hue/iAudit)
</details>

## Guardrails for AI agents

I assume some prompt injections will get through, so I build the layer that stops them from doing damage.

| Project | What it does |
|---|---|
| **[Aegis AI](https://github.com/sudarsan2507-hue/Aegis)** · *ET AI finalist* | Joins scam calls, money-mule accounts and fake currency into one ranked case for police. 183 tests, 31 endpoints |
| **[SentinelMind](https://github.com/sudarsan2507-hue/Sentinel_Mind)** | A second AI that watches an agent live and flags invented tools, loops and goal drift |
| **[Choketap](https://github.com/sudarsan2507-hue/ChokeTap)** | A checkpoint every tool call must pass: policy, taint tracking and intent, so a landed injection can't exfiltrate |
| **[Engram](https://github.com/sudarsan2507-hue/Engram)** | Offline memory for edge agents that screens synced memories for poisoning (6/6 attacks stopped) |

<details>
<summary>📸 See SentinelMind running</summary>
<br/>
<img src="assets/work/sentinelmind.webp" width="80%" alt="SentinelMind live dashboard" />
</details>

## Sensing and things people use

| Project | What it does |
|---|---|
| **[HydroFuse](https://github.com/sudarsan2507-hue/HydroFuse)** | Finds underground pipe leaks by fusing ESP32 soil and vibration sensors with five satellite sources |
| **[WISP](https://github.com/sudarsan2507-hue/WISP)** | Fall detection from Wi-Fi signals with two ESP32 boards, aiming for under one false alarm a week |
| **[Safe-Signal](https://github.com/sudarsan2507-hue/Safe-Signal)** | On-device distress detection from a hand signal, voice and movement · [live](https://safe-signal-pi.vercel.app/) |
| **[DatePilot](https://github.com/sudarsan2507-hue/DatePilot)** | A constraint-checked date plan for two people · [live](https://datepilot.onrender.com) |

All 34 projects, with team credits, are in the **[portfolio](https://sudarsan2507-hue.github.io/Portfolio/#detailed)**.

## Tools

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white)
![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?style=flat-square&logo=tensorflow&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=flat-square&logo=scikitlearn&logoColor=white)
![Hugging Face](https://img.shields.io/badge/Hugging%20Face-FFD21E?style=flat-square&logo=huggingface&logoColor=black)
![FAISS](https://img.shields.io/badge/FAISS-4B8BBE?style=flat-square&logo=meta&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![React](https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB)
![Three.js](https://img.shields.io/badge/Three.js-000000?style=flat-square&logo=threedotjs&logoColor=white)
![Flutter](https://img.shields.io/badge/Flutter-02569B?style=flat-square&logo=flutter&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white)

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/sudarsan2507-hue/sudarsan2507-hue/output/snake-dark.svg">
  <img src="https://raw.githubusercontent.com/sudarsan2507-hue/sudarsan2507-hue/output/snake.svg" alt="Contribution snake">
</picture>

<div align="center">

**Open to ML / AI internships.** Let's build something that learns.

</div>
