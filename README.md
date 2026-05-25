# RAG Pipeline

A minimal, state-of-the-art hybrid RAG pipeline designed for parsing and querying complex documents (like reports/PDFs) on Google Colab using Google Drive.

## Repository Structure

- **[`PREPROCCES.ipynb`](colab_pdf_parse_clean.ipynb)**: PDF parser converting documents into RAG-friendly cleaned Markdown.
  - Supports **Docling** (accurate layout/tables) and **PyMuPDF4LLM** (ultra-fast text conversion).
- **[`RAG.ipynb`](RAG.ipynb)**: Complete Hybrid RAG pipeline.
  - **Architecture**: BM25 (keyword) + FAISS (vector) &rarr; Reciprocal Rank Fusion (RRF) &rarr; Cross-Encoder Reranker &rarr; Parent-Document Expansion &rarr; OpenRouter LLM.

## Quick Start

1. **Parse PDFs**: Open `PREPROCCES.ipynb` in Google Colab, upload your PDFs to Google Drive, and run the cells to produce clean markdown files.
2. **Query the RAG**: Open `RAG.ipynb` in Colab, configure your OpenRouter API key in the **CONFIG** cell, and run the pipeline to start querying your documents with SOTA accuracy.
