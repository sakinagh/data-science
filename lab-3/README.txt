
Intro Data Science Lab 3 README
Sakina Ghafoor 

Overview
This project explores the use of machine learning algorithms in WEKA to predict student placement outcomes and perform clustering on 
student profile data. Using a dataset of 10,000 students, multiple classification models (Logistic Regression, IBK, K-Star, LWL) and 
clustering techniques (SimpleKMeans, EM) were applied. The goal was to evaluate model performance with various preprocessing steps 
(Discretization, Normalization) and tuning parameters (e.g., number of neighbors, distance weighting, cluster numbers). The results 
include accuracy metrics for classification models and log-likelihood/cluster analysis for clustering models.

Dataset
placementdata.csv / placementdata.csv.arff
Dataset of around 10,000 student records, with features such as: CGPA, Internships, Projects, Workshops/Certifications, Aptitude Test Score, 
Soft Skills Rating, Extracurricular Activities, Placement Training, SSC Marks, HSC Marks, Placement Status (Target variable)

Experiments Overview
Logistic Regression
	1_weka_logistic — Logistic Regression on training set
	2_weka_logistic_discretize — Logistic Regression with Discretize filter
	3_weka_logistic_cross_val — Logistic Regression with 10-fold Cross Validation
IBK (K-Nearest Neighbors)
	4_weka_ibk — IBK on training set
	5_weka_ibk_cross_val — IBK with 10-fold Cross Validation
	6_weka_ibk_cross_val_k3 — IBK with k=3
	7_weka_ibk_cross_val_dist_weight — IBK with distance weighting (1/distance)
	8_weka_ibk_cross_val_discretize — IBK with Discretize filter
K-Star & LWL
	9_weka_kstar_cross_val_discretize — K-Star with Discretize and Cross Validation
	10_weka_LWL_cross_val_discretize — LWL (Locally Weighted Learning) with Discretize and Cross Validation
Clustering
	11_weka_simplekmeans — SimpleKMeans default
	12_weka_simplekmeans_discretize — SimpleKMeans with Discretize filter
	13_weka_simplekmeans_normalize — SimpleKMeans with Normalize filter 
	14_weka_EM — EM Clustering default
	15_weka_EM_normalize — EM Clustering with Normalize filter 

Additional Files
report.txt — Summary of findings, model performance, and conclusions

Screenshots
screenshot of ibk distance weight
screenshot of ibk k value
screenshot of preprocess and attribute
screenshot of simple k means settings for numClusters and maxIterations

Notes
Data Preprocessing:
Discretization improved accuracy for classification models.
Normalization improved clustering performance.
For clustering, at least 3 clusters and 100 iterations were used.
Evaluated clustering performance using log-likelihood and number of clusters.
