# 🧠 Project DOOM (Mark I): Offline Memory Core

![Python](https://img.shields.io/badge/Python-3.9%2B-blue)
![ChromaDB](https://img.shields.io/badge/ChromaDB-Vector_Storage-orange)
![Hardware](https://img.shields.io/badge/Optimized_for-Apple_Silicon_(M1)-lightgrey)
![Status](https://img.shields.io/badge/Status-Active_Development-brightgreen)

## 📌 Overview
This repository contains the **Long-Term Memory Engine** for Project DOOM (Mark I) — a 100% offline, edge-optimized Retrieval-Augmented Generation (RAG) architecture. 

Instead of relying on heavy abstractions or cloud APIs, this system utilizes pure Python, pure Math (Cosine Similarity), and **ChromaDB** to index and retrieve high-dimensional text embeddings entirely locally on Apple Silicon. 

## 🏗️ Core Architecture
The Memory Core is designed to be lightweight and fast, executing semantic searches in milliseconds without bottlenecking the system RAM.

1. **Local Embeddings:** Text chunks are transformed into vectors using local inference (via Ollama).
2. **Persistent Vector Storage:** Vectors are not held in volatile RAM. They are persistently written to disk using ChromaDB's SQLite-backed storage.
3. **HNSW Indexing:** Utilizes the Hierarchical Navigable Small World (HNSW) algorithm for lightning-fast nearest-neighbor searches.
4. **Semantic Retrieval:** Replaces traditional keyword matching with deep semantic understanding (e.g., matching "shrimp" to "prawns").

## ⚙️ Setup & Installation

### 1. Prerequisites
Ensure you have Python installed and a local LLM runner (like Ollama) configured.
```bash
pip install chromadb numpy requests
