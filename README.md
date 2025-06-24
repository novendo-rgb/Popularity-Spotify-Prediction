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

 ## Data Cleaning
- Data Cleaning is a crucial step to to prepare clean and consistent data before proceeding to the exploratory data analysis (EDA) and model building stages.
- Checked for null values in the dataset. Since only a small number of null values were found, they were simply removed. (Nanti masukin gambar)
- Converted the "track_album_release_date" column to datetime format to facilitate easier analysis and visualization during EDA, as well as to support effective model building.
- Converted all categorical columns to category type to optimize memory usage and processing efficiency, while also preparing the data for modeling and simplifying validation.
- Create the feature list by excluding the non-feature columns.
- Encoding the categorical columns using the one-hot encoding method.

## EDA
- Performed descriptive statistics using 'df.describe()' separately on numerical and categorical features to understand their distributions.
- Created distribution plots and boxplots to analyze the distribution of numerical features grouped by the popularity label, as well as to detect outliers.
- Generated a correlation matrix to examine linear relationships between numerical features and to identify potential multicollinearity. (Nanti masukin gambar)
- Created scatter plots and pairplot to explore the relationship between individual numerical features and the popularity score.
- Performed two-sample t-tests on numerical features to assess whether the differences in means between popular and non-popular tracks are statistically significant. (Nanti masukin gambar)
- Calculated the Pearson correlation between numerical features and the popularity score, and visualized the results using a bar plot.
- Created trend plots showing the average popularity score and the number of tracks over the years.
- Explored categorical features by plotting average popularity trends by genre and subgenre, and using count plots to show the distribution of mode and key.

## Feature Engineering
- Handled skewed features using log transformation to improve model performance.
- Defined the features and target variables in the final dataset

## Model Preparation
- Applied Label Encoding to the target variable for classification.
- Divided the dataset into training and testing sets for both features and target variables with an 80:20 ratio.
- Used feature scaling for models that are sensitive to the scale of input data.

## Modelling
- Created three classification models, namely **K-Nearest Neighbors (KNN)**, **Support Vector Machine (SVM)**, and **Random Forest Classifier**.
- Used GridSearchCV for each model to find the optimal parameters.
- The best estimator from GridSearchCV was trained on the training dataset.
- Made predictions on the test dataset using the trained model.
- Generated the confusion matrix and calculated the accuracy score for the model's predictions.
- Created a classification report to evaluate precision, recall, and F1-score.
- Calculated both training and test accuracy to assess model performance.













