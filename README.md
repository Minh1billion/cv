<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0f0f0f&height=200&section=header&text=Tran%20Quang%20Minh&fontSize=48&fontColor=ffffff&fontAlignY=38&desc=AI%20%2F%20ML%20Engineer%20%C2%B7%20Year%203%20%40%20HCMUTE&descAlignY=58&descColor=aaaaaa" />

</div>

---

## About Me

I'm a **third-year Software Engineering student** at Ho Chi Minh City University of Technology and Education (HCMUTE), focused on building production-grade AI systems - from LLM-integrated pipelines and RAG architectures to ML model serving and full-stack data tools.

- 🎓 B.Eng. Information Technology · **GPA 3.2 / 4.0** · Academic Score **7.85 / 10**
- 🤖 Focused on **LLM applications, RAG systems, NLP pipelines, and ML model serving**
- 🛠️ Currently building: AI-powered data analytics tools and RAG chatbots
- 📍 Ho Chi Minh City, Vietnam
- 📧 minh01212929979@gmail.com

---

## Featured Projects

### [DALreaDone](https://github.com/Minh1billion/dalreadone) - AI Data Analytics

> Upload CSV / Excel / JSON / Parquet -> automated statistical profiling + LLM-powered insights + interactive preprocessing pipeline.

**What it does:**
- **8-step EDA pipeline** (pure Python): schema profiling, missing values, univariate stats, datetime analysis, Pearson/Cramér's V correlations, distribution analysis, weighted data quality score - runs as background task with live progress polling
- **LLM review pass** (Groq LLaMA 3.3-70b): one structured JSON per EDA run - domain inference, severity-tagged issues, semantic type detection, column relationships, keep/drop recommendations
- **Strategy-based preprocessing pipeline**: composable fit/transform ops (drop, cast, imputation, outlier clipping, encoding, scaling, feature engineering) with AI Suggest that auto-generates a full pipeline from the EDA report
- **Live LLM cost tracking** via SSE - token counts, USD cost, latency per chain streamed in real time
- **Auth**: JWT access token in memory + httpOnly refresh cookie, OAuth2 (Google + GitHub); files on AWS S3, task state in Redis

![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![React](https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![Tailwind](https://img.shields.io/badge/Tailwind-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white)
![AWS S3](https://img.shields.io/badge/AWS%20S3-FF9900?style=flat-square&logo=amazons3&logoColor=white)
![Groq](https://img.shields.io/badge/Groq-F55036?style=flat-square&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)

---

### [Npixie](https://github.com/Minh1billion/npixie-master) - RAG Chatbot for a Fantasy Marketplace

> Lore-aware chatbot routing messages to 5 NPC personas with real asset-pack recommendations from a Supabase DB.

**What it does:**
- **RAG pipeline**: embed lore documents -> store in Qdrant -> retrieve top-k chunks -> generate via Groq LLaMA - contextually grounded, lore-accurate responses
- **5 NPC personas** (Nara, Zolt, Lyra, Vexis, Echo) - auto-detected by keyword routing, each defined as a YAML file for easy extensibility
- Live **asset-pack recommendations** fetched from Supabase (PostgreSQL) based on chat context

![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![Qdrant](https://img.shields.io/badge/Qdrant-DC244C?style=flat-square&logoColor=white)
![HuggingFace](https://img.shields.io/badge/HuggingFace-FFD21E?style=flat-square&logo=huggingface&logoColor=black)
![Groq](https://img.shields.io/badge/Groq-F55036?style=flat-square&logoColor=white)
![Supabase](https://img.shields.io/badge/Supabase-3ECF8E?style=flat-square&logo=supabase&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)

---

### [News Gathering Assistant](https://github.com/Minh1billion/news-gathering-assistant) - Vietnamese Tech News Intelligence

> End-to-end pipeline that crawls, embeds, clusters, and summarises Vietnamese tech news into a weekly intelligence report.

**What it does:**
- Crawls **4 sources** (VNExpress, ThanhNien, TuoiTre, ZingNews) via HTML scraping + RSS - **100+ articles per run** into PostgreSQL
- **Vietnamese SBERT embeddings** (`keepitreal/vietnamese-sbert`) + Qdrant vector store for semantic deduplication and relevance scoring
- **K-means clustering** with silhouette-score auto-tuning + TF-IDF / semantic keyword extraction -> structured weekly JSON report
- **React 18 dashboard**: executive summary, trending keywords, topic distribution, daily volume charts, PDF export

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![React](https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB)
![Qdrant](https://img.shields.io/badge/Qdrant-DC244C?style=flat-square&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=flat-square&logo=scikit-learn&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)

---

### [Pixelism](https://github.com/Minh1billion/pixelism) - Pixel Art Marketplace

> Full-stack marketplace for game developers with ML-powered upload validation.

**What it does:**
- **ML classifier** (FastAPI + PyTorch) validates every upload - only genuine pixel art accepted
- Spring Boot REST API: JWT auth, OAuth2 (Google & GitHub), refresh token rotation, OTP email via SMTP
- Real-time upload feedback via SSE; **Next.js 15** App Router frontend; **Cloudinary** CDN; deployed on AWS EC2

![Spring Boot](https://img.shields.io/badge/Spring%20Boot-6DB33F?style=flat-square&logo=springboot&logoColor=white)
![Java](https://img.shields.io/badge/Java-ED8B00?style=flat-square&logo=openjdk&logoColor=white)
![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=nextdotjs&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white)
![AWS EC2](https://img.shields.io/badge/AWS%20EC2-FF9900?style=flat-square&logo=amazonec2&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)

---

### [Specxel](https://github.com/Minh1billion/specxel) - Pixel Art Classifier

> Training pipeline and minimal UI for pixel art classification.

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white)
![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?style=flat-square&logo=opencv&logoColor=white)

---

## Tech Stack

### AI / ML
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=flat-square&logo=scikit-learn&logoColor=white)
![HuggingFace](https://img.shields.io/badge/HuggingFace-FFD21E?style=flat-square&logo=huggingface&logoColor=black)
![LangChain](https://img.shields.io/badge/LangChain-1C3C3C?style=flat-square&logo=langchain&logoColor=white)
![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?style=flat-square&logo=opencv&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=flat-square&logo=jupyter&logoColor=white)

### Backend
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring%20Boot-6DB33F?style=flat-square&logo=springboot&logoColor=white)
![Java](https://img.shields.io/badge/Java-ED8B00?style=flat-square&logo=openjdk&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white)
![Qdrant](https://img.shields.io/badge/Qdrant-DC244C?style=flat-square&logoColor=white)
![Supabase](https://img.shields.io/badge/Supabase-3ECF8E?style=flat-square&logo=supabase&logoColor=white)

### Frontend
![React](https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB)
![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=nextdotjs&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![Tailwind CSS](https://img.shields.io/badge/Tailwind-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white)
![Vite](https://img.shields.io/badge/Vite-646CFF?style=flat-square&logo=vite&logoColor=white)

### DevOps / Cloud
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Nginx](https://img.shields.io/badge/Nginx-009639?style=flat-square&logo=nginx&logoColor=white)
![AWS S3](https://img.shields.io/badge/AWS%20S3-FF9900?style=flat-square&logo=amazons3&logoColor=white)
![AWS EC2](https://img.shields.io/badge/AWS%20EC2-FF9900?style=flat-square&logo=amazonec2&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub%20Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white)

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

<div align="center">

[![Email](https://img.shields.io/badge/Email-minh01212929979%40gmail.com-333333?style=flat-square&logo=gmail&logoColor=white)](mailto:minh01212929979@gmail.com)
[![GitHub](https://img.shields.io/badge/GitHub-Minh1billion-333333?style=flat-square&logo=github&logoColor=white)](https://github.com/Minh1billion)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-minh--trần--quang-333333?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/minh-trần-quang-bb4433377/)
[![Location](https://img.shields.io/badge/Location-Ho%20Chi%20Minh%20City-333333?style=flat-square&logo=googlemaps&logoColor=white)]()

</div>

<div align="center">
<img src="https://capsule-render.vercel.app/api?type=waving&color=0f0f0f&height=100&section=footer" />
</div>