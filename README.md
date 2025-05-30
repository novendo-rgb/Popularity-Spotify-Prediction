# Popularity-Spotify-Prediction
Analyzing and predicting Spotify song popularity based on audio and descriptive features.

## Project Overview
- Performed data cleaning and preprocessing by handling missing values, removing non-feature columns, converting categorical columns to category data type, and encoding them for modeling.
- Conducted exploratory data analysis (EDA) to understand the distribution and relationships of both numerical and categorical features.
- The data was prepared for modeling by performing a train-test split and applying feature scaling with StandardScaler to normalize the numerical features. Additionally, the categorical target variable was encoded using Label Encoder for models that require a numeric target variable.
- Built three classification models — SVM (Support Vector Machine), K-NN (K-Nearest Neighbors), and Random Forest — and optimized their parameters using GridSearchCV.
- The best model was selected by evaluating and comparing performance metrics such as the confusion matrix, classification report, and accuracy scores on both training and testing data.

## Dataset 
1. Primary Datasets
   The dataset used in this project consists of two CSV files: [high_popularity_spotify_data.csv](https://github.com/novendo-rgb/Popularity-Spotify-Prediction/blob/main/Dataset/high_popularity_spotify_data.csv)       and [low_popularity_spotify_data.csv](https://github.com/novendo-rgb/Popularity-Spotify-Prediction/blob/main/Dataset/low_popularity_spotify_data.csv). These files were created by collecting songs from Spotify's    API and separating them based on their popularity.
   Each record includes:
   - Descriptive features such as song name, artist, album, and release date.
   - Audio features extracted from Spotify’s audio analysis, including danceability, energy, valence, and tempo.
2. The combined dataset is based on a [Kaggle dataset](https://www.kaggle.com/datasets/solomonameh/spotify-music-dataset) by SOLOMON AMEH. For exploratory data analysis (EDA), reference was taken from       [HAFIDA BELAYD](https://www.kaggle.com/code/hafidabelayd/eda-spotify/notebook).
 
