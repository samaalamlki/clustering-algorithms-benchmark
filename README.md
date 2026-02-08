# Clustering Algorithms Benchmark

This project benchmarks multiple clustering algorithms on synthetic datasets with different geometric structures.
The goal is to analyze how each algorithm performs under varying data distributions and to highlight their strengths and limitations.

## Overview
Clustering is an unsupervised learning task used to discover hidden groupings in data.
Since different clustering algorithms rely on different assumptions, this project compares several popular methods across multiple datasets.

Algorithms evaluated:
- K-Means
- DBSCAN
- Agglomerative (Hierarchical) Clustering
- Gaussian Mixture Model (GMM)

## Datasets
The datasets used in this project are synthetically generated using scikit-learn:
- Linearly separable blobs
- Transformed blobs
- Two-moons dataset
- Concentric circles dataset

Synthetic datasets allow controlled evaluation of clustering performance under different geometric patterns.

## Methods
Each clustering algorithm was applied to all datasets using appropriate hyperparameters:
- K-Means: centroid-based clustering assuming spherical clusters
- DBSCAN: density-based clustering capable of detecting noise and arbitrary shapes
- Hierarchical Clustering: bottom-up agglomerative approach
- GMM: probabilistic clustering using Gaussian distributions

## Evaluation Metrics
Because the datasets are synthetic, ground-truth labels are available only for evaluation.

Metrics used:
- F1-score (macro)
- Normalized Mutual Information (NMI)
- Rand Index

> Note: In clustering, predicted cluster labels are arbitrary.
> NMI and Rand Index are more reliable metrics for unsupervised evaluation.

## Results
The clustering results were visualized and evaluated for each dataset.
A ranking table was created to compare algorithm performance.

Key observations:
- K-Means performs well on linearly separable data
- DBSCAN handles non-linear structures and noise effectively
- Hierarchical clustering provides competitive results on structured datasets
- GMM performs well when data follows Gaussian-like distributions

## How to Run
1. Install dependencies:
```bash
pip install -r requirements.txt
