# 📚 Personalized Recommendation System for DSA Problems

## 📌 Project
Mastering Data Structures and Algorithms (DSA) is essential for students and professionals in computer science. However, the overwhelming number of problems makes it challenging for learners to choose tasks that match their skill levels and objectives.  
This project presents a **personalized recommendation system** for DSA problems, primarily using **Content-Based Filtering (CBF)** to recommend problems based on attributes such as **difficulty**, **topic**, and **metadata**.  

## 🎯 Objectives
- Recommend DSA problems tailored to the learner's skill level.
- Compare and integrate **Content-Based Filtering** with **Collaborative Filtering**.
- Improve accuracy and personalization of recommendations.

## 📂 Dataset
- **Source:** [GeeksForGeeks DSA Problems](https://www.geeksforgeeks.org/) (via Kaggle)
- **Size:** Expanded from 260 to 740 problems.
- **Attributes:** Difficulty level, topic, problem statement, metadata.

## 🛠 Tools Used
- **Python**
- **Scikit-learn**
- **Pandas / NumPy**
- **TF-IDF Vectorizer**
- **Cosine Similarity**
- **Ridge Regression**
- **Collaborative Filtering**
- **Hybrid Recommendation Model**

## ⚙️ Methodology
### 1. Content-Based Filtering (CBF)
- **Feature Extraction:** Using **TF-IDF** to capture the importance of terms in problem descriptions.
- **Similarity Computation:** **Cosine Similarity** to match problems with learner profiles.
- **Recommendation:** Suggests problems with highest similarity scores.

### 2. Collaborative Filtering (CF)
- Simulated user-item interaction data (due to lack of real user logs).
- Generated random ratings for simulated users.
- Normalized ratings using standard scaling.
- Computed **item-to-item similarity** to find related problems.

### 3. Hybrid Model
- Combines **CBF** + **CF** for more accurate and personalized results.
- Integrates problem features with user interaction patterns.

## 📊 Hyperparameters
- **TF-IDF Vectorizer:**
  - `ngram_range = (1, 2)` to capture both single words and consecutive word pairs.
- **Ridge Regression:**
  - `alpha`: Regularization strength.
  - `n_iter = 20`: Number of parameter samples.
  - `cv = 5`: 5-fold cross-validation.
  - `scoring = 'r2'`: Model performance metric.

## 📈 Evaluation Metrics
- **Accuracy:** `(TP + TN) / (TP + TN + FP + FN)`
- **Precision:** `TP / (TP + FP)`
- **Recall:** `TP / (TP + FN)`
- **F1-score:** `2 * (Precision * Recall) / (Precision + Recall)`
- 
## 🚀 Results
- **Overall Accuracy:** 87%
- **Weighted F1-score:** 0.86
- **Best Performance:** "Medium" difficulty problems (F1-score: 0.93)
- **Challenge:** Lower performance on "Basic" problems due to data imbalance.
