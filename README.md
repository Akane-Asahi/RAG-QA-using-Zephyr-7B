# RAG-QA-using-Zephyr-7B

This is an Islamic RAG QA System using Zephyr-7B and SBERT demonstrates a lightweight Retrieval-Augmented Generation (RAG) pipeline built with:

- **Sentence Transformers** for semantic search
- **Zephyr-7B Alpha** for faith-aware answer generation
- A custom Islamic knowledge base (CSV) containing Quran, Hadith, and scholarly texts with references

The system is designed to provide respectful and concise answers to Islamic questions by retrieving relevant texts and generating responses grounded in those sources.

## Run it on Google Colab
<a href="https://colab.research.google.com/drive/1CazCpZqiw5F3hOjabsA_HIqfhHxK0OEi?usp=sharing"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab to run instantly in the cloud (no installation needed) " style="height:28px; vertical-align:middle; margin-right:5px"></a>  
1. Click above link to run this project with a single click.  
2. Click Run All button to run
3. Run it multimple times to check how the simulation is performing.

## Project Vision & Roadmap

### Why This Project Matters

Many Muslims today seek quick and authentic answers to religious and ethical questions. Unfortunately, most general-purpose AI models either hallucinate, omit references, or fail to align with Islamic principles.

This project addresses that gap by:

- Combining classical Islamic sources with modern NLP
- Grounding answers in retrieved religious texts
- Providing a respectful interface for faith-based dialogue

It lays the foundation for safe, transparent, and trustworthy AI tools for Islamic knowledge access.

---

### Islamic AI Scholar Roadmap

This is **Project 4** in the **AI Scholar's Islamic NLP/AI Series**, each project building toward robust, ethical, and faith-aligned AI systems.

| Project No. | Title                                       | Focus Area                                       |
|-------------|---------------------------------------------|--------------------------------------------------|
| 1           | Islamic Intent Classifier                   | Dialogue Act Classification (prayer, fatwa, etc.) |
| 2           | Quran + Hadith Semantic Search              | Dense retrieval with sentence embeddings         |
| 3           | FaithAgent: Islamic RL Simulation           | Reinforcement Learning with ethical modeling     |
| 4           | **Islamic RAG QA (this project)**           | Retrieval-Augmented Generation for question answering |
| 5           | Faith-Conscious Dialogue Agent *(Upcoming)* | Aligned Islamic chatbot with fine-tuning         |

---

## 🔧 Tech Stack

- `sentence-transformers` for SBERT-based semantic search
- `transformers` for loading Zephyr-7B model
- `accelerate` and `bitsandbytes` (optional) for model optimization
- `pandas` for CSV handling
- `Google Colab` as a rapid prototyping environment

---

## 📂 File Structure
```
├── rag_knowledge_base_large.csv # Islamic knowledge base with text and source columns  
├── islamic_rag_qa_colab.ipynb # Colab notebook for running the QA pipeline  
```

## How It Works

1. **Upload Knowledge Base**  
   Upload a CSV containing Islamic texts and sources.

2. **Corpus Embedding**  
   Encode all entries using `all-MiniLM-L6-v2` via SentenceTransformers.

3. **Semantic Search**  
   Perform cosine similarity to find top-k relevant texts for each question.

4. **Contextual Answering**  
   Construct a prompt with retrieved context and generate an answer using Zephyr-7B.
