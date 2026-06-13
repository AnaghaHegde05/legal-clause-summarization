# Hybrid GRU-Based Pointer-Generator Network for Legal Clause Summarization

> Deep Learning-based Legal Text Summarization using Bidirectional GRU, Pointer-Generator Networks, Coverage Attention, and Beam Search Decoding.

## Overview

Legal documents are often lengthy, complex, and difficult to analyze manually. This project presents an abstractive legal text summarization system designed to generate concise and coherent summaries of legal clauses and legislative documents.

The proposed architecture combines a Bidirectional GRU Encoder, Pointer-Generator Network, Coverage Attention Mechanism, and Beam Search Decoding to improve factual consistency, handle out-of-vocabulary legal terminology, and reduce repetitive text generation.

This work was developed as a research project and was presented at the IEEE International Conference on Innovative Trends in Communication and Computer Technology (I3CTCON 2026).

---

## Key Features

* Bidirectional GRU Encoder for contextual understanding
* Pointer-Generator Network for copying important legal terms
* Coverage Attention Mechanism to reduce repetition
* Coverage Loss Annealing during training
* Beam Search Decoding for improved summary quality
* ROUGE-based evaluation framework
* BillSum legal dataset integration
* End-to-end legal clause summarization pipeline

---

## Dataset

### BillSum Dataset

BillSum is a publicly available corpus of United States Congressional and California state legislative bills paired with expert-written summaries.

| Dataset Split | Samples |
| ------------- | ------- |
| Training Set  | 8,000   |
| Test Set      | 500     |

The dataset contains long-form legal documents requiring abstractive summarization while preserving critical legal information.

---

## System Architecture

```text
Input Legal Document
        │
        ▼
Bidirectional GRU Encoder
        │
        ▼
Coverage Attention Layer
        │
        ▼
Pointer-Generator Decoder
        │
        ▼
Beam Search Decoding
        │
        ▼
Generated Legal Summary
```

---

## Core Components

### Bidirectional GRU Encoder

Processes input text in both forward and backward directions to capture long-range contextual dependencies.

### Coverage Attention

Maintains a coverage vector that tracks previously attended words, significantly reducing repetitive phrase generation.

### Pointer-Generator Network

Combines two mechanisms:

* Vocabulary-based word generation
* Direct copying of important source tokens

This is particularly useful for handling legal terminology and rare entities.

### Beam Search Decoding

Generates higher-quality summaries by exploring multiple candidate sequences during inference.

---

## Technologies Used

| Category                   | Tools         |
| -------------------------- | ------------- |
| Programming Language       | Python        |
| Deep Learning              | PyTorch       |
| Data Processing            | Pandas, NumPy |
| NLP                        | NLTK          |
| Evaluation                 | ROUGE Score   |
| Visualization              | Matplotlib    |
| Machine Learning Utilities | Scikit-learn  |

---

## Training Configuration

| Parameter         | Configuration            |
| ----------------- | ------------------------ |
| Encoder           | Bidirectional GRU        |
| Decoder           | Pointer-Generator GRU    |
| Attention         | Coverage Attention       |
| Decoding Strategy | Beam Search              |
| Loss Function     | NLL Loss + Coverage Loss |
| Framework         | PyTorch                  |

---

## Results

Performance was evaluated using standard ROUGE metrics.

| Metric  | Score |
| ------- | ----- |
| ROUGE-1 | 0.504 |
| ROUGE-2 | 0.285 |
| ROUGE-L | 0.363 |

### Key Observations

* Coverage attention reduced repetitive phrase generation.
* Pointer-generator improved handling of legal terminology.
* Beam search produced more coherent summaries compared to greedy decoding.
* The model generated concise summaries while preserving important legal information.

---

## Repository Structure

```text
legal-clause-summarization/
│
├── legal_summarization.ipynb
├── requirements.txt
├── README.md
├── billsum_train.csv
└── billsum_test.csv

```

---

## Installation

```bash
git clone https://github.com/AnaghaHegde05/legal-clause-summarization.git

cd legal-clause-summarization

pip install -r requirements.txt
```

---

## Running the Project

```bash
jupyter notebook legal_summarization.ipynb
```

Run the notebook sequentially to:

1. Load and preprocess the BillSum dataset
2. Train the Pointer-Generator model
3. Evaluate using ROUGE metrics
4. Generate summaries for unseen legal documents

---

## Research Contribution

This work proposes a hybrid GRU-based Pointer-Generator architecture enhanced with Coverage Attention for legal clause summarization.

Major contributions include:

* Reducing repetitive text generation through coverage mechanisms
* Improving handling of legal terminology using pointer networks
* Enhancing summary coherence through beam search decoding
* Evaluating performance on a real-world legal summarization dataset

---

## Future Work

* Transformer-based legal summarization models
* LegalBERT integration
* Multi-document legal summarization
* FastAPI deployment for real-time inference
* Web-based summarization interface
* Explainable AI techniques for summary interpretation

---

## Publication

**Hybrid GRU-Based Pointer-Generator Model for Legal Clause-Level Summarization**

Presented at:

**IEEE International Conference on Innovative Trends in Communication and Computer Technology (I3CTCON 2026)**

---

## Author

**Anagha Hegde**

B.E. Computer Science Engineering
KLE Technological University

Interests:

* Artificial Intelligence
* Machine Learning
* Natural Language Processing
* Intelligent Systems
