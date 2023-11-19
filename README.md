# HarmonyCluster-Musical-Tracks-Clustering-Project.
Music Clustering README
Overview

This repository contains code for clustering music tracks based on their audio features using the KMeans algorithm. The goal is to group similar tracks together, enabling better organization and analysis of music collections.
Table of Contents

    Installation
    Data
    Data Cleaning
    Feature Scaling
    Clustering
    Results Visualization
    Determining Optimal Clusters
    Alternative Clustering Approaches
    Hierarchy Clustering
    DBSCAN and Epsilon Estimation

Installation

Ensure you have the required libraries installed. You can install them using:

bash

pip install pandas numpy scikit-learn seaborn matplotlib

For hierarchical clustering, you may also need:

bash

pip install scipy

For DBSCAN and HDBSCAN:

bash

pip install hdbscan

Data

The data is loaded from a CSV file (df_audio_features_5000_cleaned_whitespaces.csv) using the Pandas library. It includes information about each track, such as danceability, energy, key, loudness, and more.
Data Cleaning

The initial dataset is cleaned, ensuring there are no missing or erroneous values. The clean_data function removes any unwanted characters or whitespaces.
Feature Scaling

The selected audio features are scaled using different scaling techniques:

    Min-Max Scaling
    Robust Scaling
    Standard Scaling
    MaxAbs Scaling

Each scaling method ensures that all features are on a similar scale, preventing any particular feature from dominating the clustering process.
Clustering

KMeans clustering is applied to the scaled features. The number of clusters is determined based on various approaches, such as the Elbow Method, Silhouette Score, and Davies-Bouldin Index.
Results Visualization

The results of KMeans clustering are visualized using scatter plots. The points represent tracks in the feature space, and the colors indicate the assigned clusters.
Determining Optimal Clusters

Multiple methods are used to determine the optimal number of clusters:

    Elbow Method: Analyzing the point where the within-cluster sum of squares starts to decrease rapidly.
    Silhouette Score: Evaluating the average silhouette score for different cluster sizes.
    Davies-Bouldin Index: Calculating the index for different cluster sizes.

Alternative Clustering Approaches

Other clustering techniques, such as hierarchical clustering, DBSCAN, and HDBSCAN, are explored as alternatives to KMeans. The results are visualized to compare the clustering effectiveness.
Hierarchical Clustering

Hierarchical clustering is performed, and a dendrogram is plotted to visualize the hierarchical relationships between clusters.
DBSCAN and Epsilon Estimation

DBSCAN and HDBSCAN are applied for density-based clustering. The K-Nearest Neighbors plot is used to estimate the epsilon parameter for DBSCAN.

Feel free to reach out if you have any questions or need further clarification on any part of the code or README!
