# LifeScript: Local Document Intelligence System

> **Note on source code:** This repository currently serves as the architecture documentation for the LifeScript system. Because the project is still in active development, handles sensitive personal documents, and relies heavily on local LLM weights, the core backend codebase is kept private for security.

## What is it?
LifeScript is a fully local, 5-module personal document intelligence system. I built this to extract, classify, and query complex data without relying on cloud APIs like OpenAI, ensuring complete data privacy.

It uses a Retrieval-Augmented Generation (RAG) pipeline so users can literally "chat" with their personal documents in natural language.

## Tech Stack
* **Frontend Dashboard:** Streamlit
* **Language Model / Processing:** Python, LangChain, Ollama (Phi-3)
* **Vector Database:** ChromaDB
* **Machine Learning:** Custom NLP algorithms for document classification

## How it works
1. **Extraction & Storage:** Documents are ingested, processed locally, and stored as embeddings in ChromaDB.
2. **Classification:** The system uses custom NLP scripts to automatically categorize incoming documents (currently sitting at an 83.3% accuracy rate across complex file types).
3. **Querying:** Users interact with a responsive Streamlit web dashboard to ask questions. LangChain routes the query through ChromaDB to pull the relevant context, and Ollama (running the Phi-3 model locally) generates the answer.

## Current Status
The core RAG pipeline and frontend dashboard are functional. Active development is currently focused on improving the classification accuracy beyond 83% and optimizing the Streamlit UI to handle larger document batches faster.
