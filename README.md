# Sudarsan Ravichandran

[![](https://readme-typing-svg.demolab.com?font=JetBrains+Mono&size=20&duration=3500&pause=1200&color=A78BFA&vCenter=true&width=620&lines=failure-aware+retrieval;graph+search+for+multi-hop+QA;evaluation+that+reports+the+flat+results+too)](https://github.com/sudarsan2507-hue)

CSE (AI & ML) undergrad at VIT Chennai. Most of my work circles one question:
how do you stop a system from repeating a mistake it has already made?

That started as a retrieval problem and has since pulled me into graph search and
evaluation. Along the way I picked up audio ML, geospatial ML, and enough backend
work to deploy the things I build.

## Research

**GradeRAG**, failure-aware retrieval-augmented generation.
Built during an NLP research internship at NIT Trichy (May to June 2026). Standard
RAG has no memory of its own errors, so it makes the same retrieval mistake on
every similar question. GradeRAG grades each answer, stores the failure pattern in
a memory-knowledge graph, and consults that graph when retrieving for later
queries. Benchmarked against a standard RAG baseline on HotpotQA and TriviaQA
across three LLMs, measuring F1, exact match, and faithfulness.

![GradeRAG vs standard RAG, F1 across models and datasets](https://raw.githubusercontent.com/sudarsan2507-hue/sudarsan2507-hue/main/assets/graderag-results.svg)

<details>
<summary>Exact numbers</summary>

| Model | Dataset | Baseline F1 | GradeRAG F1 | Δ |
|---|---|---|---|---|
| Nemotron-Mini | HotpotQA | 0.72 | 0.86 | **+14.3** |
| Nemotron-Mini | TriviaQA | 0.66 | 0.79 | **+13.3** |
| GPT-4o-Mini | HotpotQA | 0.13 | 0.22 | **+9.0** |
| GPT-4o-Mini | TriviaQA | 0.12 | 0.17 | **+5.2** |
| Qwen2.5-VL | both | n/a | n/a | flat |

</details>

Two caveats worth stating up front: Qwen2.5-VL showed no measurable improvement,
and the local-model runs were on a small sample (n=15), so the Nemotron numbers
need a larger evaluation before I would lean on them.

`Python` `FAISS` `sentence-transformers` `Hugging Face` `bitsandbytes` `Neo4j`

**[DemoSearch](https://github.com/sudarsan2507-hue/DemoSearch)**, graph search for
multi-hop knowledge-graph QA. An earlier and rougher run at the same idea: when a
reasoning path fails, revive the paths that were wrongly rejected earlier instead
of restarting. Evaluated against a greedy baseline using paired t-tests and 95%
confidence intervals, with rule-based, embedding (BGE), and hybrid verifiers, plus
MCTS and beam-search variants.

**Publication.** P. Sharma, **Sudarsan Ravichandran**, V. V. Saxena, P. Kumar, and
R. Tiwari, "Investigation of Interface Trap Charges on Schottky TFET for High
Frequency Application." Accepted at VLSI SATA. A TCAD study of interface trap
charge effects on a 50 nm Double-Gate Schottky Tunnel FET, from earlier work
outside ML.

## Hackathons

**[spatialAuth](https://github.com/prayag-1771/spatialAuth)**, winner of
Hack-N-Droid 2.0 (SEQATO × VIT Chennai). Authentication that treats the room you
are standing in as the credential, built from acoustic reflections, WiFi patterns,
and magnetic distortions. I built the ML backend: a One-Class SVM over sensor
signatures served through a FastAPI enrollment and authentication API, later
refactored for multi-room support. Team of four; my work is on the
`feature/ml-backend` branch.

**Landroid**, AI land-intelligence platform (Birdscale × VIT Chennai). I built the
ML pipeline: NDVI vegetation analysis, ARIMA trend forecasting, raster validation,
and plant-zone detection, with tests covering it.

**Hawkeye**, real-time acoustic threat detection. I built the audio module: YAMNet
transfer learning over a live 16 kHz mic stream, filtered to dangerous AudioSet
classes, with confidence thresholding, an energy-based loudness check, and
automatic evidence capture, served via FastAPI.

**[SIH-137 / WeatherGuard](https://github.com/sudarsan2507-hue/SIH-137)**, Smart
India Hackathon 2025. Weather-safety dashboard that routes users toward safer
nearby locations. I owned the backend data models, the services layer, and the
Vite build and CI setup. Team of four.

## Building

**[Student-frndly](https://github.com/sudarsan2507-hue/Student-frndly)**, a skill
tracker that models decay over time. Express backend with JWT auth including
server-side revocation, bcrypt, Google OAuth, SQLite, and a Jest suite. This is
the project where I learned to make a backend secure rather than merely working.

**[yt-knowledge-assistant](https://github.com/sudarsan2507-hue/yt-knowledge-assistant)**,
RAG over YouTube transcripts for faster review. 384-dimensional embeddings and
manual cosine similarity, roughly one to two minutes for a ten-minute video.

**[Med-Smart](https://github.com/sudarsan2507-hue/Med-Smart)**, Flutter and
Firebase medication adherence app with an accessibility-focused UI for elderly
users.

## Tools

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white)
![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?style=for-the-badge&logo=tensorflow&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=for-the-badge&logo=scikitlearn&logoColor=white)
![Hugging Face](https://img.shields.io/badge/Hugging%20Face-FFD21E?style=for-the-badge&logo=huggingface&logoColor=black)

![FAISS](https://img.shields.io/badge/FAISS-4B8BBE?style=for-the-badge&logo=meta&logoColor=white)
![Neo4j](https://img.shields.io/badge/Neo4j-4581C3?style=for-the-badge&logo=neo4j&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white)
![Express](https://img.shields.io/badge/Express-000000?style=for-the-badge&logo=express&logoColor=white)

![Flutter](https://img.shields.io/badge/Flutter-02569B?style=for-the-badge&logo=flutter&logoColor=white)
![C++](https://img.shields.io/badge/C%2B%2B-00599C?style=for-the-badge&logo=cplusplus&logoColor=white)
![Java](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)
![SQLite](https://img.shields.io/badge/SQLite-003B57?style=for-the-badge&logo=sqlite&logoColor=white)
![Firebase](https://img.shields.io/badge/Firebase-FFCA28?style=for-the-badge&logo=firebase&logoColor=black)
![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white)

## Activity

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/sudarsan2507-hue/sudarsan2507-hue/output/snake-dark.svg">
  <img src="https://raw.githubusercontent.com/sudarsan2507-hue/sudarsan2507-hue/output/snake.svg">
</picture>

---

Currently going deeper into LLMs, retrieval systems, and the algorithmic side of ML.
Open to ML/AI internships.

[LinkedIn](https://www.linkedin.com/in/sudarsan-ravichandran-82b209391/) · sudarsan2507@gmail.com
