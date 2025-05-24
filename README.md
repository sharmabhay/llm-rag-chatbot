# llm-rag-chatbot

A Retrieval-Augmented Generation (RAG) chatbot built with Streamlit, LangGraph, and GPT-4. Users can upload documents or point to knowledge sources and have the chatbot answer questions related to the healthcare data.

Future developments include creating a personalized Large Language Model (LLM) from scratch.


## Features

- **Document Ingestion**
  - Upload PDFs, text files, or point to URLs
  - Automatic text extraction and chunking

- **Vector Store Retrieval**
  - Embedding-based search (FAISS, Chroma, etc.)
  - Fast similarity lookup

- **LangChain + LangGraph Orchestration**
  - Chain of retrieval → context assembly → generation
  - Graph-based prompt management

- **Interactive Streamlit UI**
  - Chat interface with streaming responses
  - Sidebar for uploading, selecting knowledge sources, and model settings
  - Conversation history persistence

- **Configurable LLM Backend**
  - Support for OpenAI, Azure, local models (e.g. Llama 2 via HuggingFace)
  - Temperature, max tokens, and top-k/top-p tuning


## Installation

1. **Clone the repo**
   ```bash
   git clone https://github.com/sharmabhay/llm-rag-chatbot.git
   cd llm-rag-chatbot
   ```

2. **Create & activate a virtualenv**
    ```bash
    python3 -m venv .venv
    source .venv/bin/activate   # macOS/Linux
    .venv\Scripts\activate      # Windows
    ```

3. **Install depedencies**
    ```bash
    pip install -r requirements.txt
    ```

4. **Set up environment variables**
    Create a `.env` in the project root:
    ```
    AZURE_OPENAI_API_KEY=...
    AZURE_OPENAI_DEPLOYMENT_NAME=...
    AZURE_ENDPOINT=...
    AZURE_OPENAI_VERSION=...

    TAVILY_API_KEY=...

    PINECONE_API_KEY=...
    PINECONE_ENV=...
    ```


## Usage

```bash
streamlit run app.py
```
