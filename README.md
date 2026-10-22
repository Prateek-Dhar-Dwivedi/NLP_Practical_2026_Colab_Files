# 📚 Natural Language Processing (NLP) Practicals — 2026

A comprehensive repository of interactive Google Colab notebooks covering fundamental to intermediate Natural Language Processing (NLP) practicals, pipelines, evaluations, and decision systems.

---

## 📌 Repository Overview

This repository contains hands-on practical assignments and mini-projects implemented with clean code, structured evaluation, and inline visualizations. Every notebook is self-contained and ready to execute in Google Colab.

| Practical | Project Title | Dataset | Key Techniques & Tools | Colab Link |
| :--- | :--- | :--- | :--- | :---: |
| **Practical 01** | **CorpusLens** — NLP Corpus Explorer | NLTK Gutenberg (`carroll-alice.txt`, Shakespeare, etc.) | Lexical diversity, vocabulary analysis, frequency distribution, word cloud, N-grams | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Prateek-Dhar-Dwivedi/NLP_Practical_2026_Colab_Files/blob/main/Practical_01_NLP_CORPUSLENS_NLP_Corpus_Explorer.ipynb) |
| **Practical 02** | **Smart NLP Preprocessing & Analyzer** | User Input / Raw English Corpus | Sentence/Word Tokenization, Regex Cleaning, Stopword Removal, Stemming vs. Lemmatization, POS Tagging, spaCy | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Prateek-Dhar-Dwivedi/NLP_Practical_2026_Colab_Files/blob/main/Practical_02_NLP_Smart_NLP_Text_Preprocessing_Analyzer.ipynb) |
| **Practical 03** | **NewsRoute** — Explainable Post Routing | 20 Newsgroups (~18k posts) | BoW vs. TF-IDF (1–2 grams), Logistic Regression, Confidence-based Abstention, Cosine Retrieval (Precision@5, MRR@10) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Prateek-Dhar-Dwivedi/NLP_Practical_2026_Colab_Files/blob/main/Practical_03_NewsRoute_Explainable_Post_Routing.ipynb) |
| **Practical 04** | **SpamGuard** — Text Dataset Evaluation Lab | UCI SMS Spam Collection (5,572 messages) | Stratified Train/Test Split, Preprocessing Data Leakage Prevention, Sklearn Pipelines, 5-Fold Stratified CV, Multinomial Naive Bayes | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Prateek-Dhar-Dwivedi/NLP_Practical_2026_Colab_Files/blob/main/Practical_4_SpamGuard_Dataset_Evaluation.ipynb) |

---

## 🔬 Practical Details

### 1. [Practical 01: CorpusLens — NLP Corpus Explorer](Practical_01_NLP_CORPUSLENS_NLP_Corpus_Explorer.ipynb)
* **Objective:** Understand how to load, inspect, clean, and profile raw text corpora.
* **Core Topics:**
  * Gutenberg corpus exploration via NLTK.
  * Quantitative lexical metrics: Character count, word count, sentence count, Type-Token Ratio (TTR / Lexical Diversity), and average word/sentence lengths.
  * Frequency distributions (`FreqDist`), stopword removal analysis, and WordCloud visualizations.
  * Cross-corpus comparison across multiple literary works.

---

### 2. [Practical 02: Smart NLP Text Preprocessing & Analyzer](Practical_02_NLP_Smart_NLP_Text_Preprocessing_Analyzer.ipynb)
* **Objective:** Build a complete, modular, end-to-end preprocessing pipeline for raw unstructured text.
* **Core Topics:**
  * Sentence segmentation and word tokenization (`nltk.tokenize`).
  * Text normalization (lowercasing, punctuation stripping, regex cleaning).
  * Stopword filtering with information-retention analysis.
  * Morphological normalization: Direct side-by-side benchmarking of **Stemming** (Porter, Lancaster) vs. **Lemmatization** (WordNet, spaCy).
  * Part-of-Speech (POS) tagging and dependency parsing with spaCy (`en_core_web_sm`).
  * Before-and-after text compression and vocabulary statistics.

---

### 3. [Practical 03: NewsRoute — Explainable Post Routing with Abstention](Practical_03_NewsRoute_Explainable_Post_Routing.ipynb)
* **Objective:** Transition from toy NLP representations to an enterprise-grade probabilistic triage and routing system.
* **Core Topics:**
  * Feature extraction comparison: Bag-of-Words vs. TF-IDF unigrams vs. TF-IDF unigram+bigram.
  * Probabilistic text classification using multi-class Logistic Regression.
  * **Selective Classification (Abstention Gate):** Routes high-confidence predictions automatically while escalating low-confidence cases to a human review queue.
  * **Similar-Case Retrieval:** Uses cosine similarity over TF-IDF vectors to retrieve past similar tickets/posts, evaluated using Information Retrieval metrics (**Precision@5** and **MRR@10**).
  * **Explainability:** Term-contribution analysis to interpret which tokens influenced the routing outcome.

---

### 4. [Practical 04: SpamGuard — Text Dataset Evaluation Lab](Practical_4_SpamGuard_Dataset_Evaluation.ipynb)
* **Objective:** Master proper evaluation methodology, cross-validation, and avoid data leakage in NLP classifiers.
* **Core Topics:**
  * Downloading and inspecting the UCI SMS Spam Collection dataset (`ham` vs. `spam`).
  * Handling real-world severe class imbalance with **Stratified Train/Test Splitting**.
  * Demonstrating and preventing **Data Leakage** during text vectorization (`TfidfVectorizer`).
  * Encapsulating vectorizers and models inside `sklearn.pipeline.Pipeline`.
  * **5-Fold Stratified Cross-Validation** using `StratifiedKFold` and `cross_validate`.
  * Comprehensive classification metrics: Precision, Recall, Macro/Weighted F1-Score, and normalized Confusion Matrices.
  * Real-time interactive inference on custom user-provided SMS messages.

---

## 🛠️ Tech Stack & Requirements

The notebooks are designed to run smoothly on Google Colab with standard Python 3 runtime. The key libraries utilized include:

* **NLP & Linguistics:** `nltk`, `spacy` (`en_core_web_sm`)
* **Machine Learning & Evaluation:** `scikit-learn`
* **Data Manipulation:** `pandas`, `numpy`
* **Visualization:** `matplotlib`, `seaborn`, `wordcloud`

---

## 🚀 How to Run

1. Click any **Open In Colab** badge in the table above, or download the `.ipynb` files to your local environment.
2. In Google Colab, select **Runtime → Run all** to execute all blocks in sequence.
3. Replace the input strings in the designated interactive sections to test custom paragraphs or SMS messages.