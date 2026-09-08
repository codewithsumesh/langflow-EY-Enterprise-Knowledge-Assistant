 EY Enterprise Knowledge Assistant

A Retrieval-Augmented Generation (RAG) application built using Langflow, OpenAI, and ChromaDB.

This application retrieves information from the EY website, converts the content into vector embeddings, stores it in ChromaDB, and uses an LLM to answer user questions based on the retrieved information.

---

## Architecture

```text
EY Website
    ↓
URL Component
    ↓
Split Text
    ↓
OpenAI Embeddings
    ↓
ChromaDB
    ↓
Semantic Search
    ↓
Parser
    ↓
Prompt Template
    ↓
GPT-4o-mini
    ↓
Chat Output