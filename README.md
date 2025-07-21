<h1 align="center">📰 Urdu News Classification using ML 🧠</h1>
<p align="center">
  <b>A Comparative Analysis using Naive Bayes, Logistic Regression & Neural Networks</b><br>
  <i>Multiclass Text Classification on Urdu News Articles from Pakistani Media</i>
</p>

---

## 📌 Project Overview

Urdu is a low-resource language with limited NLP tooling and annotated datasets. This project aims to tackle the problem of **text classification** in Urdu by categorizing news articles into 5 distinct categories:

- 🎬 Entertainment  
- 🌍 World  
- ⚽ Sports  
- 💼 Business  
- 🔬 Science & Technology

To classify articles effectively, three ML models were implemented and compared:

1. Multinomial Naive Bayes
2. Logistic Regression
3. Feedforward Neural Network (PyTorch)

All models achieved high accuracy (>96%), with Neural Networks slightly outperforming the rest.

---

## 🧠 Methodology

### 🗞️ Data Collection

News articles were **scraped** from three major Urdu news platforms:
- Jang
- Express
- Geo

> 📊 **Total Articles:** 1121  
> Distributed across 5 categories (Balanced)

### 🧹 Preprocessing Pipeline

- Urdu stopword removal
- Tokenization and stemming
- Bag-of-Words vectorization via a custom class
- Manual cleaning of non-Urdu characters
- CSV export of cleaned data

---

## 🤖 Models Implemented

### 📌 Model 1: Multinomial Naive Bayes
- BoW + Laplace Smoothing
- Very fast and interpretable
- Strong performance with:
  - **Accuracy**: 96.44%
  - **Macro F1**: 96.54%
- Weakness: Some confusion between similar classes (e.g., World vs Entertainment)

---

### 📌 Model 2: Logistic Regression
- One-vs-All multiclass classifier
- Optimized using Gradient Descent
- Config:
  - Learning Rate: 0.1
  - L2 Reg: 0.01
  - Epochs: 200
- Performance:
  - **Accuracy**: 96.44%
  - **Macro F1**: 96.49%

---

### 📌 Model 3: Neural Network (PyTorch)
- 3 Layers:
  - Dense(128, Sigmoid) → Dense(64, LeakyReLU) → Output(5)
- Optimized with Adam (lr=0.001)
- Training/Validation/Test split: 70/15/15
- Performance:
  - **Accuracy**: 97.04%
  - **Macro F1**: 97%
- Best generalization & lowest misclassifications

---

## 📊 Results Summary

| Model               | Accuracy | Macro F1 | Notes |
|---------------------|----------|----------|-------|
| Naive Bayes         | 96.44%   | 96.54%   | Fast & efficient |
| Logistic Regression | 96.44%   | 96.49%   | Balanced & interpretable |
| Neural Network      | 97.04%   | 97.00%   | Best overall performer |

---

## 📉 Misclassification Insight

Articles in the **"World"** category were most often confused with **"Entertainment"** and **"Sports"**, likely due to overlapping contexts (e.g., celebrity news or international events).

---

## 🧪 Tools & Libraries

- Python
- Numpy (for MNB & LR)
- PyTorch (Neural Net)
- Regex (for Urdu text)
- Matplotlib, Seaborn
- Pandas
- Kaggle Urdu Stopwords
- Sklearn (for splitting only)

---

## ⚠️ Limitations

- **Small Dataset (1121 samples)**: Limits generalization.
- **Linguistic Challenges**: Context-sensitive nature of Urdu made classification difficult.
- **Incomplete stopwords list**: Some irrelevant words not filtered out during preprocessing.

---

## 📌 Key Takeaways

- All models were robust and highly accurate.
- Naive Bayes provides a strong baseline.
- Neural Networks excelled at capturing complex patterns.
- Web scraping + custom preprocessing enables effective Urdu NLP pipelines.

---

## 📈 Future Work

- Increase dataset size via broader scraping or crowdsourcing
- Implement TF-IDF and Word Embeddings
- Explore deeper architectures (e.g., RNNs, Transformers)
- Integrate better Urdu-specific NLP tools

---

## 👨‍💻 Authors

- Muhammad Muiz Farhan  
- Muhammad Ibrahim  
- Abdul Samad – [GitHub](https://github.com/ASamad73)  
- Haider Abbas Virk  
- Hussain Sulaiman Zia  

---

## 📄 Reference

The project report and detailed metrics are documented in the [paper](https://github.com/ASamad73/Urdu_News_Classification-ML/blob/master/19_Report.pdf)

---

⭐️ *If you liked this project, consider giving it a star!*
