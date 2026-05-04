# Tran Quang Minh

**AI / ML Engineer · Year 3 @ HCMUTE**

Third-year Software Engineering student at Ho Chi Minh City University of Technology and Education, building production-grade AI systems - LLM pipelines, RAG architectures, ML model serving, and full-stack data tools.

- 🎓 B.Eng. Information Technology · GPA 3.2 / 4.0 · Academic Score 7.85 / 10
- 🤖 LLM applications · RAG systems · NLP pipelines · ML model serving
- 🛠️ Currently building: AI-powered data analytics tools and RAG chatbots
- 📍 Ho Chi Minh City, Vietnam
- 📧 minh01212929979@gmail.com

---

## Projects

### [DALreaDone](https://github.com/Minh1billion/dalreadone) - AI Data Analytics Platform

Upload CSV / Excel / JSON / Parquet -> automated statistical profiling + LLM-powered insights + interactive preprocessing pipeline.

- **8-step EDA pipeline** (pure Python): schema profiling, missing values, univariate stats, datetime analysis, Pearson/Cramér's V correlations, distribution analysis, weighted data quality score - runs as background task with live progress polling
- **LLM review pass** (Groq LLaMA 3.3-70b): one structured JSON per EDA run - domain inference, severity-tagged issues, semantic type detection, column relationships, keep/drop recommendations
- **Strategy-based preprocessing pipeline**: composable fit/transform ops (drop, cast, imputation, outlier clipping, encoding, scaling, feature engineering) with AI Suggest that auto-generates a full pipeline from the EDA report
- **Live LLM cost tracking** via SSE - token counts, USD cost, latency per chain streamed in real time
- **Auth**: JWT access token in memory + httpOnly refresh cookie, OAuth2 (Google + GitHub); files on AWS S3, task state in Redis

`FastAPI` `React` `TypeScript` `Tailwind` `PostgreSQL` `Redis` `AWS S3` `Groq` `Docker`

---

### [Minesweeper Hybrid RL Agent](https://github.com/Minh1billion/minesweeper-hybrid-RL-agent) - 40% Win Rate Solver
 
Hybrid AI agent combining **constraint reasoning + Q-learning**, achieving ~**40% all-time win rate** (~55% rolling) on a 10×10 board with 15 mines after 50,000 training episodes.
 
- **4-layer decision hierarchy**: constraint solver -> probability filter -> Q-policy -> random fallback - each layer only activates when the previous cannot produce a certain decision
- **Constraint solver** handles ~87% of all moves deterministically: flags cells where hidden neighbor count equals remaining mine count, reveals cells where mine count is fully satisfied
- **Probability filter** estimates `P(mine | cell)` from surrounding number cells, acting when confidence exceeds 80% (flag) or drops below 20% (reveal) - covers ~7% of decisions
- **Q-table** encodes local board state as a 5×5 observation window (25-element tuple), learns `reveal` vs `flag` values via Bellman update - intervenes in ~5% of genuinely ambiguous cases
- **1.83M Q-states** learned over 1.17M training steps; tabular approach made feasible by frontier-only evaluation and local state representation
- **Custom environment + training loop** (no Gym), real-time pygame debug UI with Q-value inspection, decision source tracking, and win rate charting

`Python` `NumPy` `Pygame`

---

### [News Gathering Assistant](https://github.com/Minh1billion/news-gathering-assistant) - Vietnamese Tech News Intelligence

End-to-end pipeline that crawls, embeds, clusters, and summarises Vietnamese tech news into a weekly intelligence report.

- Crawls **11 sources** (VNExpress, ThanhNien, TuoiTre, ZingNews, CafeBiz, VietnamNet, DanTri, Soha, VietnamPlus, Tinhte, TraiNghiemSo) via HTML scraping + RSS — **200–300 articles per run** into PostgreSQL
- **Vietnamese SBERT embeddings** (`keepitreal/vietnamese-sbert`) + Qdrant vector store for semantic deduplication and relevance scoring
- **K-means clustering** with silhouette-score auto-tuning + TF-IDF / semantic keyword extraction -> structured weekly JSON report
- **React 18 dashboard**: executive summary, trending keywords, topic distribution, daily volume charts, PDF export

`Python` `FastAPI` `React` `Qdrant` `PostgreSQL` `scikit-learn` `Docker`

---

### [DataPill](https://github.com/Minh1billion/datapill) - Modular Data Pipeline CLI

End-to-end CLI for reproducible data pipelines: **ingest -> profile -> classify -> preprocess -> export**, with artifact tracking per run.

- Multi-source ingestion: local files, PostgreSQL, MySQL, S3, Kafka, REST APIs (stream + batch)
- Dataset profiling: missing values, distributions, percentiles, skew/kurtosis, correlations (Pearson/Spearman), pattern detection (email, URL, UUID, datetime)
- Semantic column classification: rule-based + embedding-based hybrid (sentence-transformers) with confidence-based routing
- Config-driven preprocessing pipeline: JSON steps (imputation, scaling, encoding, outlier clipping, feature engineering) with dry-run + checkpoint support
- Artifact system: every run produces versioned Parquet + JSON metadata, tracked via run_id
- Sandbox execution: custom Python transformations via RestrictedPython or Docker isolation
- CLI interface: Typer-based `dp` command with async execution + progress streaming

`Python` `Polars` `PyArrow` `Typer` `Docker`

**PyPI:** https://pypi.org/project/datapill \
**Docs:** https://minh1billion.github.io/datapill

---

### [Npixie](https://github.com/Minh1billion/npixie-master) - RAG Chatbot for a Fantasy Marketplace

Lore-aware chatbot routing messages to 5 NPC personas with real asset-pack recommendations from a Supabase DB.

- **RAG pipeline**: embed lore documents -> store in Qdrant -> retrieve top-k chunks -> generate via Groq LLaMA - contextually grounded, lore-accurate responses
- **5 NPC personas** (Nara, Zolt, Lyra, Vexis, Echo) - auto-detected by keyword routing, each defined as a YAML file for easy extensibility
- Live **asset-pack recommendations** fetched from Supabase (PostgreSQL) based on chat context

`FastAPI` `Qdrant` `HuggingFace` `Groq` `Supabase` `Docker`

---

### [Pixelism](https://github.com/Minh1billion/pixelism) - Pixel Art Marketplace

Full-stack marketplace for game developers with ML-powered upload validation.

- **ML classifier** (FastAPI + PyTorch) validates every upload - only genuine pixel art accepted
- Spring Boot REST API: JWT auth, OAuth2 (Google & GitHub), refresh token rotation, OTP email via SMTP
- Real-time upload feedback via SSE; **Next.js 15** App Router frontend; **Cloudinary** CDN; deployed on AWS EC2

`Spring Boot` `Java` `Next.js` `PyTorch` `PostgreSQL` `Redis` `AWS EC2` `Docker`

---

### [Specxel](https://github.com/Minh1billion/specxel) - Pixel Art Classifier

Training pipeline and minimal inference UI for pixel art classification.

`Python` `PyTorch` `OpenCV`

---

## Tech Stack

**Languages**

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![Java](https://img.shields.io/badge/Java-ED8B00?style=flat-square&logo=openjdk&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)

**Frameworks & Libraries**

![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=flat-square&logo=scikit-learn&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat-square&logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=flat-square&logo=numpy&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring%20Boot-6DB33F?style=flat-square&logo=springboot&logoColor=white)
![React](https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB)

**Infrastructure**

![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white)
![Qdrant](https://img.shields.io/badge/Qdrant-DC244C?style=flat-square&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![AWS S3](https://img.shields.io/badge/AWS%20S3-FF9900?style=flat-square&logo=amazons3&logoColor=white)
![AWS EC2](https://img.shields.io/badge/AWS%20EC2-FF9900?style=flat-square&logo=amazonec2&logoColor=white)

**Tools**

![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub%20Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white)
![Docker Compose](https://img.shields.io/badge/Docker%20Compose-2496ED?style=flat-square&logo=docker&logoColor=white)

*Additional exposure:*
![HuggingFace](https://img.shields.io/badge/HuggingFace-FFD21E?style=flat-square&logo=huggingface&logoColor=black)
![LangChain](https://img.shields.io/badge/LangChain-1C3C3C?style=flat-square&logo=langchain&logoColor=white)
![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?style=flat-square&logo=opencv&logoColor=white)
![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=nextdotjs&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![Tailwind CSS](https://img.shields.io/badge/Tailwind-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white)
![Vite](https://img.shields.io/badge/Vite-646CFF?style=flat-square&logo=vite&logoColor=white)
![Nginx](https://img.shields.io/badge/Nginx-009639?style=flat-square&logo=nginx&logoColor=white)
![Supabase](https://img.shields.io/badge/Supabase-3ECF8E?style=flat-square&logo=supabase&logoColor=white)

---

## GitHub Stats

<div align="center">
  <img height="160" src="https://github-readme-stats-xi-vert-eomzcenz0g.vercel.app/api?username=Minh1billion&show_icons=true&theme=dark&hide_border=true&count_private=true&include_all_commits=true&bg_color=0f0f0f&title_color=ffffff&text_color=aaaaaa&icon_color=ffffff" />
  &nbsp;
  <img height="160" src="https://github-readme-stats-xi-vert-eomzcenz0g.vercel.app/api/top-langs/?username=Minh1billion&layout=compact&theme=dark&hide_border=true&langs_count=8&bg_color=0f0f0f&title_color=ffffff&text_color=aaaaaa" />
</div>

<div align="center">
  <img src="https://streak-stats.demolab.com/?user=Minh1billion&theme=dark&hide_border=true&background=0f0f0f&ring=ffffff&fire=ffffff&currStreakLabel=aaaaaa&sideLabels=aaaaaa&dates=555555" />
</div>

---

## Connect

[minh01212929979@gmail.com](mailto:minh01212929979@gmail.com) · [GitHub](https://github.com/Minh1billion) · [LinkedIn](https://www.linkedin.com/in/minh-trần-quang-bb4433377/) · Ho Chi Minh City, Vietnam
