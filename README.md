# 📄 Document-Based Q&A Chatbot using LangChain, LlamaIndex, and Groq

A simple Retrieval-Augmented Generation (RAG) chatbot that indexes a local text document and answers user questions based on the document's content.

## 🚀 Features

- Load and index local text files
- Retrieve relevant document context using LlamaIndex
- Generate accurate answers using Groq's Llama model
- Prompt management using LangChain
- Fast and lightweight implementation
- Interactive question-answering interface

---

## 🛠️ Tech Stack

- **LlamaIndex** – Document loading, indexing, and retrieval
- **LangChain** – Prompt template management
- **Groq** – Large Language Model (LLM)
- **HuggingFace Embeddings** – Text embeddings for semantic search
- **Python** – Core programming language

---

## 📂 Project Structure

```text
.
├── sample.txt              # Input document
├── chatbot.ipynb           # Main notebook
├── requirements.txt        # Dependencies
└── README.md
```

---

## ⚙️ Installation

### 1. Clone the repository

```bash
git clone <your-repository-url>
cd <repository-name>
```

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

Or

```bash
pip install llama-index \
            llama-index-llms-groq \
            llama-index-embeddings-huggingface \
            langchain \
            langchain-core
```

---

## 🔑 Configure Groq API Key

Create a Groq API key from:

https://console.groq.com/keys

Then set your API key:

```python
my_api_key = "YOUR_GROQ_API_KEY"
```

---

## 📖 How It Works

### Step 1: Load Documents

The chatbot reads a local text file using LlamaIndex.

### Step 2: Create Embeddings

The document is converted into vector embeddings using the HuggingFace model:

```text
sentence-transformers/all-MiniLM-L6-v2
```

### Step 3: Build Vector Index

LlamaIndex creates a searchable vector index from the document.

### Step 4: Retrieve Relevant Context

When a user asks a question, the most relevant content is retrieved from the document.

### Step 5: Generate Response

The retrieved context and user query are passed to Groq's Llama model to generate an answer.

---

## 💬 Example

### Input Document

```text
Paris is the capital of France.
The Eiffel Tower is located in Paris.
```

### User Query

```text
What is the capital of France?
```

### Chatbot Response

```text
The capital of France is Paris.
```

---

## ▶️ Running the Chatbot

```python
while True:
    question = input("You: ")

    if question.lower() == "exit":
        break

    response = chatbot(question)
    print("Bot:", response)
```

---

## 🎯 Learning Outcomes

This project demonstrates:

- Document indexing with LlamaIndex
- Semantic search using embeddings
- Retrieval-Augmented Generation (RAG)
- Prompt engineering with LangChain
- Integration of Groq LLMs
- Building a simple document-based chatbot

---

## 📌 Future Improvements

- Support PDF and DOCX files
- Add chat history memory
- Build a Streamlit web interface
- Support multiple documents
- Add citation/source references
- Deploy as a web application

---

Built as part of learning and exploring Retrieval-Augmented Generation (RAG), LangChain, LlamaIndex, and Groq-powered AI applications.
