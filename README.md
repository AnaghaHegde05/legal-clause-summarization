# Hybrid GRU-Based Pointer-Generator Network for Legal Clause Summarization

## Overview

Legal documents are often lengthy and difficult to analyze efficiently. This project presents a deep learning-based legal text summarization system that automatically generates concise summaries of legal clauses and legislative documents.

The model combines a Bidirectional GRU Encoder, Pointer-Generator Network, Coverage Attention Mechanism, and Advanced Beam Search Decoding to improve summary quality while reducing repetition.

This work was developed as part of a research project and was presented at an IEEE International Conference (I3CTCON 2026).

---

## Features

* Bidirectional GRU Encoder
* Pointer-Generator Decoder
* Coverage Attention Mechanism
* Coverage Loss Annealing
* Advanced Beam Search Decoding
* Repetition Reduction using Coverage Vectors
* ROUGE-based Evaluation
* BillSum Legal Dataset Support

---

## Dataset

### BillSum Dataset

BillSum is a corpus of U.S. Congressional and California state bills paired with human-written summaries.

Dataset Split:

| Dataset  | Samples |
| -------- | ------- |
| Training | 8,000   |
| Testing  | 500     |

---

## Model Architecture

Input Legal Document
↓
Bidirectional GRU Encoder
↓
Coverage Attention
↓
Pointer-Generator Decoder
↓
Beam Search Decoding
↓
Generated Summary

### Key Components

#### Bidirectional GRU Encoder

Captures contextual information from both past and future tokens.

#### Coverage Attention

Maintains a coverage vector that tracks previously attended words and reduces repeated phrases during generation.

#### Pointer-Generator Network

Allows the model to:

* Generate words from vocabulary
* Copy important words directly from the source document

#### Beam Search

Generates higher-quality summaries by exploring multiple decoding paths simultaneously.

---

## Technologies Used

* Python
* PyTorch
* NumPy
* Pandas
* NLTK
* ROUGE Score
* Matplotlib
* Scikit-learn

---

## Training Configuration

| Parameter     | Value                    |
| ------------- | ------------------------ |
| Encoder       | Bidirectional GRU        |
| Decoder       | Pointer-Generator GRU    |
| Attention     | Coverage Attention       |
| Decoding      | Beam Search              |
| Loss Function | NLL Loss + Coverage Loss |
| Framework     | PyTorch                  |

---

## Results

Evaluation was performed using ROUGE metrics.

| Metric  | Score |
| ------- | ----- |
| ROUGE-1 | 0.504 |
| ROUGE-2 | 0.285 |
| ROUGE-L | 0.363 |

The coverage mechanism significantly reduced repetition while preserving important legal information.

---

## Project Structure

```text
├── billsum_train.csv
├── billsum_test.csv
├── legal_summarization.ipynb
├── best_model_pgn_coverage_advanced.pt
├── requirements.txt
└── README.md
```

---

## Installation

```bash
git clone https://github.com/yourusername/legal-clause-summarization.git

cd legal-clause-summarization

pip install -r requirements.txt
```

---

## Run the Project

```bash
jupyter notebook legal_summarization.ipynb
```

Train the model and generate summaries using the notebook.

---

## Research Contribution

Developed a hybrid GRU-based Pointer-Generator architecture with coverage attention for legal clause summarization. The work focused on reducing repetition, improving summary coherence, and generating concise legal summaries through advanced decoding strategies.

---

## Future Improvements

* Transformer-based legal summarization
* Domain-specific legal language modeling
* Multi-document summarization
* Deployment using FastAPI
* Interactive summarization web interface

---

## Author

Anagha Hegde

B.E. Computer Science Engineering
KLE Technological University

---

## Publication

Hybrid GRU-Based Pointer-Generator Model for Legal Clause-Level Summarization

Presented at IEEE International Conference on Innovative Trends in Communication and Computer Technology (I3CTCON 2026).
