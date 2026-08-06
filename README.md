# Billing Assistant MVP

A patient-facing billing and insurance chatbot prototype built with FastAPI and OpenAI. Helps patients understand medical bills, insurance terminology, and portal navigation.

## Background

This prototype demonstrates a retrieval-augmented generation (RAG) assistant designed to answer questions about medical bills, explain insurance concepts (deductible, copay, coinsurance), and guide users through a mock billing portal. All data shown is synthetic; no real patient data is used.

## Architecture

1. The FastAPI backend serves a mock billing portal with sample patient accounts.
2. User queries are processed through an intent classifier.
3. A RAG pipeline retrieves relevant billing and insurance definitions from a local knowledge base.
4. The LLM generates responses targeted at a 4th to 6th grade reading level based on mock data.
5. A PHI protection filter detects and blocks inputs containing account numbers, SSNs, or personal identifiers.

## Setup

```bash
git clone https://github.com/atharvasathaye/MVP-Chatbot.git
cd MVP-Chatbot
python -m venv .venv
.venv/Scripts/activate
pip install -r requirements.txt

# Add OpenAI API key
echo "OPENAI_API_KEY=sk-your-key-here" > .env

# Start application server
uvicorn main:app --reload --port 8000
```

Requires Python 3.11+ and an OpenAI API key.

## Tech Stack

- Python 3.11
- FastAPI
- OpenAI API (GPT-4o-mini, text-embedding-3-small)
- Jinja2
- Pydantic

## Collaborators

Team project: Nishit Mistry (PM), Atharva Sathaye, Akshay Wagh, Jasmitha Duvvuru, Juhi Khare.

## License

MIT

## Author

Atharva Sathaye

