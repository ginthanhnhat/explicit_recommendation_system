# Explicit Recommendation System – Rating Prediction

🔗 **Google Colab Version:**  
The complete notebook implementation can be accessed and executed on Google Colab:  
👉 https://colab.research.google.com/drive/1ozqrrd0RKNrWHvWhPNu2vj_M6nVIo-Mn?usp=sharing  

> Note: If the `.ipynb` file does not render properly on GitHub, please use the Colab link above to run the project.


This project implements and compares multiple Explicit Feedback Recommendation Systems using rating data.
The goal is to build, train, and evaluate different recommendation algorithms across multiple datasets.


## Project Overview
This repository contains implementations of:
- Content-Based Filtering (CBF)
- Neighborhood-Based Collaborative Filtering (NBCF)
    - User-User Collaborative Filtering (UUCF)
    - Item-Item Collaborative Filtering (IICF)
- Matrix Factorization Collaborative Filtering (MFCF)
All models are evaluated using explicit rating prediction tasks.

## Datasets Used
The models are tested on:
1. Gift Cards
2. Cell Phones and Accessories
3. MovieLens 1M

## Implemented Methods

1. Content-Based Filtering (CBF)
- Builds item profiles using item features.
- Computes user profiles from previously rated items.
- Recommends items based on similarity between user and item vectors.
- Similarity metric: Cosine Similarity.

2. Neighborhood-Based Collaborative Filtering (NBCF)
- User-User Collaborative Filtering (UUCF)
    - Finds similar users based on rating similarity.
    - Predicts rating using weighted average of neighbors.
- Item-Item Collaborative Filtering (IICF)
    - Finds similar items based on user ratings.
    - Predicts rating using similarity between items rated by the user.

3. Matrix Factorization Collaborative Filtering (MFCF)
- Decomposes rating matrix into:
    - User latent factors
    - Item latent factors
- Learns latent embeddings using optimization (SGD, ALS).
- Captures hidden interactions between users and items.

## Evaluation
Models are evaluated using common regression metrics:
- RMSE (Root Mean Squared Error)
- MAE (Mean Absolute Error)

Comparison is performed across:
- Different algorithms
- Different datasets