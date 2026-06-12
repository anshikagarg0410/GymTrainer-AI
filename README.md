# GymTrainer-AI

> AI-powered workout tracking and coaching using real-time computer vision and LLMs
> https://gymtrainer-ai.streamlit.app/

## 📑 Table of Contents

- [Description](#description)
- [Key Features](#key-features)
- [Quick Start](#quick-start)
- [Key Dependencies](#key-dependencies)
- [Project Structure](#project-structure)
- [Development Setup](#development-setup)

## 📝 Description

GymTrainer-AI is an interactive fitness companion designed to guide users through their physical workouts while monitoring their form in real time. Built using Python and the Streamlit framework, the application solves the challenge of receiving immediate, actionable feedback on physical exercises without needing an in-person personal trainer. It provides a structured space for managing exercises and maintaining workout consistency.

## ✨ Key Features

- **🎥 Real-Time Video Processing** — Uses streamlit_webrtc and custom video processors to capture and analyze user exercise form directly through the browser.
- **🤖 AI Coaching and Speech** — Integrates Groq LLMs and a Text-to-Speech system to provide interactive coaching and vocal feedback.
- **💾 Local SQLite Database** — Saves user sessions, workout historical metrics, and configurations locally using a structured database.
- **🔐 Secure Session Management** — Protects access via a session-aware login wall and customizable UI style injection.

## ⚡ Quick Start

```bash

# 1. Clone the repository
git clone https://github.com/anshikagarg0410/GymTrainer-AI.git

# 2. Create & activate a virtualenv
python -m venv venv && source venv/bin/activate

# 3. Install dependencies
pip install -r requirements.txt
```

## 📦 Key Dependencies

```
streamlit: 1.54.0
streamlit-webrtc: 0.64.5
mediapipe: 0.10.14
opencv-python-headless: 4.10.0.84
pandas: 2.2.3
groq: 0.12.0
gtts: 2.5.3
python-dotenv: 1.2.2
```

## 📁 Project Structure

```
.
├── .streamlit
│   └── config.toml
├── core
│   ├── __init__.py
│   └── base_exercise.py
├── data.db
├── detectors
│   ├── __init__.py
│   ├── biceps_curl.py
│   ├── lunges.py
│   ├── pushup.py
│   ├── shoulder_press.py
│   └── squat.py
├── main.py
├── ml_models
│   ├── __init__.py
│   └── pose_landmarker_full.task
├── requirements.txt
├── services
│   ├── __init__.py
│   ├── auth
│   │   └── login_wall.py
│   ├── coaching
│   │   ├── llm.py
│   │   ├── tts.py
│   │   └── voice_pipeline.py
│   ├── config
│   │   └── workout_config.py
│   ├── persistence
│   │   └── exercise_repository.py
│   ├── state
│   │   ├── session_defaults.py
│   │   └── ui
│   │       └── style_loader.py
│   ├── tracking
│   │   └── metrics.py
│   └── vision
│       ├── __init__.py
│       └── exercise_video_processor.py
└── static
    ├── AdobeClean.otf
    └── style.css
```

## 🛠️ Development Setup

### Python
1. Install Python (v3.10+ recommended)
2. `python -m venv venv && source venv/bin/activate`  (Windows: `venv\Scripts\activate`)
3. `pip install -r requirements.txt`
