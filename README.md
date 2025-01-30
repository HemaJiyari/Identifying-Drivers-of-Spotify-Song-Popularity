# 🎵 Predicting Spotify Song Popularity  

---

## 📖 Table of Contents  
1. [Introduction](#introduction)  
2. [Dataset Overview](#dataset-overview)  
3. [Methodology](#methodology)  
4. [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)  
5. [Machine Learning Models](#machine-learning-models)  
6. [Results & Findings](#results--findings)  
7. [Future Enhancements](#future-enhancements)  
8. [Repository Contents](#repository-contents)  
9. [Conclusion](#conclusion)  

---

## 🎵 Introduction  
Spotify, a leading music streaming platform, provides vast amounts of data on songs, including features such as **tempo, energy, danceability, loudness, valence, and more**. Understanding what makes a song popular can provide valuable insights for:  
- **Music producers** to optimize song features.  
- **Streaming services** to improve recommendation algorithms.  
- **Artists and labels** to better target audiences.  

This project explores **what features drive song popularity on Spotify** by applying **Exploratory Data Analysis (EDA), Clustering, and Machine Learning Models** to predict popularity.  

---

## 📂 Dataset Overview  
- **Source:** Kaggle  
- **Size:** 20,000 songs  
- **Attributes:**  
  - **Metadata:** Genre, Artist Name, Track Name, Track ID  
  - **Audio Features:** Popularity, Acousticness, Danceability, Duration, Energy, Instrumentalness, Key, Loudness, Mode, Speechiness, Tempo, Valence, etc.  
- **Target Variable:** **Popularity Score (0–100)**  

### **Key Observations from Data**  
- **High variation** in popularity scores.  
- **Skewed distribution**, with most songs having a lower popularity score.  
- **Strong correlations** between features like **loudness, danceability, and energy** with song popularity.  

---

## 🔍 Methodology  
### 1️⃣ Exploratory Data Analysis (EDA)  
- **Feature Distribution Analysis:** Visualized feature distributions using **histograms, scatter plots, and boxplots**.  
- **Correlation Analysis:** Identified relationships between features and popularity using a **correlation matrix**.  
- **Outlier Detection & Handling:** Used **Z-score method** to cap extreme values.  

### 2️⃣ Data Preprocessing  
- **Handled Missing Values** (mean replacement or row removal).  
- **Removed Duplicates** (~2,000 songs had duplicate track names).  
- **Normalized Features** to bring them to the same scale.  

### 3️⃣ Clustering Analysis  
- **Hierarchical Clustering (Dendrograms)**  
- **K-Means Clustering:** Identified 6 clusters with distinct characteristics.  

### 4️⃣ Machine Learning Models  
We tested five models to predict song popularity:  
✅ **Linear Regression**  
✅ **Random Forest (Best Performing Model)**  
✅ **Decision Tree**  
✅ **K-Nearest Neighbors (KNN)**  
✅ **Naïve Baseline Model**  

---

## 📊 Exploratory Data Analysis (EDA)  
### **Feature Importance Findings:**  
- **Loudness, Energy, and Danceability** are strongly correlated with **high popularity**.  
- **Instrumentalness and Acousticness** negatively correlate with **popularity**.  
- **Speech-oriented tracks** (high speechiness) tend to have **lower popularity scores**.  

### **Clusters Insights (K-Means Clustering)**
- **Cluster 0:** High Danceability & Popularity, Low Acousticness.  
- **Cluster 1:** High Instrumentalness & Acousticness, Low Valence.  
- **Cluster 2:** High Acousticness, Low Energy.  
- **Cluster 3:** High Energy, Low Duration.  
- **Cluster 4:** High Speechiness & Tempo.  
- **Cluster 5:** Low Danceability, High Loudness & Energy.  

---

## 🤖 Machine Learning Models  

We implemented five machine learning models to predict song popularity:  

- **Linear Regression**  
  - Mean Squared Error (MSE): **0.92**  
  - Root Mean Squared Error (RMSE): **0.96**  
  - Mean Absolute Error (MAE): **0.75**  
  - Adjusted R²: **0.08**  

- **Decision Tree**  
  - MSE: **0.85**  
  - RMSE: **0.92**  
  - MAE: **0.72**  
  - Adjusted R²: **0.12**  

- **K-Nearest Neighbors (KNN)**  
  - MSE: **0.81**  
  - RMSE: **0.90**  
  - MAE: **0.70**  
  - Adjusted R²: **0.14**  

- **Random Forest (Best Model)** ✅  
  - MSE: **0.75**  
  - RMSE: **0.87**  
  - MAE: **0.65**  
  - Adjusted R²: **0.22**  

💡 **Final Model:** **Random Forest** outperformed all others in predictive accuracy, showing the lowest error rates and highest Adjusted R².  

---

## 🔮 Results & Findings  
✅ **Loudness, Energy, and Danceability** are the strongest predictors of song popularity.  
✅ **Random Forest** outperformed other models in predictive accuracy.  
✅ **High instrumentalness and acousticness negatively impact popularity.**  
✅ **Understanding these factors helps artists/producers tailor their music for success.**  

---

## 🚀 Future Enhancements  
- 🔹 **Deep Learning Models:** Try Recurrent Neural Networks (RNNs) and Transformers.  
- 🔹 **Real-Time Streaming Data:** Integrate dynamic data from Spotify APIs.  
- 🔹 **Feature Engineering:** Extract more song features to improve accuracy.  
- 🔹 **Recommendation System:** Build a system to suggest hit songs based on trends.  

---

## 📁 Repository Contents  
- 📂 `Songs_data.csv` – Cleaned dataset used for analysis.  
- 📂 `Spotify_drivers.ipynb` – Jupyter Notebook with full EDA, preprocessing, clustering, and model training.  

---

## 🎤 Conclusion  
Understanding what makes a song popular is **valuable for artists, producers, and streaming services**.  
By leveraging **data mining and machine learning**, we have identified the most influential features and developed a model that **predicts song popularity with reasonable accuracy**.  

📌 **Check out the full analysis in our Jupyter Notebook!**  

---
