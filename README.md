Cervical Cancer Prediction with Unsupervised Learning

1. Introduction
Cervical cancer is one of the leading causes of cancer-related deaths among women worldwide. Early detection and diagnosis are critical for improving survival rates. In this project, we explore an unsupervised learning approach to classify and analyze pap smear images. The objective is to cluster images into distinct categories, representing different cell types, using a combination of feature extraction, dimensionality reduction, and clustering techniques. This project also explores how these techniques can aid in cancer prediction and detection by identifying patterns and abnormalities in cell images.
The specific goals of the project include:

Extracting meaningful features from pap smear images using texture descriptors and deep learning.

Performing dimensionality reduction to enhance clustering performance.

Clustering algorithms (K-Means, GMM, DBSCAN) are applied to group images into biologically meaningful categories.

Evaluating the clustering results using performance metrics such as Adjusted Rand Index (ARI) and confusion matrices.

Incorporating augmented data and testing the model’s generalizability.

2. Feature Extraction
   
2.2.1 Local Binary Patterns (LBP)
LBP was used as a texture descriptor to extract local patterns in grayscale images. The feature vector was normalized to ensure comparability across images.

2.2.2 Deep Features with VGG16
A pretrained VGG16 model (excluding the fully connected layers) was used to extract deep features. The convolutional layers provided a 2048-dimensional feature vector for each image.


3. Clustering Algorithms
   
3.1 K-Means Clustering
K-Means was used to partition the dataset into six clusters. The algorithm iteratively minimized within-cluster variance and assigned each data point to its nearest cluster centre.

3.2 Gaussian Mixture Models (GMM)
GMM was employed to model each cluster as a Gaussian distribution. Different covariance types (full, diagonal, spherical, tied) were evaluated to find the best fit.

4. Evaluation Metrics
   
4.1 Adjusted Rand Index (ARI)
Images after clustering
ARI was used to measure the similarity between true labels and predicted clusters, accounting for chance groupings.

4.2 Confusion Matrix
A confusion matrix was generated for K-Means and GMM to evaluate how well the clusters matched the true labels.

4.3 Silhouette Score
The silhouette score measured the compactness and separability of clusters.
