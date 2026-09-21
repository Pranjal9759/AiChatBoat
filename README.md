# AI Practical — From LLM Basics to a RAG Chatbot

A hands-on notebook that walks through building a real AI application step by step, using Python, LangChain, and Google Gemini.

## What's Inside

By the end of this notebook you will have built:

1. **A basic chatbot** — single LLM call, no memory
2. **A chatbot with memory** — conversation history resent on every turn
3. **A RAG system** — answers questions from a real document
4. **A full mini AI app** — memory + RAG combined into one assistant

## Stack

| Tool | Purpose |
|---|---|
| Python 3.11+ | Runtime |
| LangChain | AI orchestration framework |
| Google Gemini | The underlying LLM |
| `gemini-embedding-001` | Text embedding model for RAG |
| `InMemoryVectorStore` | Vector store (in-memory, no setup needed) |

## Project Structure

```
.
├── practical.ipynb   # Main notebook — run this
├── .env              # Your API key (never committed)
├── .gitignore        # Excludes .env from git
└── README.md
```

## Setup

### 1. Clone the repo

```bash
git clone <your-repo-url>
cd <repo-folder>
```

### 2. Get a Gemini API key

Go to [Google AI Studio](https://aistudio.google.com/apikey) and create a free API key.

### 3. Create a `.env` file

```
GEMINI_API_KEY=your_key_here
```

> The `.env` file is in `.gitignore` — it will never be committed.

### 4. Open the notebook in VS Code

- Install the **Python** and **Jupyter** extensions in VS Code
- Open `practical.ipynb`
- Select **Python 3.11+** as the kernel
- Run Cell 1 to install all dependencies, then `Shift+Enter` through each cell in order

## Notebook Sections

| Section | Topic |
|---|---|
| 2 | Configure Gemini via LangChain |
| 3 | LLM parameters — temperature, max tokens, model selection |
| 4 | Basic stateless chatbot |
| 5 | Conversation history and short-term memory |
| 6 | Introduction to RAG |
| 7 | Build a RAG pipeline (load → chunk → embed → retrieve → answer) |
| 8 | Final system combining memory + RAG |

## Key Concepts Covered

- **Frameworks** — what LangChain is and why it's useful
- **Temperature** — controlling randomness in LLM outputs
- **Statelessness** — why LLMs have no memory by default
- **Short-term memory** — resending conversation history on every call
- **Embeddings** — converting text into vectors that capture meaning
- **Vector search** — finding semantically similar chunks, not just keyword matches
- **RAG** — grounding LLM answers in your own documents
- **Hallucination prevention** — telling the model to say "I don't know" when the answer isn't in the document

## Requirements

All dependencies are installed automatically when you run Cell 1 of the notebook:

```
langchain-core
langchain-google-genai
langchain-text-splitters
google-generativeai
google-genai
python-dotenv
numpy
```
