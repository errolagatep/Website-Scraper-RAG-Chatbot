# 🔍 Website Scraper & RAG Chatbot with Pinecone (n8n Workflows)

This repository contains two powerful **n8n** workflows:

1. **Website Scraper & Pinecone Uploader**
2. **Chatbot with Retrieval-Augmented Generation (RAG)**

Together, they enable a fully functional **RAG-based chatbot** that scrapes website content, stores it as vector embeddings in Pinecone, and uses it to answer user questions intelligently.


## 📁 Workflow 1: Website Scraper & Pinecone Uploader

### 🔧 Purpose

This workflow scrapes content from a specified website, converts it into Markdown, processes it, and uploads it as vector embeddings into **Pinecone** for future retrieval.

### 🔄 Flow

1. **Trigger**: Manual start (`Execute workflow`).
2. **HTTP Request**: Fetches raw HTML content from the target website.
3. **Markdown Conversion**: Transforms HTML into Markdown for clean text formatting.
4. **Text File Creation**: Saves content as a text file (e.g., to Google Drive or local).
5. **Text Splitting**: Splits long text into manageable chunks for embedding.
6. **OpenAI Embeddings**: Generates embeddings using OpenAI.
7. **Pinecone Vector Store**: Stores the embeddings for semantic search.


## 💬 Workflow 2: RAG Chatbot with Pinecone & Tools

### 🔧 Purpose

This chatbot answers user questions by retrieving relevant documents from **Pinecone** and augmenting them into prompts for an **OpenAI-powered chat model** (RAG approach).

### 🔄 Flow

1. **Trigger**: Activated when a user sends a chat message.
2. **AI Agent**:
   - Uses **OpenAI Chat Model**.
   - Retrieves relevant context from **Pinecone Vector Store**.
   - Optionally uses:
     - `BYDCars_q` for domain-specific queries.
     - `SerpAPI` for web search.
     - `Simple Memory` for persistent session context.
3. **Response Generation**: Combines retrieved context + message into a single intelligent reply.


## 🧠 Technologies Used

- 🌐 **n8n** (Automation platform)
- 📄 **Markdown & HTML parsing**
- 🤖 **OpenAI** (Chat & Embeddings)
- 🧠 **Pinecone** (Vector DB)
- 🛠️ **SerpAPI**, **Wikipedia**, and optional tools for extended knowledge
- 💾 **Simple Memory** for short-term context storage


## ⚙️ Use Cases

- Company documentation bots  
- Customer service AI with up-to-date site content  
- Internal tools for technical teams  
- Chatbots with enhanced domain knowledge


## ✍️ Author

Created by - Errol Ace Agatep
Contributions and suggestions are welcome!
