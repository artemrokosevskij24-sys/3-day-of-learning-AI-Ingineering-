Python & AI Embeddings Learning Journey 🚀

Welcome to my repository! This project documents my practical exploration of embeddings, vector databases, and integrating Google Gemini API into local Python workflows.

📂 What's Inside

This repository contains two main scripts demonstrating how text representations work and how to build a semantic search pipeline:

1. first_embedding.py — Manual Vectors & Cosine Similarity

What it does: Sends raw text strings to the Google Gemini API (gemini-embedding-001) to generate multi-dimensional vector embeddings.

Core Concepts:

Extracting raw float values from vector responses (result.embeddings[0].values).

Implementing a mathematical Cosine Similarity function using numpy (np.dot and np.linalg.norm).

Comparing semantic proximity between related sentences (e.g., morning jogs) vs. unrelated topics (e.g., PC hardware optimization).

2. chroma_test.py — Semantic Search with ChromaDB & Custom Gemini Embeddings

What it does: Sets up a local vector database (ChromaDB) and equips it with a custom embedding function powered by Google Gemini.

Core Concepts:

Writing a Custom Embedding Function (chromadb.EmbeddingFunction) to bridge ChromaDB and the modern google-genai SDK.

Storing documents with unique IDs (collection.add(...)).

Performing local semantic queries (collection.query(...)) to retrieve the most contextually relevant documents based on meaning rather than exact keyword matching.

🛠️ Tech Stack & Libraries

Python 3.x

Google GenAI SDK (google-genai)

ChromaDB (Vector database)

NumPy (Mathematical operations for similarity)

Python-Dotenv (Secure environment variable management)

⚙️ Getting Started & Installation

Clone the repository:

git clone <your-repository-url>
cd <repository-folder>


Install the required dependencies:

pip install google-genai chromadb numpy python-dotenv


Set up your API Key:

Create a .env file in the root directory.

Add your Google Gemini API key:

GEMINI_API_KEY="your_api_key_here"


Run the scripts:

python first_embedding.py
python chroma_test.py
