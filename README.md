# RAG Chatbot with IBM WatsonX AI & LangChain

This repository provides a **Retrieval-Augmented Generation (RAG) chatbot** using **IBM Watsonx AI** and **Langchain**. It allows users to upload a **PDF document** and ask questions about its content. The chatbot retrieves relevant information from the document and generates answers using a combination of **document retrieval** and **text generation**. A simple **Gradio interface** enables easy interaction, letting users upload files and submit queries seamlessly.

## Features

- **PDF Document Upload**: Upload a PDF document for processing.
- **Question Answering**: Ask questions related to the uploaded document, and receive generated answers.
- **IBM Watsonx AI Integration**: Utilizes IBM Watsonx models for text generation and embedding.
- **Gradio Interface**: A user-friendly interface for document uploads and queries.

## How It Works

1. **Document Upload**: Upload a PDF, and the app extracts the content using Langchain’s `PyPDFLoader`.
2. **Text Chunking**: The document is split into smaller chunks for easier processing.
3. **Embedding**: The document chunks are embedded using **IBM Watsonx AI** and stored in a Chroma vector database.
4. **Query Handling**: When a user submits a query, the chatbot retrieves relevant document chunks and generates an answer using the **IBM Watsonx AI model**.
5. **Interactive Chat**: Users interact with the chatbot through the Gradio interface, uploading documents and typing queries.

## Installation

### Option 1: Using `pyenv` and `requirements.txt`

1. **Create a virtual environment** (optional but recommended):
    ```bash
    pyenv virtualenv 3.9.13 rag-chatbot-env
    pyenv activate rag-chatbot-env
    ```

2. **Clone this repository**:
    ```bash
    git clone https://github.com/nadeen-elsaued/RAG_Chatbot.git
    cd RAG_Chatbot
    ```

3. **Install dependencies**:
    ```bash
    pip install -r requirements.txt
    ```

4. **Run the application**:
    ```bash
    python qa_bot.py
    ```

   The app will be hosted locally at `http://127.0.0.1:7862`, and you can also access it via a public link.

