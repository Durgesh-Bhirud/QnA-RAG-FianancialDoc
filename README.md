# 📊 Financial Document Q&A Bot using RAG (Azure OpenAI)

## 🔍 Overview

This project implements an AI-powered Question Answering (Q&A) system designed to extract insights from financial reports (PDFs).

It leverages Retrieval-Augmented Generation (RAG) to provide accurate, context-aware answers to user queries.

---

## 🎯 Problem Statement

Financial reports are complex, containing:
- Unstructured text
- Structured tables
- Financial metrics

Manual analysis is:
- Time-consuming
- Error-prone
- Requires expertise

👉 This system automates financial understanding using AI.

---

## 🧠 Solution

The system:
1. Extracts text and tables from PDFs
2. Converts them into embeddings
3. Stores them in a vector database
4. Retrieves relevant context for queries
5. Uses LLMs (GPT-3.5 / GPT-4) to generate answers
6. Evaluates responses using a second LLM

---

## ⚙️ Key Features

- 📄 PDF + Table extraction
- 🧠 RAG-based architecture
- 🔍 Semantic search (ChromaDB)
- 🤖 Dual-model system (generation + evaluation)
- 💬 Conversation memory
- 📊 Response scoring (0–100)

---

## 🏗️ Architecture

# 🧠 Model Architecture

The system follows a multi-layer RAG architecture.

<img width="848" height="412" alt="Screenshot 2026-04-07 131023" src="https://github.com/user-attachments/assets/b2bf5016-24e2-4fcc-abb9-f8d1ef00d250" />

---

## 🔹 1. Document Processing Layer

- PyPDF → Extracts text
- Camelot → Extracts tables
- Chunking:
  - Size: 512
  - Overlap: 20

---

## 🔹 2. Embedding Layer

- Azure OpenAI Embeddings
- Converts text → vectors

Stored in:
- ChromaDB vector database

---

## 🔹 3. Retrieval Layer

- Uses cosine similarity
- Top-K retrieval (k=5)

---

## 🔹 4. Response Generation Layer

- Models:
  - GPT-3.5
  - GPT-4

Input:
- Query + retrieved context

---

## 🔹 5. Evaluation Layer

- Second LLM evaluates response
- Score: 0–100

---

## 🧠 Key Insight

Using dual LLMs improves:
- Reliability
- Trustworthiness
- Performance analysis

---

## 🧪 Example Capabilities

- "What is the company’s net profit?"
- "What are the key risk factors?"
- "Compare revenue trends"

---

## ⚠️ API Note

Azure OpenAI subscription has expired.

👉 To run:
- Add your own API keys

---

## 📸 Demo

<img width="829" height="438" alt="Screenshot 2026-04-07 131220" src="https://github.com/user-attachments/assets/2c1d8cb8-4923-4f14-afc7-524d3df70362" />


---

## 🧠 Key Learnings

- Built full RAG pipeline
- Implemented evaluation system using LLM
- Applied prompt engineering + CoT reasoning
- Handled financial document complexity

---

## 👤 Author

Durgesh Bhirud
