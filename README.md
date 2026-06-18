# ICU Alarm Fatigue — RAG Q&A System

A domain-specific Retrieval-Augmented Generation (RAG) system built to combat ICU alarm fatigue. 
Clinical staff can query best practices and research on alarm management using natural language. 
Designed with scalability toward patient-level EHR integration and individualized alarm contextualization.

---

## Architecture

1. Healthcare PDF ingestion from GCP Cloud Storage via UnstructuredPDFLoader
2. Text chunking and 768-dimensional embedding generation using Vertex AI text-embedding-005
3. Scalable Vector Search index deployment on Vertex AI
4. RetrievalQA pipeline constructed with LangChain
5. Gemini 2.5 Pro LLM integration with custom prompt engineering for clinical response generation

---

## Tech Stack

- Python
- Google Cloud Platform — Cloud Storage, Vertex AI, Vector Search
- LangChain
- Gemini 2.5 Pro
- Jupyter Notebook

---

## Setup & Usage

1. Set up a GCP project with Vertex AI and Cloud Storage enabled
2. Install dependencies:
```bash
   pip install langchain google-cloud-aiplatform unstructured
```
3. Authenticate with GCP:
```bash
   gcloud auth application-default login
```
4. Run notebooks in sequence:
   - PDF ingestion and embedding generation
   - Vector Search index setup
   - RAG pipeline and Q&A interface

GCP credentials and API keys are not included in this repository.

---

## Future Work

- Integrate hospital-specific EHR data for patient-level alarm contextualization
- Deploy as a REST API for clinical system integration
- Add a lightweight UI for clinical staff query access

---

## Author

Omar Aamir
MS in Advanced Data Analytics (Applied AI) — University of North Texas
