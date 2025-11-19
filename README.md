# Session 4 — Applied NLP 

## Paragraph-Level Text Analysis

This repository contains the materials for **Week 4** of *Applied Natural Language Processing*.  
- Slides: see [`slides/`](./slides/) folder  
- Notebooks: see [`notebooks/`](./notebooks/) folder 
---

## Session Outline

In this session, you will learn how to analyze text at the **paragraph level** using various computational measures. These techniques are foundational for modern NLP applications including RAG systems, document chunking, and text quality assessment.

### Learning Objectives

By the end of this session, you will be able to:
- Compute semantic coherence within paragraphs using embeddings
- Measure topic drift between consecutive text segments
- Analyze discourse marker usage patterns
- Assess paragraph compressibility and summarizability
- Classify paragraph functions using prototype-based methods
- Connect classical NLP metrics to modern AI systems (ChatGPT, RAG, etc.)

### Notebooks Overview

**Notebook 1: Paragraph Semantic Coherence**  
- **Focus**: Measuring how well sentences within a paragraph relate to each other
- **Techniques**: MiniLM embeddings, cosine similarity, centroid-based coherence
- **Application**: Quality assessment for RAG chunk selection, identifying well-written text
- **Key Insight**: High coherence = sentences discuss the same topic/idea

**Notebook 2: Topic Drift Between Paragraphs**  
- **Focus**: Detecting topic/scene changes across consecutive paragraphs
- **Techniques**: Paragraph embeddings, inter-paragraph similarity, drift detection
- **Application**: Document segmentation, chapter boundary detection, context window management
- **Key Insight**: Low similarity between paragraphs = major topic shift

**Notebook 3: Discourse Marker Density**  
- **Focus**: Counting transition words and structural signals in text
- **Techniques**: Pattern matching, density calculation, stylistic analysis
- **Application**: Text classification, formality detection, writing style analysis
- **Key Insight**: Marker density reveals writing style (formal vs. narrative)

**Notebook 4: Paragraph–Summary Similarity (Compressibility)**  
- **Focus**: Measuring how well paragraphs can be summarized
- **Techniques**: Extractive summarization, embedding similarity, compressibility scoring
- **Application**: Identifying well-focused paragraphs, optimizing document chunking for AI
- **Key Insight**: High compressibility = clear, focused paragraphs easy to summarize

**Notebook 5: Paragraph Function Classification**  
- **Focus**: Categorizing paragraphs by their narrative/structural role
- **Techniques**: Prototype-based classification, embedding similarity, label assignment
- **Application**: Document structure analysis, content organization, automated tagging
- **Key Insight**: Paragraphs serve different functions (dialogue, action, description, etc.)


### Connection to Modern AI

Each notebook explicitly connects traditional NLP measures to contemporary AI systems:
- **RAG (Retrieval-Augmented Generation)**: How paragraph quality affects retrieval accuracy
- **ChatGPT & LLMs**: How context window management relies on paragraph segmentation
- **Document Chunking**: Best practices for splitting long texts for AI consumption
- **Summarization**: Understanding what makes text easy or hard to compress

### Technical Requirements

- Python 3.11+
- ~2GB free disk space (for MiniLM model)
- 8GB+ RAM recommended

---
## 🚀 Environment Setup

Before starting, please **fork this repository** and create a fresh Python virtual environment.  
All required libraries are listed in `requirements.txt`.

> ⚠️ If you encounter errors during `pip install`, try removing the version pinning for the failing package(s) in `requirements.txt`.  
> On Apple M1/M2 systems you may also need to install additional system packages (the “M1 shizzle”).

---

### macOS / Linux (bash/zsh)

```bash
# Select Python version (if using pyenv)
pyenv local 3.11.3

# Create and activate virtual environment
python -m venv .venv
source .venv/bin/activate

# Upgrade pip and install dependencies
pip install --upgrade pip
pip install -r requirements.txt
```

### Windows (PowerShell)
```bash
# Select Python version (if using pyenv)
pyenv local 3.11.3

# Create and activate virtual environment
python -m venv .venv
.venv\Scripts\Activate.ps1

# Upgrade pip and install dependencies
python -m pip install --upgrade pip
pip install -r requirements.txt
```

### Windows (Git Bash)
```bash
# Select Python version (if using pyenv)
pyenv local 3.11.3

# Create and activate virtual environment
python -m venv .venv
source .venv/Scripts/activate

# Upgrade pip and install dependencies
python -m pip install --upgrade pip
pip install -r requirements.txt
```

You’re now ready to run the session notebooks!

Deactivate the environment when you’re done:
```bash
deactivate
```
