# 🕵️‍♂️ Fake News Forensic – Detecting & Summarizing Misinformation with GenAI

> A Retrieval-Augmented Generation (RAG) pipeline that leverages embeddings, vector search, and large language models to detect and explain fake news claims.

---

## 🚀 Overview

Misinformation is one of the most pressing issues of our time. This project demonstrates how Generative AI can support fact-checking efforts by retrieving related references from a curated dataset and generating short, grounded explanations using a Large Language Model (LLM).

We combine:

- 🔍 **Embeddings + Vector Stores** for semantic search  
- 🤖 **Retrieval-Augmented Generation (RAG)** for grounded LLM outputs  
- ✍️ **Prompt Engineering** for consistent and structured responses

---

## 🧠 Features

- ✅ Load and label the **ISOT Fake News Dataset**
- ✅ Generate text embeddings using `sentence-transformers`
- ✅ Store embeddings in a FAISS vector index for fast similarity search
- ✅ Use OpenAI's GPT (`gpt-3.5-turbo` or `gpt-4`) to generate short, evidence-based explanations
- ✅ Demonstrate both standard and structured (JSON) LLM outputs
- ✅ Easily extensible: try other models, APIs, or data sources

---

## 📁 Folder Structure
fake-news-forensic/ │ ├── notebook.ipynb # Main Jupyter Notebook ├── README.md # Project documentation (you are here) └── /data/ # Folder for local datasets (optional)


---

## 📦 Requirements

Install dependencies (if not using Kaggle or Colab):

```bash
pip install sentence-transformers langchain chromadb faiss-gpu openai

🔑 OpenAI API Setup
To use the LLM for generation, you’ll need an OpenAI API key:

Create an account at platform.openai.com

Generate an API key

Store it in your environment:
import openai
openai.api_key = "your-key-here"


