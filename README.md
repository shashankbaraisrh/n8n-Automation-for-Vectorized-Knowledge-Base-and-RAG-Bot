# n8n-Automated Knowledge Base RAG Bot


## Overview

This project demonstrates an **end-to-end Retrieval-Augmented Generation (RAG) system** built using **n8n automation**, **Pinecone vector database**, and **OpenAI models**.

The system automatically transforms unstructured documents into a **searchable vector knowledge base** and enables **semantic question answering** through a RAG bot.


---

## Architecture Summary

The solution consists of **two dependent workflows**:

1. Automated Knowledge Base Creation  
2. RAG Bot for Semantic Retrieval  

Both workflows are orchestrated using **n8n** and connected through **Pinecone**.


---

## 1. Automated Document-to-Vector Pipeline

- Documents (Tesla financial reports) are uploaded to Google Drive  
- n8n automatically triggers ingestion and processing  
- Documents are chunked using a recursive text-splitting strategy  
- OpenAI embeddings are generated for each chunk  
- Vectors are stored in Pinecone for semantic search  

**Outcome:**  
A continuously updatable **vectorized knowledge base** with no manual intervention.


---

## 2. RAG Bot on Top of the Knowledge Base

- User queries are received via a chat interface  
- Queries are embedded and matched against Pinecone vectors  
- Relevant document context is retrieved in real time  
- An LLM generates **accurate, source-grounded responses**  
- Conversation memory enables contextual follow-up questions  

**Outcome:**  
A RAG bot that answers questions strictly based on the ingested documents.


---

## Tech Stack

- **n8n** – Workflow automation and orchestration  
- **Pinecone** – Vector database for semantic retrieval  
- **OpenAI** – Embeddings and LLM-based response generation  
- **Google Drive** – Document source  
- **RAG Architecture** – Retrieval-Augmented Generation  


---

## Key Features

- Fully automated document ingestion  
- Scalable vector knowledge base  
- Semantic search over financial documents  
- Reduced hallucination via document grounding  
- Modular and extensible architecture  


---

## Use Case Example

> **Question:**  
> *What was Tesla’s total automotive revenue in Q4 2024?*  

The bot retrieves the most relevant sections from Tesla’s reports and generates a factual, context-backed answer.


---

## Visual Overview

The repository includes a merged workflow diagram illustrating:

- Knowledge base automation pipeline  
- RAG bot querying layer  


---

## Why This Project

This project demonstrates practical experience in:

- AI workflow automation  
- Vector databases and embeddings  
- Retrieval-Augmented Generation  
- Applied LLM system design  

