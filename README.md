<h1 align="center">Hi, I'm Alae Bajoudi 👋</h1>
<h3 align="center">M2 AI & Connected Objects student · Machine Learning · Computer Vision</h3>

<p align="center">
  <a href="https://www.linkedin.com/in/alae-bajoudi-a5a199281"><img src="https://img.shields.io/badge/LinkedIn-Alae%20Bajoudi-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"/></a>
  <a href="mailto:alaebajoudi128@gmail.com"><img src="https://img.shields.io/badge/Email-alaebajoudi128%40gmail.com-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Email"/></a>
  <img src="https://img.shields.io/badge/Open%20to-Internship%20·%202027-2EA44F?style=for-the-badge" alt="Open to internship"/>
</p>

---

## 👨‍💻 About me

I'm a Master's student in **Artificial Intelligence and Connected Objects** at Ibn Tofail University (Kénitra). My path started in **embedded electronics** and moved into **AI**. That gives me a mix that is useful for real-world AI systems: I understand the hardware, and I build models that go from raw data all the way to a deployed app.

- 🔭 Currently: M2 in AI & Connected Objects
- 🌱 Focus: deep learning, computer vision, generative AI, LLM apps and RAG
- 🛠️ I like projects that ship: clean data pipelines, honest evaluation, and a usable interface on top
- ⚡ Vibe coding is fun when you can troubleshoot: I build fast with AI coding tools, then read the code, debug what breaks and check the results with tests and evals
- 🏭 Industry experience: embedded electronics internship at **Nexteer Automotive** (automotive steering systems)
- 📍 Based in Kénitra, Morocco · 🗣️ French (fluent) · English (fluent) · Arabic (native)

---

## 🚀 Featured projects

### 📜 [Teyvat Lorekeeper](https://github.com/kayzo001/teyvat-lorekeeper)

A local RAG assistant for Genshin Impact lore: ask about the Archons, characters and history of Teyvat and get an answer with citations to the wiki sections it came from. Runs fully offline and free.

- **Data:** 3,520 lore pages pulled from the Fandom wiki through the MediaWiki API, cleaned with mwparserfromhell into 21,958 section chunks
- **Retrieval:** hybrid search, BM25 + dense embeddings (bge-small in ChromaDB) fused with reciprocal rank fusion, plus an optional cross-encoder reranker. **Recall@5 0.97** on a 43-question eval
- **Generation:** a local LLM through Ollama that cites every claim as `[n]` and refuses when the wiki doesn't cover the question. **qwen3.5:4b** beat **llama3.2:3b** on correct answers (82% vs 55%) and correct citations (89% vs 37%)
- **Debugging:** traced a hallucination ("who is the Cryo Archon?") to a gap in the data rather than the prompt, and fixed it at the data layer
- **App:** FastAPI streaming API and web UI, a CLI, Docker Compose with Ollama, 65 tests and CI

`Python` `Ollama` `FastAPI` `ChromaDB` `sentence-transformers` `BM25` `Docker` `pytest`

### 🧊 [SpatialForge](https://github.com/kayzo001/spatialforge)

Turns 20 to 150 ordinary photos into an interactive 3D scene you can explore in the browser.

- Camera poses and sparse geometry from real Structure-from-Motion (COLMAP), then point-cloud refinement with Open3D
- Optional 3D Gaussian Splatting training (Nerfstudio Splatfacto, on GPU or Colab), evaluated with PSNR, SSIM and LPIPS
- FastAPI backend with a job queue and live progress over SSE, and a React + TypeScript + three.js viewer; the geometric pipeline runs on a laptop CPU

`Python` `COLMAP` `Open3D` `Gaussian Splatting` `FastAPI` `React` `three.js`

### 🎮 [League of Legends Esports Win Predictor](https://github.com/kayzo001/league-of-legends-e-sports-game-predictor)

Predicts the winner of a **professional** League of Legends match using only the game state at **15 minutes**.

- **Data:** 2024 pro matches from Oracle's Elixir, about 12k raw rows narrowed to 1,672 team-games with complete 15-minute stats
- **Features:** gold and XP differences, turret plates, first objectives, side, and a **draft advantage score** computed on training data only to avoid leakage
- **Modeling:** benchmarked 5 models (Logistic Regression, Random Forest, XGBoost, AdaBoost, Gradient Boosting), then tuned them and built **voting** and **stacking** ensembles
- **Result:** **~78% test accuracy**, consistent under 5-fold cross-validation
- **Deployment:** a **Flask** web app where you enter a game state and get a win probability

`Python` `scikit-learn` `XGBoost` `pandas` `Flask` `matplotlib` `seaborn`

### 📨 [X Outreach Manager](https://github.com/kayzo001/X-outreach-manager)

A full-stack, consent-aware campaign manager for X (Twitter), built on the official API.

- CSV/XLSX import with deduplication, lead scoring, campaign scheduling with caps, dry-run mode and an emergency stop
- Background job worker (BullMQ), encrypted tokens (AES-256-GCM), rate limiting
- **95 automated tests** run against a real PostgreSQL database

`TypeScript` `Next.js` `PostgreSQL` `Prisma` `Redis` `Docker` `Vitest`

---

## 🧰 Tech stack

**AI / ML**

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white)
![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?style=flat-square&logo=tensorflow&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=flat-square&logo=scikitlearn&logoColor=white)
![XGBoost](https://img.shields.io/badge/XGBoost-189FDD?style=flat-square)
![pandas](https://img.shields.io/badge/pandas-150458?style=flat-square&logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=flat-square&logo=numpy&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=flat-square&logo=jupyter&logoColor=white)

**LLMs & RAG**

![Ollama](https://img.shields.io/badge/Ollama-000000?style=flat-square&logo=ollama&logoColor=white)
![Hugging Face](https://img.shields.io/badge/Hugging%20Face-FFD21E?style=flat-square&logo=huggingface&logoColor=black)
![ChromaDB](https://img.shields.io/badge/ChromaDB-FF6446?style=flat-square)
![RAG](https://img.shields.io/badge/RAG-hybrid%20search-6E40C9?style=flat-square)

**Apps & deployment**

![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![Flask](https://img.shields.io/badge/Flask-000000?style=flat-square&logo=flask&logoColor=white)
![React](https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB)
![three.js](https://img.shields.io/badge/three.js-000000?style=flat-square&logo=threedotjs&logoColor=white)
![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?style=flat-square&logo=streamlit&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=nextdotjs&logoColor=white)

**Data & tools**

![SQL](https://img.shields.io/badge/SQL-4479A1?style=flat-square&logo=postgresql&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white)

**Embedded / IoT**

![Embedded Systems](https://img.shields.io/badge/Embedded%20Systems-555555?style=flat-square)
![IoT](https://img.shields.io/badge/IoT-555555?style=flat-square)

---

## 🎓 Education

| Years | Degree | School |
| --- | --- | --- |
| 2025 – 2027 | **Master's**, Artificial Intelligence and Connected Objects | Ibn Tofail University, Kénitra |
| 2024 – 2025 | **Licence d'Excellence** (Bachelor's), Artificial Intelligence | Ibn Tofail University, Kénitra |
| 2021 – 2024 | **DUT**, Embedded Electronic Systems | Ibn Tofail University, Kénitra |

---

## 📊 GitHub stats

<p align="center">
  <img height="165" src="https://github-readme-stats.vercel.app/api?username=kayzo001&show_icons=true&hide_border=true&count_private=true" alt="GitHub stats"/>
  <img height="165" src="https://github-readme-stats.vercel.app/api/top-langs/?username=kayzo001&layout=compact&hide_border=true" alt="Top languages"/>
</p>

---

<p align="center">
  <b>Recruiting for an AI / ML internship in France in 2027?</b><br/>
  I'd be glad to talk: <a href="mailto:alaebajoudi128@gmail.com">alaebajoudi128@gmail.com</a> · <a href="https://www.linkedin.com/in/alae-bajoudi-a5a199281">LinkedIn</a>
</p>
