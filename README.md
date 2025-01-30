# Identifying-Drivers-of-Spotify-Song-Popularity
🎵 Identifying Drivers of Spotify Song Popularity
📌 Project Overview
This project explores the key factors that drive the popularity of songs on Spotify using data mining and machine learning techniques. By analyzing various audio features and metadata, we aim to identify patterns that contribute to a song’s success and develop predictive models to estimate song popularity.
📂 Dataset
Source: The dataset was obtained from Kaggle and contains 20,000 songs with 18 attributes.
Attributes Include:
Metadata: Genre, Artist Name, Track Name, Track ID
Audio Features: Popularity, Acousticness, Danceability, Duration, Energy, Instrumentalness, Key, Loudness, Mode, Speechiness, Tempo, Valence, and more
Ranking: Songs are ranked from 1 to 100 based on their popularity on Spotify.
🛠️ Methodology
🔎 1. Exploratory Data Analysis (EDA)
Visualized feature distributions to understand patterns.
Identified correlations between attributes and song popularity.
Plotted scatter plots and bar graphs to analyze trends.
🔄 2. Data Preprocessing
Handled missing values by either removing rows or filling them with mean values.
Removed duplicate entries (~2,000 songs had identical track names).
Identified and treated outliers in the popularity attribute using the Z-score method.
Normalized features to bring them to a common scale.
🎯 3. Clustering Analysis
Performed Hierarchical Clustering using Single Linkage & Average Linkage methods.
Applied K-Means Clustering, identifying six distinct clusters based on song characteristics.
🤖 4. Model Selection & Training
Machine Learning Models Used:
Linear Regression
Naïve Model
Random Forest (Best Performing Model)
Decision Tree
K-Nearest Neighbors (KNN)
Evaluation Metrics:
Mean Squared Error (MSE), Root Mean Squared Error (RMSE), Mean Absolute Error (MAE), Adjusted R²
🏆 5. Best Performing Model
Random Forest outperformed all other models with the lowest RMSE and highest Adjusted R².
Error Metrics for Random Forest:
MSE: 0.75
RMSE: 0.87
MAE: 0.65
Adjusted R²: 0.22
📊 Key Findings
Loudness, Energy, and Danceability have the highest positive correlation with song popularity.
Instrumentalness and Acousticness are negatively correlated with popularity.
Popular songs tend to have high tempo, loudness, and danceability.
K-Means Clustering categorized songs into six meaningful groups based on their characteristics.
💡 Conclusion
This project provides valuable insights into what makes a song popular on Spotify. By leveraging data mining and machine learning, we have identified the most influential features and built predictive models that help artists, producers, and music platforms understand and enhance their music strategies.
