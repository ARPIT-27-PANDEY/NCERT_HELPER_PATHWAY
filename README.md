# NCERT Helper Question Answering System

The **NCERT Helper Question Answering System** is an AI-powered application designed to assist students with their studies by providing fast, context-aware answers to questions from uploaded educational documents.

The system uses a **Retrieval-Augmented Generation (RAG)** approach to retrieve relevant information from uploaded documents and generate contextually appropriate answers. The core RAG pipeline is implemented using **Pathway**, with **Mistral LLM** used for response generation and **Sentence-Transformers** used for semantic retrieval and embeddings.

The application supports multiple document sources and is designed for real-time document processing and question answering.

The application is **containerized using Docker**, ensuring a reproducible and deployable environment. Dependencies are managed through `requirements.txt` and installed automatically during the Docker build process.

Additional **Gemini API** and **Hugging Face API** components are included for experimentation and supporting parts of the RAG pipeline.

---

## VIDEO DEMO OF THE APP

https://drive.google.com/file/d/1kYhPRoR28ofsfLW9dG4DKPu8jFuR-Fm2/view?usp=sharing

---

## Business Usage

The NCERT Helper Question Answering System is designed to help students through:

- **Personalized Learning:** Provides context-aware answers to questions based on uploaded NCERT and educational documents.
- **Efficiency:** Enables students to retrieve relevant information quickly instead of manually searching through multiple documents.
- **Scalability:** Can be extended to support a wide range of subjects, grades, and educational resources.

For educational institutions and ed-tech companies, the system can be integrated as:

- **A digital assistant for learning apps**, providing immediate answers to NCERT curriculum queries.
- **A homework assistant**, helping students solve questions without requiring constant teacher intervention.
- **An AI tutor**, enabling students to learn at their own pace through interactive question answering.

### E-Commerce Adaptation

The same RAG architecture can be adapted to other domain-specific applications, including **e-commerce customer-support chatbots**.

For example, companies such as **Epto** can use the system to provide real-time responses to customer queries using their internal documents, product information, FAQs, and support resources, with the potential to substantially reduce manual customer-support effort.

---

## Features

- **RAG Pipeline:** Uses Retrieval-Augmented Generation to combine semantic document retrieval with LLM-based response generation.
- **Pathway Integration:** Provides the underlying dataflow pipeline for document ingestion, processing, retrieval, and real-time updates.
- **Mistral LLM:** Used as the primary language model for generating human-readable answers from retrieved context.
- **Sentence-Transformers:** Generates semantic embeddings used for identifying relevant document content.
- **Gemini API:** Included as an additional LLM/API component for experimentation and supporting functionality.
- **Hugging Face API:** Used for embedding and retrieval-related components.
- **Streamlit UI:** Provides a simple and interactive chatbot interface for submitting queries and viewing generated responses.
- **Docker Deployment:** Containerizes the application and its dependencies for reproducible deployment across environments.
- **Multi-Document Support:** Supports more than **50 files** and **10+ file types**, including PDFs, documents, links, and text files.
- **Domain Optimization:** The pipeline can be adapted and optimized for domain-specific knowledge bases and pre-loaded datasets.

---

## Features of NCERT Helper Question Answering System 📚

### Personalized Learning Assistance
Provides tailored answers to students' specific NCERT questions, supporting both general queries and more complex topics.

### User-Friendly Interface
Powered by **Streamlit**, providing simple navigation and interactive chatbot-based question answering.

### Pathway Integration
Utilizes **Pathway** for real-time data processing and context retrieval, allowing the system to efficiently process changing document sources without requiring a traditional external database.

### Real-Time Responses
The system retrieves relevant information from uploaded documents and generates context-aware answers for user queries.

### Multi-File Processing
The application can process **50+ files** at a time across **10+ file types**, including PDFs, documents, links, and text files.

### Cross-Platform Deployment
The application is fully containerized using **Docker**, making deployment and dependency management consistent across environments.

---

## Tech Stack

- **Pathway**: Version >11.0
- **Mistral LLM**: Primary LLM for response generation
- **Sentence-Transformers**: Semantic embedding and retrieval
- **Gemini API**: Additional LLM/API component
- **Hugging Face API**: Embedding and retrieval-related components
- **Streamlit**: Frontend and chatbot interface
- **Docker**: Containerization and deployment

---

## System Architecture

The overall RAG workflow can be summarized as:

```text
                    ┌─────────────────────┐
                    │   Uploaded Files    │
                    │ PDF / Docs / Links  │
                    │      / Text         │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │ Document Processing │
                    │      Pathway        │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │ Text Chunking &     │
                    │ Embedding Generation│
                    │ Sentence-Transformers│
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │ Semantic Retrieval  │
                    │ Relevant Chunks     │
                    └──────────┬──────────┘
                               │
                    ┌──────────▼──────────┐
                    │   Query + Context   │
                    │   Prompt Formation  │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │     Mistral LLM     │
                    │ Answer Generation   │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │    Streamlit UI     │
                    │ Human-readable      │
                    │      Answer         │
                    └─────────────────────┘
