# Lightweight RAG for Academic Papers

This project implements a lightweight Retrieval-Augmented Generation (RAG) system for answering questions over local academic paper PDFs.

The main artifact is the notebook [building_lightweight_rag_for_academic_papers.ipynb](./building_lightweight_rag_for_academic_papers.ipynb), which walks through the full pipeline:
- PDF text extraction
- Page and chunk processing
- Embedding and vector retrieval
- Question answering with citations
- A small ablation study for retrieval settings

## Project Structure

- `data/`: local academic paper PDFs
- `building_lightweight_rag_for_academic_papers.ipynb`: main implementation notebook
- `requirements.txt`: core dependencies
- `requirements-optional.txt`: optional dependency for FAISS
- `DSAI5201_Project_Instructions.pdf`: course project instructions

## Setup

Install the core packages:

```bash
pip install -r requirements.txt
```

Install FAISS if needed:

```bash
pip install -r requirements-optional.txt
```

## How to Run

1. Open the notebook in Jupyter.
2. Make sure the `data/` folder contains the paper PDFs.
3. Run the notebook from top to bottom.

The notebook is designed with fallbacks:
- If `faiss` and `sentence-transformers` are available, it uses a stronger semantic retrieval setup.
- If not, it falls back to a lightweight TF-IDF-based retrieval pipeline so the workflow can still run.

## Output

The notebook can:
- retrieve relevant chunks for a question
- generate an evidence-grounded answer
- show source citations
- compare chunking configurations in a simple evaluation

## Notes

This project is designed for the DSAI5201 applied track topic:
**Building a Lightweight RAG System for Academic Papers**.
