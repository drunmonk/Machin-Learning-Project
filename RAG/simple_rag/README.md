# RAG Pipeline — From Scratch


A minimal but complete Retrieval-Augmented Generation (RAG) pipeline built from first principles. No LangChain, no LlamaIndex — just the core components wired together directly.


## What It Does


Takes a body of text, chunks it, embeds it, stores it in a vector database, and answers questions about it using only retrieved context — not model memory.


## Stack


| Component | Technology |
|---|---|
| Embeddings | Ollama (all-minilm, local) |
| Vector Store | PostgreSQL + pgvector |
| LLM | Groq API (LLaMA 3.1 8B) |
| Language | Python |


## Architecture


```
Input Text
    │
    ▼
Chunking (sliding window with overlap)
    │
    ▼
Embedding (Ollama all-minilm)
    │
    ▼
Vector Store (PostgreSQL + pgvector)
    │
    ▼
Query → Embed Query → Cosine Similarity Search → Top-K Chunks
    │
    ▼
Context Injection → LLM (Groq) → Answer
```


## How It Works


**Chunking** — Text is split into overlapping word windows. Overlap preserves context across chunk boundaries so retrieval doesn't miss information split at a boundary.


**Embedding** — Each chunk is embedded locally using Ollama with the all-minilm model. No external embedding API calls — runs fully local.


**Vector Storage** — Embeddings are stored in PostgreSQL using the pgvector extension. Similarity search uses cosine distance (`<=>` operator) to find the most relevant chunks for a given query.


**Retrieval** — At query time the question is embedded using the same model, top-K most similar chunks are retrieved from the vector store.


**Generation** — Retrieved chunks are injected as context into a prompt. The LLM (LLaMA 3.1 8B via Groq) is instructed to answer only from the provided context — reducing hallucination.


## Setup


### Prerequisites


- PostgreSQL with pgvector extension installed
- Ollama running locally with all-minilm pulled
- Groq API key


### Environment Variables


```bash
export DB_NAME=your_db_name
export DB_USER=your_db_user
export DB_PASSWORD=your_db_password
export DB_HOST=localhost
export DB_PORT=5432
export GROQ_API_KEY=your_groq_api_key
```


### Database Setup


```sql
CREATE EXTENSION IF NOT EXISTS vector;


CREATE TABLE documents (
    id SERIAL PRIMARY KEY,
    content TEXT,
    embedding vector(384)
);
```


### Install Dependencies


```bash
pip install psycopg2-binary requests groq
```


### Run


```python
from rag_pipeline import rag_pipeline


# Load your text
with open("your_document.txt") as f:
    words = f.read().split()


# Build the pipeline
pipeline = rag_pipeline(words)
pipeline.build_vector_store()


# Query
answer = pipeline.model__("Your question here")
```


## Design Decisions


**Why pgvector over a dedicated vector DB?** Keeps the stack simple — one database for both structured data and vectors. Sufficient for learning and small-to-medium scale.


**Why local embeddings?** Privacy, no API costs, and forces understanding of what embeddings actually are rather than treating them as a black box.


**Why context-only prompting?** Reduces hallucination. The model is explicitly told to say "I don't have enough information" rather than guess — which is the correct behavior for a retrieval system.


## What's Missing (Intentionally)


This is a learning project focused on understanding the core RAG loop. Not included:
- Reranking
- Hybrid search (keyword + vector)
- Metadata filtering
- Streaming responses
- Persistent sessions


## Author


Derick Devassy — [github.com/drunmonk](https://github.com/drunmonk)


