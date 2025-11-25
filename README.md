# 🍕 Restaurant Review RAG Assistant (LangChain + Ollama + Chroma)

A **Retrieval-Augmented Generation (RAG)** assistant built using **LangChain**, **Ollama**, and **ChromaDB**.  
It analyzes restaurant reviews and answers questions using both semantic search and LLM reasoning.

---

## 🚀 Features

- Offline LLM using **Ollama**
- **mxbai-embed-large** for embeddings
- **ChromaDB** for vector search
- Fully local RAG pipeline
- Interactive CLI chatbot
- Clean project structure

---

## 📁 Project Structure

```
AIAgent/
│── main.py                  # Chat/chat loop
│── vector.py                # Vector store creation + retriever
│── realistic_restaurant_reviews.csv
│── README.md
│── venv/
│── .gitignore
```

---

## ▶️ Setup Instructions

### 1️⃣ Install Ollama  
Download: https://ollama.com/download

Verify:
```bash
ollama --version
```

### 2️⃣ Install required LLM + embedding model

```bash
ollama pull llama3.1
ollama pull mxbai-embed-large
```

---

## 3️⃣ Create virtual environment

```bash
python3 -m venv venv
source venv/bin/activate
```

---

## 4️⃣ Install dependencies

```bash
pip install langchain langchain-ollama langchain-chroma chromadb pandas
```

---

## 5️⃣ Build vector database

```bash
python3 vector.py
```

---

## 6️⃣ Run chatbot

```bash
python3 main.py
```

Input example:
```
What is the best pizza in town?
```

---

## 🧠 How RAG Works

1. User question  
2. Retriever finds top relevant reviews  
3. LLM (via Ollama) receives:  
   - reviews  
   - user question  
4. LLM generates a final answer  

---

## 📌 Future Enhancements
- Add FastAPI API endpoint  
- Add UI (Streamlit / Gradio)  
- Add sentiment analysis  
- Add vector store evaluation  

---

## 🏆 Good For
Portfolio projects for:
- AI Engineers  
- LLM Developers  
- Data Scientists  
- NLP/RAG Engineers
