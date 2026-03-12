
# Symptom Checker AI

A quick hackathon demo app that turns a free-text symptom into a **triage recommendation** with a **severity color bar**.

## Features
- Single demo user profile (pregnant 25 y/o with asthma).
- Uses OpenAI **Responses API** with **Structured Outputs (JSON Schema)** for reliable UI rendering.
- Visual **green→red severity bar** with a marker positioned by the triage level.

## Setup

```bash
python -m venv .venv
source .venv/bin/activate   # Windows: .venv\Scripts\activate
pip install -r requirements.txt

# set your key (Mac/Linux)
export OPENAI_API_KEY="sk-..."
# Windows PowerShell:
# $env:OPENAI_API_KEY="sk-..."

# optional: choose a model
export OPENAI_MODEL="gpt-5"
```

https://github.com/user-attachments/assets/44f0b8b0-d7ab-446e-b8cf-0dc2bab1677b

## Run



```bash
streamlit run app.py
```

Open the local URL in your browser. If no API key is set, the app will still run using a simple mock ruleset.

## Notes
- uses healthcare databases
- For a real build, plug in a vetted medical content source and add stronger red-flag rules.
