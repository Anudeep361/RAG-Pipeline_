📚 Wikipedia Question Answering (RAG Pipeline)

A simple Retrieval-Augmented Generation (RAG) pipeline that answers questions using Wikipedia content, Sentence Transformers, FAISS, and Hugging Face Transformers.

🚀 Features

Fetches content from Wikipedia

Splits text into chunks

Generates embeddings using Sentence Transformers

Performs fast similarity search with FAISS

Answers questions using a Transformer-based QA model

🛠 Tech Stack

Python 3.9+

Hugging Face Transformers

Sentence-Transformers

FAISS (CPU)

Wikipedia API

NumPy

PyTorch

📦 Installation
pip install wikipedia
pip install faiss-cpu
pip install transformers sentence-transformers torch numpy


⚠️ Restart the kernel/runtime after installing dependencies.

📂 Project Structure
.
├── app.py                 # Main pipeline script
├── README.md              # Project documentation
└── requirements.txt       # Python dependencies

▶️ Usage
question = "What is machine learning?"
answer = qa_pipeline(question)
print(answer)

🧠 How It Works

Wikipedia pages are loaded as source documents

Text is chunked into smaller passages

Each chunk is converted into vector embeddings

FAISS retrieves the most relevant chunks

A QA model extracts the final answer

⚠️ Notes

FAISS runs in CPU mode by default

Triton warnings can be safely ignored

For large-scale production, consider chunk caching and IVF/HNSW indexes

🔮 Future Improvements

Switch to wikipedia-api for better reliability

Add GPU-based FAISS indexing

Support multiple documents and sources

Integrate LLM-based answer generation
