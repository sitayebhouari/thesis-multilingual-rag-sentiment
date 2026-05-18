# 🎓 Multilingual RAG + Economic Sentiment Analysis for Macroeconomic Forecasting

> **Master's Thesis** — ENSSEA | Si Tayeb Houari | 2025–2026  
> *Hybrid NLP Framework for Multilingual Economic Document Analysis and Macroeconomic Forecasting*

---

## 📌 Overview

This repository contains all resources for a **Master's thesis** that proposes and evaluates a **hybrid multilingual NLP framework** combining:

- Retrieval-Augmented Generation (RAG) with FAISS + BM25 + CrossEncoder reranking
- Multilingual Ensemble Sentiment Analysis (FinBERT + XLM-RoBERTa + Economic Lexicon)
- Economic Forecasting via SARIMAX augmented with Sentiment Index
- Statistical Validation (Granger causality, Diebold-Mariano test)

The system is designed specifically for **Arabic, French, and English** economic documents — particularly **Bank of Algeria** and **IMF Annual Reports** (2000–2025).

---

## 🏗️ Repository Structure

```
thesis-multilingual-rag-sentiment/
│
├── 📁 notebooks/               # All Jupyter notebooks
│   ├── thesis_main.ipynb       # Core analysis & experiments
│   ├── sentiment_analysis.ipynb
│   └── forecasting.ipynb
│
├── 📁 app/                     # Gradio web application
│   ├── app.py                  # Main application file
│   └── requirements.txt
│
├── 📁 data/                    # Dataset links & samples
│   └── data_sources.md
│
├── 📁 evaluation/              # RAG evaluation queries & gold labels
│   ├── rag_eval_queries.csv
│   └── gold_labels.csv
│
├── 📁 figures/                 # Generated charts and visualizations
│   └── yearly_sentiment_index_line.png
│
├── 📁 appendices/              # Thesis appendix materials
│   └── appendix_e_links.md
│
└── README.md
```

---

## 🔬 Research Questions

1. Can multilingual ensemble sentiment analysis reliably extract economic signals from Arabic, French, and English macroeconomic reports?
2. Does integrating a sentiment index as an exogenous variable in SARIMAX improve forecasting accuracy over baseline ARIMA?
3. Does a hybrid RAG pipeline (FAISS + BM25 + CrossEncoder) outperform sparse-only retrieval on multilingual economic documents?

---

## 🧠 Models & Technologies

| Component | Model / Library |
|-----------|----------------|
| Sentence Embeddings | `sentence-transformers/paraphrase-multilingual-MiniLM-L12-v2` |
| Cross-encoder Reranking | `cross-encoder/ms-marco-MiniLM-L-6-v2` |
| Sentiment (General) | `cardiffnlp/twitter-xlm-roberta-base-sentiment` |
| Sentiment (Economic) | Fine-tuned FinBERT + Economic Lexicon |
| LLM Backend | `llama-3.3-70b` via Groq API |
| Vector Search | FAISS (CPU) |
| Sparse Retrieval | BM25 (custom implementation) |
| Forecasting | ARIMA(1,1,1) vs SARIMAX + Ensemble Sentiment |
| Statistical Tests | Granger Causality, Diebold-Mariano |

---

## 📊 Key Results

### Yearly Ensemble Sentiment Index — Algeria (2000–2025)

![Sentiment Index](figures/yearly_sentiment_index_line.png)

Key economic events are clearly captured:
- 📈 **2004–2005**: Oil boom — positive sentiment peak
- 📉 **2008–2009**: Global financial crisis — sharp drop
- 📈 **2011–2012**: Oil boom recovery — highest sentiment
- 📉 **2014–2016**: Oil price shock — highly negative
- 📉 **2020**: COVID-19 — negative shock
- 📈 **2022–2025**: Recovery trend

### Forecasting Performance

| Model | RMSE | MAE | MAPE |
|-------|------|-----|------|
| ARIMA(1,1,1) | — | — | — |
| SARIMAX + Ensemble Sentiment | — | — | — |

*See notebooks for full results.*

---

## 🔗 Project Resources

| Resource | Link |
|----------|------|
| 🤗 Live Demo (HuggingFace Space) | [sitayeb/xlmr](https://huggingface.co/spaces/sitayeb/xlmr) |
| 📓 Notebooks Repository | *(link to thesis-notebooks repo)* |
| 📊 LABR Arabic Sentiment Dataset | [mohamedadaly/labr](https://huggingface.co/datasets/mohamedadaly/labr) |
| 📊 Sentiment140 Dataset | [stanfordnlp/sentiment140](https://huggingface.co/datasets/stanfordnlp/sentiment140) |
| 🌐 App Source Code | *(link to rag-sentiment-app repo)* |
| 📂 Evaluation Data | *(link to thesis-evaluation-data repo)* |

---

## 🚀 Quick Start

```bash
git clone https://github.com/YOUR_USERNAME/thesis-multilingual-rag-sentiment.git
cd thesis-multilingual-rag-sentiment
pip install -r app/requirements.txt
```

---

## 📄 Citation

If you use this work, please cite:

```bibtex
@mastersthesis{sitayeb2026multilingual,
  title     = {Hybrid Multilingual RAG Framework for Economic Sentiment Analysis and Macroeconomic Forecasting},
  author    = {Si Tayeb Houari},
  school    = {ENSSEA},
  year      = {2026}
}
```

---

## 📬 Contact

**Si Tayeb Houari** — ENSSEA, Algeria  
Master's in [Your Specialization] | 2025–2026

---

*© 2026 Si Tayeb Houari — ENSSEA Master's Thesis*
