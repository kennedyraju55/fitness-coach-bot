<div align="center">
<img src="https://img.shields.io/badge/💪_Fitness_Coach_Bot-Local_LLM_Powered-blue?style=for-the-badge&labelColor=1a1a2e&color=16213e" alt="Project Banner" width="600"/>

<br/>

<img src="https://img.shields.io/badge/Gemma_4-Ollama-orange?style=flat-square&logo=google&logoColor=white" alt="Gemma 4"/>
<img src="https://img.shields.io/badge/Python-3.9+-blue?style=flat-square&logo=python&logoColor=white" alt="Python"/>
<img src="https://img.shields.io/badge/Streamlit-Web_UI-red?style=flat-square&logo=streamlit&logoColor=white" alt="Streamlit"/>
<img src="https://img.shields.io/badge/Click-CLI-green?style=flat-square&logo=gnu-bash&logoColor=white" alt="Click CLI"/>
<img src="https://img.shields.io/badge/License-MIT-yellow?style=flat-square" alt="License"/>

<br/><br/>

<strong>Part of <a href="https://github.com/kennedyraju55/90-local-llm-projects">90 Local LLM Projects</a> collection</strong>

</div>

<br/>
# 💪 Fitness Coach Bot

![Python](https://img.shields.io/badge/Python-3.10%2B-blue?logo=python)
![LLM](https://img.shields.io/badge/LLM-Gemma%204-orange)
![License](https://img.shields.io/badge/License-MIT-green)
![UI](https://img.shields.io/badge/UI-Streamlit-red?logo=streamlit)

> AI-powered personal fitness trainer that creates customized workout plans using a local LLM.

## ✨ Features

- **3 Fitness Levels** — Beginner, intermediate, and advanced programs
- **6 Goal Types** — Weight loss, muscle gain, endurance, flexibility, strength, general fitness
- **Equipment Aware** — Plans tailored to your available equipment
- **Workout Logging** — Track exercises, sets, reps, and weights
- **Progress Tracking** — Record body weight and body fat with charts
- **Exercise Library** — Built-in library with muscle groups and difficulty
- **Streamlit Web UI** — Interactive browser-based interface with tabs for plans, logging, and progress
- **Rich CLI Interface** — Beautiful formatted terminal output
- **Safety First** — Includes warm-ups, cool-downs, and injury prevention tips
- **Configurable** — YAML-based settings

## 📦 Installation

```bash
pip install -r requirements.txt
pip install -e .
```

## 🚀 Usage

### CLI

```bash
# Basic usage
python -m fitness_coach.cli --level beginner --goal "weight-loss" --equipment "dumbbells,mat"

# Advanced with custom schedule
python -m fitness_coach.cli --level advanced --goal "muscle-gain" --equipment "barbell,rack" --days 5 --duration 60
```

### Web UI (Streamlit)

```bash
streamlit run src/fitness_coach/web_ui.py
```

### CLI Commands

| Command       | Action                        |
|---------------|-------------------------------|
| `<exercise>`  | Get exercise form details     |
| `log`         | Log a workout                 |
| `progress`    | View progress summary         |
| `library`     | Browse exercise library       |
| `quit`        | Exit the session              |


## 🧪 Running Tests

```bash
pytest tests/ -v
```

## ⚙️ Configuration

Edit `config.yaml` to customize model, workout defaults, and storage paths.

## 📸 Screenshots

<div align="center">
<table>
<tr>
<td><img src="https://via.placeholder.com/400x250/1a1a2e/e94560?text=CLI+Interface" alt="CLI Interface"/></td>
<td><img src="https://via.placeholder.com/400x250/16213e/e94560?text=Web+UI" alt="Web UI"/></td>
</tr>
<tr>
<td align="center"><em>CLI Interface</em></td>
<td align="center"><em>Streamlit Web UI</em></td>
</tr>
</table>
</div>

## 📁 Project Structure

```
04-fitness-coach-bot/
├── src/
│   └── fitness_coach/
│       ├── __init__.py      # Package metadata
│       ├── core.py          # Core business logic
│       ├── cli.py           # Click CLI interface
│       ├── web_ui.py        # Streamlit web interface
│       ├── config.py        # Configuration management
│       └── utils.py         # Workout logging, progress, exercise library
├── tests/
│   ├── __init__.py
│   ├── test_core.py         # Core logic tests
│   └── test_cli.py          # CLI tests
├── config.yaml              # Default configuration
├── setup.py                 # Package setup
├── requirements.txt         # Dependencies
├── Makefile                 # Common commands
├── .env.example             # Example environment variables
└── README.md                # This file
```
