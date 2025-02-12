# Advanced RAG Pipeline on Website

## Overview
This project implements a **Retrieval-Augmented Generation (RAG) pipeline** with **ChromaDB** for fast information retrieval. The system performs **web crawling**, **semantic chunking**, **embedding storage**, and **query-based retrieval**. It can be deployed as a **Streamlit web app** for interactive search.

## Features
### 1. **Web Crawling with Playwright & Crawl4AI**
- Uses **Playwright** for handling dynamic web pages.
- Crawl4AI extracts structured text and metadata.
- Saves data in **JSON format** for further processing.

### 2. **Semantic Chunking & Preprocessing**
- Uses **spaCy** for intelligent text chunking.
- Splits long text into semantically meaningful segments with **overlap** to maintain context.
- Stores chunked data in `semantic_chunked_models.json`.

### 3. **Embedding & Storage in ChromaDB**
- **ChromaDB** stores embeddings for fast search.
- Each chunk is indexed for **efficient retrieval**.
- Uses **Spacy-based embeddings** (can be improved with `sentence-transformers`).

### 4. **Streamlit-Based UI for Retrieval**
- Allows users to **search for relevant information**.
- Retrieves the **most relevant chunks** from ChromaDB.
- Can be extended with **multi-modal search** (text + images).

```


## Folder Structure
```
Advanced-RAG-Pipeline/
│── crawling.ipynb  # Web crawling script
│── embedding_chromadb_streamlit.ipynb  # Data processing & storage
│── data/
│   ├── cleaned_winning_models.json  # Raw extracted data
│   ├── semantic_chunked_models.json  # Chunked and processed text
│── app.py  # Streamlit web interface
│── requirements.txt  # Dependencies
│── README.md  # Project documentation

```

