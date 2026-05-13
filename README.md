# IMDb Box Office Prediction Model

This project uses machine learning to predict whether a movie will be classified as a "Hit" or a "Flop" based on IMDb metadata such as title type, release year, genres, ratings, and vote counts.

## Overview

The dataset was built using IMDb title basics and ratings datasets. After preprocessing and feature engineering, a Random Forest Classifier was trained to classify movies into two categories:

- Hit
- Flop

The classification rule was created using:
- Average Rating ≥ 5
- Number of Votes ≥ 500

Movies satisfying both conditions were labeled as "Hit"; otherwise, they were labeled as "Flop".

## Technologies Used

- Python
- pandas
- scikit-learn
- imbalanced-learn (SMOTE)

## Machine Learning Workflow

### Data Processing
- Loaded IMDb datasets using pandas
- Merged title basics and ratings datasets
- Removed missing values
- Converted `startYear` into numeric format

### Feature Engineering
- Selected features:
  - `titleType`
  - `startYear`
  - `genres`
- Applied:
  - OneHotEncoding for categorical features
  - MultiLabelBinarizer for genres

### Handling Imbalanced Data
- Used SMOTE oversampling to balance the dataset before training

### Model Training
- Trained a Random Forest Classifier using scikit-learn

### Evaluation
The model was evaluated using:
- Accuracy Score
- Confusion Matrix
- Classification Report

## Files

- `main.py` — model training and evaluation script
- IMDb datasets used:
  - `title.basics.tsv`
  - `title.ratings.tsv`

## What I Learned

Through this project, I learned:
- Data preprocessing and cleaning
- Feature encoding techniques
- Handling imbalanced datasets using SMOTE
- Building and evaluating classification models
- Working with real-world datasets using pandas and scikit-learn
