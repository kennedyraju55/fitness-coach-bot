# 🏋️ Fitness Coach Bot

![Python 3.11+](https://img.shields.io/badge/Python-3.11%2B-3776AB?style=flat-square&logo=python&logoColor=white) ![MIT License](https://img.shields.io/badge/License-MIT-22c55e?style=flat-square) ![Gemma 4](https://img.shields.io/badge/Gemma_4-Google-4285F4?style=flat-square&logo=google&logoColor=white) ![Privacy-First](https://img.shields.io/badge/Privacy--First-100%25_Local-8b5cf6?style=flat-square) ![Ollama](https://img.shields.io/badge/Ollama-Powered-000000?style=flat-square&logo=ollama&logoColor=white)

**AI-powered personal fitness coach that generates custom workout plans, tracks your progress, and provides exercise guidance — all running 100 % locally on your machine.**

---

## Architecture

```
┌──────────────────────────────────────────────────┐
│                 Fitness Coach Bot                 │
│                                                  │
│  ┌──────────┐  ┌──────────┐  ┌──────────────┐   │
│  │   CLI    │  │  Web UI  │  │  REST API    │   │
│  │  (Click) │  │(Streamlit)│  │  (FastAPI)   │   │
│  └────┬─────┘  └────┬─────┘  └──────┬───────┘   │
│       └──────────────┼───────────────┘           │
│              ┌───────┴───────┐                   │
│              │  Core Engine  │                   │
│              │ generate_plan │                   │
│              │ get_exercise  │                   │
│              └───────┬───────┘                   │
│              ┌───────┴───────┐                   │
│              │  Ollama LLM   │                   │
│              │   (Gemma 4)   │                   │
│              └───────────────┘                   │
│  ┌───────────────────────────────────────────┐   │
│  │  Storage: workout_log.json | progress.json│   │
│  └───────────────────────────────────────────┘   │
└──────────────────────────────────────────────────┘
```

---

## ✨ Key Features

- **Personalized Workout Plans** — generates multi-day programs tailored to your level, goal, equipment, and schedule
- **Six Fitness Goals** — weight loss, muscle gain, endurance, flexibility, strength, and general fitness
- **Three Difficulty Levels** — beginner, intermediate, and advanced with progressive overload guidance
- **Exercise Library** — built-in catalog with muscle groups, equipment type, and difficulty ratings
- **Detailed Exercise Guidance** — AI-generated form cues, common mistakes, and modifications
- **Workout Logging** — persistent JSON storage for exercises, sets, reps, and weight
- **Progress Tracking** — record body weight and body fat percentage over time with change summaries
- **Streamlit Web UI** — tabbed interface with plan generation, logging, progress charts, and library search
- **FastAPI REST API** — programmatic endpoints for workout plans and exercise details
- **100 % Local & Private** — no cloud calls, no API keys, no data leaves your machine

---

## 🚀 Quick Start

### Prerequisites

| Requirement | Version |
|-------------|---------|
| Python      | 3.11+   |
| Ollama      | latest  |
| Gemma 4 model | pulled via Ollama |

### Installation

```bash
git clone https://github.com/kennedyraju55/fitness-coach-bot.git
cd fitness-coach-bot
pip install -r requirements.txt
ollama pull gemma4
```

### Run

```bash
# CLI
python -m src.fitness_coach.cli --level beginner --goal weight-loss --equipment bodyweight

# Web UI
streamlit run src/fitness_coach/web_ui.py

# REST API
uvicorn src.fitness_coach.api:app --host 0.0.0.0 --port 8003

# Docker
docker compose up
```

---

## 🛠️ Tech Stack

| Component        | Technology             |
|------------------|------------------------|
| Language         | Python 3.11+           |
| LLM              | Gemma 4 via Ollama     |
| CLI Framework    | Click + Rich           |
| Web UI           | Streamlit              |
| REST API         | FastAPI + Uvicorn      |
| Data Storage     | JSON files             |
| Configuration    | YAML (config.yaml)     |
| Containerization | Docker + Docker Compose|
| Testing          | pytest                 |

---

## 📁 Project Structure

```
fitness-coach-bot/
├── src/fitness_coach/
│   ├── core.py        # Workout plan & exercise generation
│   ├── cli.py         # Click CLI with interactive REPL
│   ├── web_ui.py      # Streamlit web interface
│   ├── api.py         # FastAPI REST endpoints
│   ├── utils.py       # Logging, progress tracking, exercise library
│   └── config.py      # YAML config loader
├── common/            # Shared LLM client
├── tests/             # pytest test suite
├── config.yaml        # Default configuration
├── requirements.txt   # Python dependencies
├── Dockerfile         # Container build
└── docker-compose.yml # Multi-service orchestration
```

---

## 👤 Author

**Nrk Raju Guthikonda**

- GitHub: [kennedyraju55](https://github.com/kennedyraju55)
- Dev.to: [https://dev.to/kennedyraju55](https://dev.to/kennedyraju55)
- LinkedIn: [https://www.linkedin.com/in/nrk-raju-guthikonda-504066a8/](https://www.linkedin.com/in/nrk-raju-guthikonda-504066a8/)

---

## 📄 License

This project is licensed under the MIT License. See [LICENSE](LICENSE) for details.
