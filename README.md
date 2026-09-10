<div align="center">

# 🚀 Nexus FM Platform

### End-to-End Foundation Model Training Infrastructure

**Train · Fine-tune · Evaluate · Deploy · Monitor — All in One Platform**

[![Python](https://img.shields.io/badge/Python-3.10+-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://python.org)
[![FastAPI](https://img.shields.io/badge/FastAPI-0.109-009688?style=for-the-badge&logo=fastapi&logoColor=white)](https://fastapi.tiangolo.com)
[![React](https://img.shields.io/badge/React-18-61DAFB?style=for-the-badge&logo=react&logoColor=black)](https://react.dev)
[![Vite](https://img.shields.io/badge/Vite-5-646CFF?style=for-the-badge&logo=vite&logoColor=white)](https://vitejs.dev)
[![TailwindCSS](https://img.shields.io/badge/Tailwind-3-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white)](https://tailwindcss.com)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=for-the-badge)](LICENSE)

[Features](#-features) • [Architecture](#-architecture) • [Tech Stack](#-tech-stack) • [Setup](#-quick-start) • [API](#-api-endpoints) • [Roadmap](#-roadmap)

</div>

---

## 📖 Overview

**Nexus FM Platform** is a full-stack MLOps platform that demonstrates the complete lifecycle of foundation models — from distributed training and PEFT-based fine-tuning to production inference, evaluation, and GPU cluster orchestration.

Built as a **flagship project** to showcase end-to-end AI infrastructure engineering with a beautiful, production-grade React UI and a robust FastAPI backend.

> ⚡ **Note:** This project is designed for **learning and demonstration**. Real GPU training is **simulated**, while actual LLM inference is powered by the **Google Gemini API**.

---

## ✨ Features

<table>
<tr>
<td width="50%">

### 🧠 Distributed Training
- DDP / FSDP / Pipeline Parallel **simulation**
- Multi-node config editor
- Real-time loss & throughput curves
- Gradient accumulation controls

### 🎛️ LoRA / QLoRA Fine-Tuning
- Configurable rank, alpha, dropout
- Target module selection
- Adapter versioning & registry
- QLoRA 4-bit quantization config

### ⚡ Mixed Precision
- FP32 / FP16 / BF16 toggles
- Gradient scaler settings
- Memory footprint estimator

</td>
<td width="50%">

### 📦 Model Registry
- Versioned model cards
- Metadata (params, size, family)
- Tags, search & filters
- Lineage tracking

### 🔌 Inference APIs
- **Gemini-powered** text generation
- Chat + completion endpoints
- Temperature / top_p / max_tokens controls
- Streaming responses

### 📊 Evaluation Dashboard
- Benchmark runs (MMLU, HellaSwag mock)
- Radar & comparison charts
- Leaderboard view
- Side-by-side metrics

### 🖥️ GPU Cluster Management
- Live node grid (simulated)
- Utilization, memory, temp
- WebSocket real-time updates
- Cluster topology view

</td>
</tr>
</table>

---

## 🏗️ Architecture



---

## 🧰 Tech Stack

| Layer | Technology |
|-------|-----------|
| **Frontend** | React 18, Vite, TailwindCSS, Recharts, Framer Motion, Zustand, Axios |
| **Backend** | Python 3.10+, FastAPI, SQLAlchemy, Pydantic, Alembic, JWT |
| **Database** | SQLite (dev) / PostgreSQL (optional) |
| **AI/LLM** | Google Gemini API |
| **Real-time** | WebSockets |
| **DevOps** | Docker, Docker Compose |

---

## 📂 Project Structure



---

## 🚀 Quick Start

### Prerequisites
- Python 3.10+
- Node.js 18+
- Gemini API Key ([Get free](https://aistudio.google.com/app/apikey))

### 1. Clone
```bash
git clone https://github.com/vishakha2121/nexus-fm-platform.git
cd nexus-fm-platform


cd backend
python -m venv venv
source venv/bin/activate      # Windows: venv\Scripts\activate
pip install -r requirements.txt

cp .env.example .env
# Add your GEMINI_API_KEY in .env

python db/init_db.py
python db/seed_data.py
uvicorn main:app --reload --port 8000


cd frontend
npm install
npm run dev