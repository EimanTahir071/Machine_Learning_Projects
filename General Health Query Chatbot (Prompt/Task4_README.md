```markdown
# Task 4 — General Health Query Chatbot (Prompt Engineering)

## Objective
Create a chatbot that answers general health-related questions using a Large Language Model (LLM). Emphasize prompt engineering for helpful, empathetic responses and include safety filters to avoid harmful medical advice.

## Tools / Backends
- Primary: OpenAI Chat API (gpt-3.5 family) — requires OPENAI_API_KEY.
- Fallback: Hugging Face Inference API (optional) — requires HF_API_TOKEN.
- Notebook demonstrates both programmatic calls and an interactive loop.

## Notebook
- Filename: Task4_Health_Chatbot_notebook.py (Jupyter-style .py) or .ipynb

## Environment / Requirements
- Python 3.8+
- Key packages:
  - openai (for OpenAI backend)
  - requests (for HF inference)
  - regex, standard Python libs

Install:
pip install openai requests

## What this notebook does (step-by-step)
1. Defines a safety filter (rule-based) to detect dangerous queries (diagnosis, dosing, self-harm, emergencies).
2. Implements prompt engineering:
   - System prompt instructing the assistant to be friendly, non-diagnostic, and to include a disclaimer.
   - Few-shot examples to guide tone and content.
3. Provides functions:
   - chat_with_openai(messages): call to OpenAI ChatCompletion.
   - chat_with_hf(prompt): fallback via Hugging Face inference.
   - is_dangerous_query(text): checks for dangerous patterns.
   - run_chatbot(): interactive Jupyter CLI loop.
   - answer_query(query, backend="openai"): programmatic single-query function.
4. Includes example queries and explains how to run the interactive loop.

## How to run
1. Set environment variables:
   - For OpenAI: export OPENAI_API_KEY="sk-..."
   - For Hugging Face (fallback): export HF_API_TOKEN="hf_..."
2. Run notebook in a terminal-enabled environment:
   jupyter notebook Task4_Health_Chatbot_notebook.py
3. Start interactive loop:
   - In the notebook, call `run_chatbot()` (or run using `if __name__...` flow).
4. Ask questions like "What causes a sore throat?" or "Is paracetamol safe for children?"

## Safety & Limitations
- The assistant is for informational purposes only.
- The notebook enforces a rule-based safety filter to refuse diagnosis, prescription, dosing, or emergency instructions.
- Always include the disclaimer: "I am not a doctor. For medical diagnosis or treatment, please consult a healthcare professional."

## Tips & Extensions
- Add more advanced safety checks and a triage flow (direct to emergency services if explicit emergency).
- Use a moderation API for extra safety filtering.
- Build a lightweight web UI with Streamlit for an accessible interface.

## Submission Checklist
- Notebook with prompt design explanation and safety logic.
- README (this file).
- Note about required API keys and environment variables.
- GitHub repo link when submitting.
```