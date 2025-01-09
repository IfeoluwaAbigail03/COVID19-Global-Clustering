# COVID19-Global-Clustering
This project analyzed COVID-19 data from Our World in Data to reveal patterns across countries using unsupervised machine learning techniques. 
The project used KMeans Clustering, DBSCAN, and Hierarchical Clustering, with Principal Component Analysis (PCA) for dimensionality reduction and visualization.

# Main Objective of the Analysis
The primary goal is to apply clustering techniques to group countries with similar COVID-19 trends in helping healthcare organizations:

Identify patterns in case numbers and healthcare capacity.
Prioritize resource allocation based on the severity of the situation.
Analyze case fatality rates to detect areas with high mortality rate.
Dataset Description

# The dataset is sourced from Our World in Data. Key features include:
total_cases: Cumulative confirmed cases.
new_cases: New confirmed cases.
total_deaths: Cumulative confirmed deaths.
hospital_beds_per_thousand: Healthcare capacity (proxy).
case_fatality_rate: Mortality risk calculated as total deaths/total cases.

# Data Cleaning and Preprocessing
Imputed missing values (numerical using median, categorical using mode).
Standardized numerical features with StandardScaler for comparability.
Removed columns with >50% missing data.
Created case_fatality_rate as a new feature.

# Models Applied
Three clustering algorithms were applied:
KMeans Clustering:
Chose 5 clusters using the Elbow Method.
Best-performing model for this dataset due to interpretability and stability.
DBSCAN:
Density-based clustering.
Struggled with noise sensitivity (not ideal for this dataset).
Hierarchical Clustering:
Ward’s linkage for distance-based clustering.
Less scalable for large datasets.

# Dimensionality Reduction (PCA)
Applied Principal Component Analysis (PCA) to reduce the dataset to 2 dimensions for better visualization and improved cluster separation.

# Cluster Visualization
KMeans Clusters (PCA reduced)
DBSCAN Clusters (PCA reduced)
Hierarchical Clustering Dendrogram

# Key Insights
Cluster 0: Moderate total cases (~5.3 million), moderate fatality rate (2.83%).
Cluster 1: High cases (~336 million), high fatality (~4.37 million), good healthcare.
Cluster 2: Very low cases but high fatality (~846%); needs further investigation.
Cluster 3: High total cases (~598 million), low fatality (1%).
Cluster 4: High cases (~127 million), moderate fatality (2.65%).

 # Future Suggestions for Improvement
Investigate anomalies in Cluster 2.
Incorporate additional data (e.g., vaccination rates, ICU availability) to refine clustering.

