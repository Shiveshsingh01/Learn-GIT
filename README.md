
Medical Diagnosis Assistant Using RAG and Langchain

## Overview
The Medical Diagnosis Assistant is a system designed to assist healthcare professionals by leveraging Retrieval-Augmented Generation (RAG) and LangChain. The project retrieves medical knowledge and embeds patient medical histories to provide accurate and context-aware diagnosis suggestions.


## Objectives
1. Medical Knowledge Retrieval: Efficiently retrieve medical information relevant to patient symptoms from a knowledge base.
2. Embedding Patient Histories: Represent patient medical histories as dense embeddings for similarity-based retrieval and contextual understanding.
3. RAG-Powered Diagnosis: Use a Retrieval-Augmented Generation (RAG) pipeline to combine retrieved medical knowledge and patient-specific details to suggest potential diagnoses.



## Approach

1. Data Preparation
2. Embedding and Vectorization**
#### a. Converting Data to Documents
Both patient histories and medical knowledge are converted into LangChain `Document` objects, preserving metadata for contextual retrieval.

#### b. Creating Embeddings
A llm(Ollama) is used to generate dense embeddings for documents. These embeddings are stored in a FAISS vector database.

#### c. Storing and Retrieving
The FAISS vector store is saved locally to allow retrieval of similar documents based on queries.


3. RAG Pipeline
#### a. Retriever Setup
The vector store is used to create a retriever that fetches the most relevant documents based on similarity.

#### b. LLM Integration
A large language model (e.g., Llama 3) is integrated to generate diagnosis suggestions by combining patient history with retrieved knowledge.

#### c. Prompt Design
A structured prompt is crafted to guide the LLM in generating accurate and context-aware responses.







