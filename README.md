# 📚 Book Recommendation System (BPR Model)

A production-style collaborative filtering recommendation system built using 
**Bayesian Personalized Ranking (BPR)** and PyTorch.

This project implements an implicit-feedback recommender system trained on user-book interaction data and evaluated using ranking-based metrics.

---

## 🚀 Project Overview

This system:

- Filters sparse users and items
- Splits data per user (leave-one-out strategy)
- Encodes raw IDs into embedding indices
- Trains a BPR model using negative sampling
- Evaluates with ranking metrics
- Provides interactive CLI-style recommendations
- Analyzes dataset sparsity and popularity bias

---

## 🧠 Model Architecture

The model learns:

- User embeddings
- Book embeddings

Prediction score is computed as:

score(u, i) = dot(user_embedding, item_embedding)

Loss Function:
Bayesian Personalized Ranking (BPR Loss)

---

## 📊 Evaluation Metrics

The model is evaluated using:

- **HitRate@5**
- **HitRate@10**
- **NDCG@10**

Example performance:

```
HitRate@5  : 0.4924
HitRate@10 : 0.6698
NDCG@10    : 0.3964
```

These metrics measure ranking quality rather than rating prediction.

---

## 📈 Dataset Analysis

- Users: 35,710  
- Books: 10,000  
- Ratings: 932,940  
- Sparsity: 99.74%

The dataset is highly sparse, which is typical for recommender systems.

---

## 🔍 Popularity Bias Analysis

The project includes:

- Top 10 most popular books
- Top 10 least popular books
- Average ratings per book
- Median ratings per book

This helps analyze popularity skew in recommendations.

---

## 💻 Interactive Recommendation System

```
===== BOOK RECOMMENDER SYSTEM =====
1 - Recommend for Random User
2 - Recommend Similar Books
3 - Exit
```

Features:
- Random user recommendations
- Content-based style similar book retrieval via embedding similarity
- Cold-start handling for filtered books

---

## 🛠 Tech Stack

- Python
- PyTorch
- Pandas
- NumPy

---

## 📂 Project Structure

book_recommender.ipynb # Full pipeline (EDA → Training → Evaluation → CLI)
requirements.txt # Dependencies
.gitignore # Ignored files
README.md # Project documentation


---

## 📌 Key Concepts Demonstrated

- Implicit Feedback Learning
- Negative Sampling
- Ranking-based Evaluation
- Embedding-based Similarity
- Dataset Sparsity Analysis
- Popularity Bias Inspection

---

## 🎯 Purpose

This is a personal machine learning project built to demonstrate:

- Deep understanding of recommender systems
- Implementation of ranking-based models
- Evaluation beyond accuracy
- Professional ML project structuring

---

## 👤 Author

Tilak Raj Giri  
Computer Science Student  
Machine Learning & Recommender Systems Enthusiast
