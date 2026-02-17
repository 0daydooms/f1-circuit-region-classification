# f1-circuit-region-classification
Machine Learning classification of Formula 1 circuits into geographic regions using KNN, SVM,m Forest and Decision Tree models with PCA dimensionality reduction.


# F1 Circuit Region Classification

A Machine Learning project that classifies Formula 1 circuits into geographic
regions (Europe, Americas, Asia/Oceania) based on circuit features such as
latitude, longitude, and altitude.

## Overview

This project explores supervised classification models to predict the
geographic region of F1 circuits. It was developed as a course project
for a Machine Learning class and runs entirely on **Google Colab**.

## Objective

Predict the **region** (Europe, Americas, Asia/Oceania) of an F1 circuit
using geographic and engineered features.

## Dataset

- **Source:** Formula 1 World Championship dataset (`circuits.csv`)
- **Samples:** ~77 circuits
- **Features:** Latitude, Longitude, Altitude, Name Length, Absolute Latitude
- **Target:** Region (Europe, Americas, Asia/Oceania)

## Pipeline
Raw Data → Feature Engineering → Standardization → PCA → Model Training → Evaluation


## Models Tested

| Model | Variants |
|-------|----------|
| K-Nearest Neighbors | K=3, K=5, K=7 |
| Support Vector Machine | Linear, Polynomial (degree=3) |
| Random Forest | 100 estimators |
| Decision Tree | Max depth = 5 |

## Key Results

- **Best Model:** KNN
- **Evaluation:** 5-Fold Stratified Cross-Validation
- **Visualizations:** PCA projections, decision boundaries, confusion matrices

## Tech Stack

- Python 3
- scikit-learn
- pandas / NumPy
- matplotlib / seaborn
- Google Colab

## Quick Start

1. Open the notebook in Google Colab
2. Upload `circuits.csv` when prompted
3. Run all cells sequentially

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/)

## Project Structure

f1-circuit-region-classification/
├── f1_classification.ipynb # Main Colab notebook
├── circuits.csv # Dataset
├── README.md # This file
└── images/ # Generated plots
├── pca_projection.png
├── cv_results.png
├── confusion_matrix.png
└── decision_boundaries.png

## Sample Outputs

### PCA Projection
Circuits projected onto 2 principal components, colored by region.

### Decision Boundaries
Visual comparison of how each model separates the regions in 2D space.

### Model Comparison
Cross-validation accuracy distribution and test accuracy for all 7 model
variants.

## Findings

| Aspect | Insight |
|--------|---------|
| **Best approach** | KNN leverages geographic proximity naturally |
| **PCA impact** | Reduces 5 features to 3-4 components retaining 95% variance |
| **Dataset challenge** | Small size (~77 samples) limits complex model performance |
| **Key features** | Latitude and Longitude are the strongest predictors |

## Author

Islam Taouri [VR533905]

Machine Learning Course Project — Università degli Studi di Verona — 25/26
