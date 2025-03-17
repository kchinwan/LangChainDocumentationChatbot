LangChain Documentation Chatbot

This project implements a RAG (Retrieval-Augmented Generation) based chatbot that interacts with LangChain documentation using embeddings and Pinecone for vector storage. The chatbot is deployed both as a Streamlit web application and a FastAPI/Flask API.

🚀 Project Overview

Goal: To build a chatbot capable of answering user queries related to LangChain documentation using embeddings and retrieval-based generation.

Tech Stack:

LangChain

Pinecone

Hugging Face Transformers (Embeddings & LLM)

Streamlit (Web App)

FastAPI/Flask (API)

Python

📂 Project Structure
📁 LangChainDocumentationChatbot
├── 📁 data
├── 📁 notebooks
│   ├── 1_load_docs.ipynb
│   ├── 2_preprocess_docs.ipynb
│   ├── 3_create_embeddings.ipynb
│   ├── 4_upload_pinecone.ipynb
│   ├── 5_build_chatbot.ipynb
│   └── 6_test_chatbot.ipynb
├── 📁 api
│   ├── main.py
├── 📁 app
│   ├── app.py
├── 📁 saved_models
│   └── embeddings.pkl
├── 📄 requirements.txt
├── 📄 README.md
├── 📄 .env

📖 How It Works

Document Loading & Preprocessing:

Load all .mdx files from the LangChain documentation.

Clean and split documents into smaller chunks for embeddings.

Embeddings & Pinecone Storage:

Generate embeddings using sentence-transformers/all-MiniLM-L6-v2.

Store the embeddings in Pinecone with metadata.

Building the Chatbot:

Create a retriever using Pinecone vector store.

Utilize HuggingFaceHub LLM (tiiuae/falcon-7b-instruct) for querying.

Set up a LangChain RetrievalQA pipeline.

Deployment:

Streamlit App: Interactive web app for chatbot interaction.

FastAPI/Flask API: Provides an API endpoint to get answers from the chatbot.

💻 Installation

Clone the repository:
$ git clone https://github.com/your-username/LangChainDocumentationChatbot.git
$ cd LangChainDocumentationChatbot

2. Install dependencies:
$ pip install -r requirements.txt

3. Set up environment variables (.env file):
PINECONE_API_KEY=<your_pinecone_api_key>
PINECONE_ENVIRONMENT=<your_pinecone_environment>
HUGGINGFACEHUB_API_TOKEN=<your_huggingfacehub_api_token>


🔍 Usage

1. Generate & Store Embeddings

Run the notebooks in sequence:

1_load_docs.ipynb

2_preprocess_docs.ipynb

3_create_embeddings.ipynb

4_upload_pinecone.ipynb

2. Build & Test the Chatbot

5_build_chatbot.ipynb

6_test_chatbot.ipynb

3. Deploy the App (Streamlit)

    streamlit run app/app.py

4. Deploy the API (FastAPI/Flask)

    python api/main.py


