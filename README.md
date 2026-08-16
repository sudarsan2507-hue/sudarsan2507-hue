# Sudarsan Ravichandran

CSE (AI & ML) undergrad at VIT Chennai. Most of my work circles one question:
how do you stop a system from repeating a mistake it has already made?

That question started as a RAG problem and has since pulled me into retrieval,
graph search, and evaluation. Along the way I've picked up audio ML, geospatial
ML, and enough backend work to actually deploy the things I build.

---

## Research

**GradeRAG — failure-aware retrieval-augmented generation**
Built during an NLP research internship at NIT Trichy (May–June 2026).
A RAG system that stores its own failure patterns in a growing memory-knowledge
graph and consults them to retrieve better on later questions.

Benchmarked against standard RAG across three LLMs (GPT-4o-Mini, Nemotron-Mini,
Qwen2.5-VL) on HotpotQA and TriviaQA, measuring F1, exact match, and faithfulness.

| Model | Dataset | Baseline F1 | GradeRAG F1 | Δ |
|---|---|---|---|---|
| Nemotron-Mini | HotpotQA | 0.72 | 0.86 | **+14.3** |
| Nemotron-Mini | TriviaQA | 0.66 | 0.79 | **+13.3** |
| GPT-4o-Mini | HotpotQA | 0.13 | 0.22 | **+9.0** |
| GPT-4o-Mini | TriviaQA | 0.12 | 0.17 | **+5.2** |
| Qwen2.5-VL | both | — | — | flat |

Honest caveats: gains were consistent on most setups but Qwen showed no real
improvement, and the local-model runs were on a small sample (n=15).

`Python` `FAISS` `sentence-transformers` `Hugging Face` `bitsandbytes` `Neo4j`

**[DemoSearch](https://github.com/sudarsan2507-hue/DemoSearch)** — an earlier,
rougher take on the same idea. A graph-search algorithm for multi-hop
knowledge-graph QA that revives wrongly-rejected paths on failure. Evaluated
against a greedy baseline with 95% confidence intervals and paired t-tests,
with rule-based, embedding (BGE), and hybrid verifiers, plus MCTS and beam-search
variants.

**Publication** — P. Sharma, **S. Ravichandran**, V. V. Saxena, P. Kumar, and
R. Tiwari, "Investigation of Interface Trap Charges on Schottky TFET for High
Frequency Application." Accepted, VLSI SATA. TCAD study of interface trap charge
effects on a 50 nm Double-Gate Schottky Tunnel FET.

---

## Selected projects

**[spatialAuth](https://github.com/prayag-1771/spatialAuth)** — *Winner, Hack-N-Droid 2.0 (SEQATO × VIT Chennai)*
Authentication that uses the room you're in as the credential: acoustic
reflections, WiFi patterns, and magnetic distortions form a "room signature."
I built the ML backend — a One-Class SVM over sensor signatures served through a
FastAPI enrollment/authentication API, later refactored for multi-room support.
Teammates built the Android sensor-capture app. Team of 4; my work is on the
`feature/ml-backend` branch.

**Hawkeye** — real-time acoustic threat detection *(team)*
I built the audio module: YAMNet transfer learning over a live 16 kHz mic
stream, filtered to dangerous AudioSet classes (gunshot, scream, siren), with
confidence thresholding, an energy-based loudness check, and automatic evidence
capture, served via FastAPI.

**Landroid** — AI land-intelligence platform, Birdscale × VIT Chennai hackathon *(team)*
I built the ML pipeline: NDVI vegetation analysis, ARIMA trend forecasting,
raster validation, and plant-zone detection, with a test suite covering it.

**[Student-frndly](https://github.com/sudarsan2507-hue/Student-frndly)** — full-stack skill tracker
Models skill decay over time. Express backend with JWT auth including
server-side revocation, bcrypt, Google OAuth, SQLite, and a Jest suite. The
project where I learned to make a backend actually secure rather than just working.

**[yt-knowledge-assistant](https://github.com/sudarsan2507-hue/yt-knowledge-assistant)** — RAG over YouTube
Extracts and summarizes video content for faster review. 384-dim embeddings,
manual cosine similarity, roughly 1–2 minutes for a 10-minute video.

**[SIH-137 / WeatherGuard](https://github.com/sudarsan2507-hue/SIH-137)** — Smart India Hackathon 2025 *(team of 4)*
Weather-safety dashboard routing users toward safer nearby locations. I owned
the backend data models, the services layer, and the Vite build and CI setup.

**[Med-Smart](https://github.com/sudarsan2507-hue/Med-Smart)** — Flutter + Firebase medication
adherence app with an accessibility-focused UI for elderly users.

---

## Tools

Python (PyTorch, TensorFlow, scikit-learn, sentence-transformers, FAISS, FastAPI),
JavaScript/Node, Dart/Flutter, C++, Java. Comfortable with Git, REST APIs, and
SQLite/Firestore.

---

Currently going deeper into LLMs, retrieval systems, and the algorithmic side of ML.
Open to ML/AI internships.

[LinkedIn](https://www.linkedin.com/in/sudarsan-ravichandran-82b209391/) · sudarsan2507@gmail.com
