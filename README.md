# 🎵 Music Recommendation Engine – End-to-End Data Science Pipeline

An end-to-end **content-driven music recommendation system** built using Spotify audio features.  
This project demonstrates how real-world recommendation systems can be designed, evaluated, and scaled using **audio content alone**, addressing challenges such as **cold start**, **diversity**, and **personalization**.

---

## 📌 Project Overview

Modern music platforms host millions of tracks, making discovery a challenging problem.  
This project builds a **music recommendation engine** that:

- Learns similarity from audio features
- Groups songs into meaningful musical clusters
- Balances relevance and discovery using a **hybrid recommendation approach**
- Performs well even for **low-popularity and unseen tracks**

The system is designed as a realistic prototype inspired by production recommender pipelines used in music streaming platforms.

---

## 🧠 Recommendation Approaches Implemented

### 1️⃣ Content-Based Filtering
- Uses **cosine similarity** on normalized audio features
- Recommends tracks that sound similar to a given song
- Naturally handles **cold-start items**

### 2️⃣ Clustering-Based Recommendation
- Groups songs using **K-Means clustering**
- Recommends popular tracks from the same musical cluster
- Improves scalability and diversity

### 3️⃣ Hybrid Recommendation System
- Combines:
  - **60% content similarity**
  - **40% cluster membership**
- Balances **accuracy and exploration**
- Mimics real-world production recommender systems

### 4️⃣ Genre-Filtered Recommendation
- Restricts recommendations to a specific genre
- Useful for playlist generation and genre-specific discovery

---

## 📊 Dataset

- **Source:** Spotify 30,000 Songs Dataset (Kaggle)
- **Tracks:** 28,356 unique songs after cleaning
- **Features:**
  - Audio: danceability, energy, loudness, tempo, valence, speechiness, etc.
  - Metadata: popularity, duration
  - Genre and subgenre labels

Audio features are derived from Spotify’s Audio Analysis API.

---

## ⚙️ Feature Engineering

- **Normalization:** MinMaxScaler for stable similarity computation
- **Dimensionality Reduction:** PCA  
  - 7 components explain ~90% of variance
- **Composite Features:**
  - party_score
  - chill_score
  - workout_score
  - energy_danceability
  - valence_energy

These engineered features capture interpretable musical characteristics beyond raw audio attributes.

---

## 📈 Evaluation & Analysis

### ✔ Recommendation Quality
- High cosine similarity across recommendations (≈ 0.99)
- Stable performance across genres

### ✔ Diversity Metrics
- Genre diversity
- Popularity variance
- Inter-recommendation similarity

### ✔ Cold-Start Performance
- Effective for songs with **popularity = 0**
- No reliance on user interaction history

### ✔ User Profile Simulation
- Tested on simulated **rap**, **pop**, and **EDM** users
- Hybrid model enables controlled cross-genre discovery

---

## 🔍 Key Insights

- **Popularity is weakly correlated with audio features**  
  Popularity is influenced more by social and cultural factors than sound alone.
- **Hybrid recommenders outperform single-method systems**  
  They balance relevance and diversity effectively.
- **Content-based models excel at cold start**  
  Ideal for new and niche tracks.

---

## 🛠️ Tech Stack

- **Language:** Python
- **Libraries:** pandas, numpy, scikit-learn, matplotlib, seaborn, plotly
- **Models:** Cosine Similarity, K-Means Clustering, PCA

---

