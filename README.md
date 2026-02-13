🚀 Code Documentation Navigator
AI-Powered Semantic Code Understanding using Retrieval-Augmented Generation (RAG)
📌 Project Overview

Understanding large codebases is time-consuming and cognitively demanding. Developers often spend significant effort navigating files, tracing logic, and interpreting undocumented functions.

Code Documentation Navigator is an AI-powered Retrieval-Augmented Generation (RAG) system that enables intelligent exploration and explanation of GitHub repositories.

The system:

Clones any public GitHub repository

Extracts and processes Python source files

Generates semantic embeddings for code chunks

Stores embeddings in a vector database (ChromaDB)

Retrieves relevant code context

Uses an LLM to generate contextual explanations

This enables semantic code search and automated code understanding.

🎯 Problem Statement

Modern software repositories contain hundreds or thousands of files. Navigating and understanding them manually is inefficient.

Key challenges:

Locating relevant code across modules

Understanding relationships between functions/classes

Reading long files to find specific logic

Lack of documentation

This project addresses these issues by enabling natural language querying over source code.

🏗 System Architecture
User Input (GitHub Repo URL)
          ↓
Clone Repository
          ↓
Extract Python Files
          ↓
Chunk Code (Recursive Text Splitting)
          ↓
Generate Embeddings (SentenceTransformers)
          ↓
Store in ChromaDB (Vector Database)
          ↓
User Question
          ↓
Similarity Search (Top-K Relevant Chunks)
          ↓
LLM Generation (distilgpt2)
          ↓
Context-Aware Explanation

⚙️ Technology Stack
Component	Technology
Programming Language	Python
RAG Framework	LangChain
Vector Database	ChromaDB
Embeddings Model	sentence-transformers/all-MiniLM-L6-v2
Language Model	distilgpt2
Git Integration	GitPython
Text Processing	RecursiveCharacterTextSplitter
🔥 Key Features

Works with any public GitHub repository

Fully automated ingestion pipeline

Semantic search over source code

Context-aware explanation generation

Modular and extensible architecture

Single executable application

Local model execution (no API key required)

📦 Installation
1️⃣ Clone the Repository
git clone https://github.com/yourusername/code-documentation-navigator.git
cd code-documentation-navigator

2️⃣ Install Dependencies
pip install -r requirements.txt

▶️ How to Run
python app.py


You will be prompted to enter a GitHub repository URL.

Example:

https://github.com/psf/requests


After indexing completes, you can ask questions like:

What does this project do?
Explain how HTTP requests are handled.
Describe the Session class.
How does this function work?

🧠 How It Works
1. Repository Ingestion

The system clones the specified GitHub repository locally.

2. Code Extraction

It scans and extracts .py files.

3. Code Chunking

Files are split into manageable chunks using recursive character splitting.

4. Embedding Generation

Each chunk is converted into a semantic vector representation.

5. Vector Storage

Embeddings are stored in ChromaDB for similarity search.

6. Retrieval

When a question is asked:

Top relevant code chunks are retrieved.

They are provided as context to the LLM.

7. Explanation Generation

The LLM generates a natural language explanation based on retrieved code.

📊 Example Use Cases

Rapid onboarding into unfamiliar codebases

Educational tool for understanding open-source projects

Developer productivity enhancement

Semantic search over large repositories

AI-assisted documentation generation

🚀 Future Improvements

Upgrade to instruction-tuned LLM for improved explanation quality

Web interface using Streamlit

Multi-language support (Java, C++, etc.)

Dependency graph visualization

Performance benchmarking on large repositories

Dockerized deployment

Cloud-based API service

📈 Learning Outcomes

Through this project:

Implemented a complete RAG pipeline

Integrated vector databases with LLMs

Built semantic search for code

Designed an end-to-end AI system

Learned practical system architecture for GenAI applications

🔐 Security

This project:

Does not require API keys

Runs fully locally

Does not store sensitive credentials

Uses public repositories only

👤 Author

Akhil Subudhi
AI & Machine Learning Enthusiast

🏆 Project Type

AI Systems Development
Retrieval-Augmented Generation (RAG)
Code Intelligence

📜 License

This project is for educational and research purposes.

🌟 Conclusion

Code Documentation Navigator demonstrates how Retrieval-Augmented Generation can be applied to real-world software engineering challenges, enabling intelligent, context-aware exploration of codebases.
