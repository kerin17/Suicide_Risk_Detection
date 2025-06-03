# 🧠 Mental Health & Suicide Risk Detection Using NLP

This project explores the application of Natural Language Processing (NLP) techniques to detect signs of mental illness and assess suicide risk based on Reddit posts. It combines deep learning models and linguistic analysis to provide early warning signals that could support intervention strategies.

> 🛡️ **DISCLAIMER:**  
> The conclusions of this study are derived solely from the datasets used and should not be generalized. This model is **not** a diagnostic tool. It is intended to assist organizations in identifying potentially abnormal behavior online to support broader intervention efforts.

---

## 🎯 Objectives

- Determine whether individuals are at risk of suicide.
- Identify the potential mental illness they may be experiencing.
- Assess associations between types of mental illness and suicide risk.

---

## 📂 Datasets

### 1. **Suicide Watch Dataset**  
- 348,124 Reddit posts (2008–2021)  
- Source: [Kaggle - SuicideWatch subreddit](https://www.kaggle.com/datasets)  
- Labels: `suicide`, `depression`, `non-suicide` (from r/teenagers)

### 2. **Mental Illness Dataset**  
- 52,642 Reddit posts  
- Discusses 7 types of mental illness  
- Source: [Hugging Face API](https://huggingface.co/datasets)

---

## ⚙️ Preprocessing Steps

- Remove null/empty rows and standardize label names
- Clean text (HTML tags, URLs, emojis, contractions)
- Remove stopwords and internet slang (custom list)
- Correct common text formatting and typos
- Normalize text using **spaCy** and **NLTK**

---

## 🧪 Methods & Models

### 🧩 Sentiment Analysis & Topic Modeling  
- Performed on preprocessed text to understand emotional tones and content distribution.

### 📘 Methodology I: GloVe + BiLSTM  
- Embedding posts with **GloVe**
- Classification using **Bidirectional LSTM**

### 📗 Methodology II: DistilBERT  
- Fine-tuned **DistilBERT** for embedding and classification
- Predicts mental illness and suicide risk probabilities

### 🔁 Combined Modeling Strategy  
- Step 1: Feed text to DistilBERT to identify mental illness  
- Step 2: Use same text to assess suicide risk probability  
- Results support multi-stage intervention modeling

---

## 🔍 Key Insights

- NLP can effectively identify language patterns associated with mental health struggles.
- Combining illness classification with suicide risk prediction allows for a more nuanced and targeted detection model.
- Such models could support mental health professionals in early screening and triage efforts.

---

## ⚠️ Limitations

- **Subreddit Bias**: Labels are based on subreddit sources which may not represent real diagnoses.
- **Cultural Variability**: Sarcasm, slang, and linguistic nuances affect generalizability.
- **Risk of Misclassification**: False negatives or positives could have serious implications in real-world use.

---

## 📌 Future Work

- Incorporate explainability tools (e.g., SHAP) for model transparency.
- Explore multilingual support and cultural adaptation.
- Collaborate with mental health experts to refine labeling and interpretation.

---

## 📁 Repository Contents

- `notebooks/` – Jupyter notebooks with full code  
- `data/` – Not included due to size; available via external links  
- `models/` – Trained model files
- `README.md` – Project overview  

---

