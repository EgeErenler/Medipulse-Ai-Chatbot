# MediPulse AI

An AI health assistant for people in the UK. You describe your symptoms in plain language, and Florence, the assistant, gives NHS-style guidance and points you to the right service: 999, NHS 111, your GP or a pharmacist.

**Live app:** [medipulse-ai.streamlit.app](https://medipulse-ai.streamlit.app)

This repository holds the live version of the app.

## What it does

- Chat-based triage in warm, plain UK English
- Safety rules on every reply: emergencies go to 999, urgent cases to NHS 111, mental health crises to Samaritans (116 123)
- Never diagnoses or prescribes; always signposts to NHS services
- Collects a short profile (name, age, gender, existing conditions) one question at a time to make answers more relevant
- Demo mode with offline answers for key topics when no API key is connected, and the same offline answers if the AI service is down

## Built with

- Python
- Streamlit
- Groq API with open models (`openai/gpt-oss-120b` by default). If a model is retired, the app falls back to the next one automatically. Set `GROQ_MODEL` to choose your own.

## Run it locally

```bash
pip install -r requirements.txt
streamlit run app.py
```

Add your Groq API key in one of these ways:

- a `.env` file with `GROQ_API_KEY=your_key`
- Streamlit secrets (`GROQ_API_KEY`)
- the sidebar field when the app opens

You can get a free key at [console.groq.com](https://console.groq.com).

## Disclaimer

MediPulse AI is a portfolio project. It does not give medical advice and does not replace a doctor. In an emergency, call 999.

## Author

Built by **Ege Erenler**, software engineer and data scientist in London.
Portfolio: [egeerenler.com](https://egeerenler.com) · GitHub: [@EgeErenler](https://github.com/EgeErenler)
