# AI_chatbot
# 🧠 RAG-Powered AI Chatbot with PDF Support

This project is an AI chatbot built using **Retrieval-Augmented Generation (RAG)**. It allows users to upload a PDF document, extracts and indexes its contents, and provides intelligent answers based on user queries — powered by **DeepSeek R1** via **Ollama** and orchestrated with **LangChain**.

## 🚀 Features

- 📄 Upload and parse PDF documents
- 🧠 Context-aware responses using RAG
- 🔎 Semantic search with **FAISS** and **Qdrant**
- 🤖 LLM-powered answer generation with **DeepSeek R1** (via Ollama)
- 🛠️ Modular architecture using **LangChain**
- 🌐 Interactive UI built with **Streamlit**

## 🧰 Tech Stack

| Component        | Technology Used                |
|------------------|--------------------------------|
| PDF Parsing      | `PyMuPDF`, `pdfplumber`, etc.  |
| Embeddings       | DeepSeek Embeddings via Ollama |
| Vector Store     | `FAISS`, `Qdrant`              |
| LLM              | `DeepSeek R1` via `Ollama`     |
| Framework        | `LangChain`                    |
| Frontend         | `Streamlit`                    |

## 📚 How It Works

1. **PDF Upload**: Users upload a PDF via the Streamlit UI.
2. **Text Extraction**: The PDF is parsed into clean, readable chunks.
3. **Embedding Generation**: Text chunks are converted into embeddings using Ollama + DeepSeek.
4. **Vector Indexing**: Embeddings are stored in FAISS/Qdrant for efficient semantic search.
5. **Query Handling**: User's query is embedded and matched to top-k relevant chunks.
6. **RAG Pipeline**: Retrieved context + query is passed to DeepSeek R1 for answer generation.
7. **Response Display**: The answer is shown back to the user in the Streamlit interface.
