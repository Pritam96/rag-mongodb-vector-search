# MongoDB Vector Search RAG with OpenAI

This project demonstrates how to build a Retrieval-Augmented Generation (RAG) pipeline using MongoDB Vector Search and OpenAI's Large Language Models (LLMs). It extracts text from a PDF, generates embeddings, stores them in MongoDB, and performs semantic searches to answer user queries based on the document's context.

## Features
* **Document Ingestion:** Uses LangChain to load and split PDF documents into manageable chunks.
* **Vector Embeddings:** Utilizes OpenAI's `text-embedding-3-large` model to convert text into high-dimensional vector embeddings.
* **Vector Database:** Stores embeddings securely in MongoDB and utilizes MongoDB Atlas Vector Search for fast, similarity-based retrieval.
* **Contextual Q&A:** Uses OpenAI's `gpt-4o` to generate accurate answers based strictly on the retrieved document context.
* **Secure Configuration:** Manages API keys and database credentials securely using a `.env` file.

## Technologies Used
* Python 3.x
* [OpenAI API](https://platform.openai.com/) (Embeddings & Chat Completions)
* [MongoDB Atlas](https://www.mongodb.com/products/platform/atlas-vector-search) (Vector Search)
* [LangChain](https://python.langchain.com/) (Document loading and text splitting)
* Jupyter Notebook

## Prerequisites
Before running the notebook, ensure you have the following:
1. An active [OpenAI API key](https://platform.openai.com/api-keys).
2. A [MongoDB Atlas](https://www.mongodb.com/cloud/atlas/register) cluster set up with database access.
3. Python installed on your local machine.

## Installation and Setup

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/Pritam96/rag-mongodb-vector-search.git](https://github.com/Pritam96/rag-mongodb-vector-search.git)
   cd rag-mongodb-vector-search
   ```

2. **Install the required dependencies:**
   ```bash
   pip install openai pymongo langchain-community langchain-text-splitters python-dotenv pypdf
   ```

3. **Set up your environment variables:**
   Create a `.env` file in the root directory and add your credentials securely:
   ```env
   OPENAI_API_KEY="your_openai_api_key_here"
   MONGO_URI="your_mongodb_connection_string_here"
   ```

4. **Run the project:**
   Launch Jupyter Notebook and open `rag.ipynb` to execute the cells step-by-step:
   ```bash
   jupyter notebook
   ```