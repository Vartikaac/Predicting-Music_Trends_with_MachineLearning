# Predicting Music Track Popularity Using Machine Learning

## Project Overview
This project aims to predict the popularity of a music track using its musical features, which can help music streaming services and record labels better allocate marketing resources, identify emerging artists, and curate playlists. The project explores various machine learning models to determine the most effective way of predicting a track’s popularity, categorized as "Low", "Medium", or "High" based on predefined popularity thresholds.

## Problem Statement
The ability to accurately predict the popularity of a music track is a valuable asset for artists, record labels, and streaming platforms. This project addresses the challenge of identifying which musical features most strongly contribute to a track's success. Our goal is to build models capable of classifying tracks into popularity classes using the following musical features:

- Acousticness
- Danceability
- Energy
- Instrumentalness
- Liveness
- Loudness
- Speechiness
- Tempo
- Valence
- Duration
- Key
- Mode
- Time Signature

## Project Workflow

### 1. Data Collection & Preprocessing
- The dataset includes tracks' musical features and their popularity scores.
- We dropped irrelevant columns such as the track ID and artist names.
- Popularity was categorized into "Low", "Medium", and "High" using predefined thresholds.

### 2. Exploratory Data Analysis (EDA)
A preliminary analysis was conducted to understand the distribution of the popularity classes and the relationships between musical features.

**Fig**: ![image](https://github.com/Vartikaac/Predicting-Music_Trends_with_MachineLearning
/blob/main/results/DC.png)

### 3. Model Development
Three machine learning models were developed and evaluated to predict the popularity of a track based on its musical features:

#### Logistic Regression:
- Logistic Regression was chosen for its simplicity and interpretability. However, it struggled with the "Low" popularity class.

**Fig**: Confusion Matrix for Logistic Regression showing model performance across popularity classes.

#### Random Forest:
- Random Forest was used for its ability to handle non-linear relationships and feature interactions. It performed significantly better across all popularity classes.

**Fig**: Confusion Matrix for Random Forest showing improved performance, especially for the 'Low' and 'High' popularity classes.

#### Naive Bayes:
- Naive Bayes was also tested, but it exhibited lower overall accuracy compared to Random Forest and Logistic Regression.

**Fig**: Confusion Matrix for Naive Bayes showing model performance with lower precision for the 'Low' popularity class.

### 4. Feature Importance Analysis
We analyzed the importance of each musical feature using the coefficients from the Logistic Regression model and the feature importances from the Random Forest model.

**Fig**: Feature importances from Logistic Regression.

**Fig**: Feature importances from Random Forest.

---

## Results & Findings

### Model Comparison:

- Logistic Regression achieved an accuracy of ~53%, struggling with the "Low" popularity class.
- Random Forest outperformed Logistic Regression with an accuracy of ~77%, showing much better performance in classifying all popularity classes.
- Naive Bayes performed poorly with an accuracy of ~40%, particularly misclassifying "Low" popularity tracks.

### Key Insights:

- **Instrumentalness** and **Acousticness** were found to be highly influential in predicting popularity.
- The **Random Forest model** was the most effective in balancing between the three popularity classes.

---

## Conclusion
The **Random Forest Classifier** significantly outperforms Logistic Regression and Naive Bayes in predicting track popularity, making it the most suitable model for this task. By leveraging the insights from feature importance, artists and record labels can focus on enhancing specific musical features to improve the likelihood of track success.
