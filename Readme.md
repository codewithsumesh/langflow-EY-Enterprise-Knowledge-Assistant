# EY Enterprise Knowledge Assistant

A RAG-based enterprise knowledge assistant built using Langflow, OpenAI, and ChromaDB. It retrieves relevant information from the EY website, converts the content into vector embeddings, stores the embeddings in ChromaDB, and uses an LLM to generate answers based on the retrieved context.

## Tech Stack

- Langflow
- OpenAI
- ChromaDB
- GPT-4o-mini
- RAG

## .env requirement

OPENAI_API_KEY

## Workflow

                 EY Website
                      │
                      ▼
                URL Component
                      │
                      ▼
                  Split Text
                chunk_size = 1000
              chunk_overlap = 200
                      │
                      ▼
              OpenAI Embeddings
           text-embedding-3-small
                      │
                      ▼
                 ChromaDB
                      │
                      ▼
              Vector Storage

## When user asks question?

                 Chat Input
                      │
                      ▼
                 ChromaDB
                      │
                      ▼
              Semantic Search
                      │
                      ▼
                   Parser
                      │
                      ▼
              Prompt Template
                      │
                      ▼
               GPT-4o-mini
                      │
                      ▼
                Chat Output.