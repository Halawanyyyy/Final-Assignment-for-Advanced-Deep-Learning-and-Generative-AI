# Final-Assignment-for-Advanced-Deep-Learning-and-Generative-AI


# 🔍 Hybrid AI/Data Science Q&A System

This project implements a state-of-the-art hybrid question answering system that combines lexical (BM25) and semantic (MiniLM) retrieval with FLAN-T5 answer generation, designed specifically for AI and Data Science domains.

![System Architecture](https://i.imgur.com/r3JZg1n.png)

## ✨ Features
- **Hybrid Retrieval Engine**: Combines BM25 keyword matching with MiniLM-L6 semantic embeddings
- **Reciprocal Rank Fusion**: Advanced algorithm to merge results from different retrieval methods
- **RAG Answer Generation**: FLAN-T5 transformer generates answers using retrieved context
- **Citation Support**: Answers include inline references to original sources
- **Gradio Web Interface**: User-friendly interface for live Q&A
- **Evaluation Framework**: Benchmarks using MAP@10, MRR@10, and NDCG@10 metrics

## 📊 Performance Comparison
| Metric     | BM25   | Semantic | Hybrid |
|------------|--------|----------|--------|
| **MAP@10** | 0.2722 | 0.7333   | 0.7500 |
| **MRR@10** | 0.2722 | 0.7333   | 0.7500 |
| **NDCG@10**| 0.3987 | 0.7974   | 0.8123 |

## ⚙️ System Components
1. **Retrieval Modules**:
   - `search_bm25()`: Traditional keyword-based search
   - `search_semantic()`: Dense vector similarity search
   - `hybrid_search()`: Combined RRF ranking (BM25 + Semantic)

2. **Answer Generation**:
   - `generate_answer_rag_hf()`: Generates answers with citations
   - `generate_answer_hf()`: Standard context-based generation

3. **Evaluation Framework**:
   - Ground truth Q&A pairs
   - ranx metrics evaluation
   - Performance comparison

## 🚀 Installation
1. Clone repository:
```bash
git clone https://github.com/yourusername/ai-qa-system.git
cd ai-qa-system
