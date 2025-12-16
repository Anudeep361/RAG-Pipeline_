📚 Wikipedia Question Answering System

A retrieval-augmented question answering (RAG) system that uses Wikipedia as a knowledge source, semantic vector search for retrieval, and Transformer-based models for answer extraction.

🧩 Description

This project implements an end-to-end pipeline that retrieves relevant Wikipedia passages using dense embeddings and FAISS, then extracts accurate answers using a pre-trained question-answering model.

⚙️ Core Components

📄 Document Ingestion: Wikipedia content retrieval

🧠 Embedding Layer: Sentence Transformers

🔍 Vector Store: FAISS for similarity search

🤖 Inference Layer: Hugging Face Transformer QA model

🛠️ Technology Stack

🐍 Python

🌐 Wikipedia API

🧬 Sentence-Transformers

⚡ FAISS (CPU)

🤗 Hugging Face Transformers

🔥 PyTorch, NumPy

🚀 Setup
pip install wikipedia faiss-cpu transformers sentence-transformers torch numpy


🔄 Restart the runtime after installing dependencies.

▶️ Example Usage
query = "What is machine learning?"
response = qa_pipeline(query)
print(response)

🔄 System Flow

📥 Fetch and preprocess Wikipedia documents

✂️ Split text into manageable chunks

🧠 Generate vector embeddings

🔎 Retrieve top-matching passages via FAISS

✅ Extract answers using a QA model

📌 Design Notes

Clean, modular, and easy to extend

Runs fully on CPU by default

⚠️ Triton-related warnings do not impact functionality

🗺️ Roadmap

➕ Multiple data source support

🚀 GPU-accelerated indexing

🧭 Advanced retrieval strategies (HNSW, IVF)

✨ LLM-based generative answering
