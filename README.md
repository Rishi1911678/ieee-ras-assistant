# ieee-ras-assistant
# IEEE RAS RAG AI Assistant

This repository contains a Retrieval-Augmented Generation (RAG) assistant built for the IEEE Robotics and Automation Society (IEEE RAS). The application processes domain documentation into a vector database to answer user questions accurately based on retrieved context.

Live Application: ieee-ras-rogassistant-19678.streamlit.app

## Overview

The system loads source text documents, splits them into semantic chunks, and creates vector embeddings stored in a FAISS vector store. When a query is submitted, relevant document chunks are retrieved via vector similarity search and processed through Google Gemini to generate a response. If no API key is present or available, the system falls back to displaying the raw retrieved context chunks directly.

## Technology Stack

* Language: Python 3.14
* Web Framework: Streamlit
* RAG Framework: LangChain
* Vector Store: FAISS
* Embeddings: Hugging Face (sentence-transformers/all-MiniLM-L6-v2)
* LLM: Google Gemini API

## File Structure

* app.py - Main Streamlit application and RAG pipeline code
* ieee_ras_info.txt - Source domain documentation file
* requirements.txt - Required Python dependencies
* README.md - Project documentation

## Installation and Local Running

1. Clone the repository:
   git clone https://github.com/Rishi1911git/ieee-ras-rogassistant.git
   cd ieee-ras-rogassistant

2. Install the required dependencies:
   pip install -r requirements.txt

3. Start the application:
   streamlit run app.py
