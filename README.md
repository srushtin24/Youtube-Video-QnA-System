# YouTube Video QnA System

An end-to-end Retrieval-Augmented Generation (RAG) system that enables semantic question answering over YouTube video content. The system extracts transcripts, performs embedding-based retrieval, and generates context-aware responses using a Large Language Model (LLM).


## 🚀 Overview

This project implements a production-style RAG pipeline that allows users to query YouTube videos using natural language. It leverages transcript extraction, semantic search over embeddings, and LLM-based generation to produce accurate, context-grounded answers while minimizing hallucinations..


## ✨ Key Features

- **Semantic Retrieval over Video Transcripts**  
  Retrieves relevant content using embedding-based similarity search

- **Context-Grounded Response Generation**  
  Constrains LLM output using retrieved transcript segments

- **Efficient Handling of Long Content**  
  Uses chunking to process and query large transcripts

- **Modular Pipeline Design**  
  Separates ingestion, retrieval, and generation components


## 🧠 System Architecture<br>

→ Transcript Extraction (yt-dlp)
→ Transcript Parsing & Cleaning
→ Text Chunking (LangChain Recursive Splitter)
→ Embedding Generation
→ Vector Storage (FAISS)
→ User Query
→ Query Embedding
→ Top-K Semantic Retrieval
→ Prompt Construction
→ LLM Inference (Groq API)
→ Final Answer


## ⚙️ Pipeline Execution Flow
1. Extract subtitles using yt-dlp in JSON3 format
2. Parse and clean transcript into structured segments
3. Split transcript into semantically meaningful chunks
4. Convert text chunks into vector embeddings (embedding model configurable)
5. Store embeddings in FAISS vector index
6. Convert user query into embedding
7. Retrieve top-K relevant chunks using similarity search
8. Construct prompt using retrieved context + user query
9. Generate response using LLM via Groq API


## 🏗️ Tech Stack

1. Core AI / GenAI
   - Retrieval-Augmented Generation (RAG)
   - Large Language Models (LLMs) via Groq API
   - Prompt Engineering
2. Data & Retrieval
  - FAISS (Vector Database)
  - Embeddings (e.g., SentenceTransformers / OpenAI – configurable)
3. Libraries & Tools
  - LangChain
  - yt-dlp (Transcript Extraction)
  - youtube-transcript-api
  - tiktoken
  - python-dotenv 

## ⚡ System Strengths
- Grounded responses reduce hallucination
- Efficient semantic retrieval over long transcripts
- Scalable and modular pipeline design
- Works effectively on unstructured video data

## ▶️ Usage
- Provide a YouTube video URL
- System extracts transcript automatically
- Ask questions related to the video
- Receive accurate, context-aware answers

## 🚀 Future Improvements
- Multi-video knowledge base support
- Conversational memory (multi-turn chat)
- Hybrid search (keyword + vector retrieval)
- Response evaluation metrics (accuracy, relevance)
- Deployment (FastAPI backend + React frontend)
