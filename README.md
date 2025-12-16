Wikipedia Question Answering (RAG)

A lightweight Retrieval-Augmented Generation (RAG) pipeline that answers user questions using Wikipedia content, semantic search, and Transformer-based question answering.

Overview

This project retrieves relevant information from Wikipedia, performs vector similarity search using FAISS, and extracts precise answers using a pre-trained Transformer QA model.

Tech Stack

Python 3.9+

Wikipedia API

Sentence Transformers (Embeddings)

FAISS (Vector Search)

Hugging Face Transformers

PyTorch, NumPy

Installation
pip install wikipedia
pip install faiss-cpu
pip install transformers sentence-transformers torch numpy


Restart the kernel/runtime after installation.

Usage
question = "What is machine learning?"
answer = qa_pipeline(question)
print(answer)

Architecture

Load Wikipedia documents

Chunk text into passages

Generate embeddings

Retrieve top-K relevant chunks using FAISS

Extract answer using a QA model

Notes

FAISS runs in CPU mode by default

Triton warnings can be safely ignored

Designed for clarity and learning; production setups may require optimization

Future Enhancements

Improved document loaders

GPU-based FAISS indexing

Support for multiple knowledge sources

LLM-based answer generation
