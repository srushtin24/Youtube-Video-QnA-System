# YouTube Video QnA System

A retrieval-augmented question-answering system that enables users to query YouTube video content using natural language. The system processes transcripts, retrieves relevant context using semantic search, and generates grounded responses using an LLM.


## 🚀 Overview

This project implements a **Retrieval-Augmented Generation (RAG)** pipeline over YouTube transcripts. Video content is converted into embeddings and stored in a vector database. For each query, the system retrieves the most relevant transcript segments and uses them to guide LLM responses, improving accuracy and reducing hallucinations.


## ✨ Key Features

- **Semantic Retrieval over Video Transcripts**  
  Retrieves relevant content using embedding-based similarity search

- **Context-Grounded Response Generation**  
  Constrains LLM output using retrieved transcript segments

- **Efficient Handling of Long Content**  
  Uses chunking to process and query large transcripts

- **Modular Pipeline Design**  
  Separates ingestion, retrieval, and generation components

---

## 🧠 System Architecture
