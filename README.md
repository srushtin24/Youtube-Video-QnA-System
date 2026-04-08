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


## 🧠 System Architecture<br>

YouTube Video URL<br>
↓<br>
Transcript Extraction<br>
↓<br>
Text Chunking<br>
↓<br>
Embedding Generation<br>
↓<br>
Vector Store (ChromaDB)<br>
↓<br>
User Query<br>
↓<br>
Top-K Semantic Retrieval<br>
↓<br>
Context Injection into Prompt<br>
↓<br>
LLM Response Generation<br>


## ⚙️ How It Works

1. Extract transcript from a YouTube video  
2. Split transcript into smaller chunks  
3. Generate embeddings and store them in a vector database  
4. Accept user query  
5. Retrieve top-k relevant chunks using semantic similarity  
6. Inject retrieved context into the LLM prompt  
7. Generate and return a grounded answer  


## 🏗️ Tech Stack

- **LLM & Orchestration:** LangChain, LLM APIs  
- **Vector Database:** ChromaDB  
- **Embeddings:** Sentence Transformers / OpenAI  
- **Backend / Processing:** Python  

## 🚀 Future Improvements

- Multi-video knowledge base  
- Source attribution (timestamps)  
- Hybrid retrieval (keyword + vector search)  
- API deployment for production use 
