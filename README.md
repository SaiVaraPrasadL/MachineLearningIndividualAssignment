k-Means Clustering with Different Distance Metrics
Overview
This study explores how various distance metrics affect the performance of k-Means clustering.  The Mall customers Segmentation Dataset is used in the study to assess the Euclidean, Manhattan, and Cosine distances for customer segmentation.  By examining elbow technique findings, silhouette scores, and mean squared error (MSE), the objective is to identify the best distance metric for clustering.

Table of Contents
Introduction
Methodology
Dataset Selection & Preprocessing
Choosing the Optimal Number of Clusters
K-Means with Different Distance Metrics
Results and Analysis
Elbow Method Results
Silhouette Scores
Comparison of MSE
Cluster Visualization
Conclusion
How to Run the Code
Requirements


Introduction:

An unsupervised machine learning method called clustering puts data into groups according to commonalities.  The choice of distance measure, which affects how data points are classified, has a significant impact on how successful clustering is.  The following metrics are most frequently used in k-Means clustering:
Euclidean Distance: Assumes clusters are spherical and of equal size.
Manhattan Distance: Measures absolute differences but struggles with diagonal clusters.
Cosine Similarity: Evaluates vector direction rather than magnitude, making it suitable for high-dimensional text data.
This study compares these three metrics to determine which produces the best clustering results for customer segmentation.

Methodology:

Dataset Selection & Preprocessing
Dataset: Mall Customer Segmentation Dataset

Features:
CustomerID: Unique identifier
Gender: Male/Female
Age: Customer’s age
Annual Income: Indicator of purchasing power
Spending Score: Measure of spending behavior

Preprocessing:
Standardized data using StandardScaler to maintain zero mean and unit variance.

Choosing the Optimal Number of Clusters:
Elbow Method: Determines optimal k by finding the "elbow point" in the Within-Cluster Sum of Squares (WCSS) plot.
Silhouette Score: Measures how well data points fit into clusters. Higher scores indicate better clustering.

K-Means with Different Distance Metrics:
Euclidean Distance: Standard k-Means metric, assumes compact and spherical clusters.
Manhattan Distance: Measures distances along axes, reducing sensitivity to outliers.
Cosine Similarity: Measures angular distance, better suited for text and sparse data.

Results and Analysis:
Elbow Method Results:

Euclidean Distance: Optimal k = 5
Manhattan Distance: Optimal k = 5
Cosine Distance: Optimal k = 2
Silhouette Scores
Euclidean Distance: Highest silhouette score at k = 5
Manhattan Distance: Similar to Euclidean, confirming k = 5
Cosine Distance: Best performance at k = 2, indicating poor numerical clustering
Comparison of MSE
Distance Metric	Optimal K	MSE	Observations
Euclidean Distance	5	0.1639	Best clustering performance
Manhattan Distance	5	0.1639	Similar performance to Euclidean
Cosine Distance	2	0.6742	Poor clustering due to high MSE

Cluster Visualization:
Euclidean & Manhattan Distance: Created five distinct clusters, effectively segmenting customers.
Cosine Similarity: Formed only two large clusters, failing to differentiate spending behaviors.

Conclusion:
This study demonstrates that Euclidean and Manhattan distances produce the best k-Means clustering results for customer segmentation, achieving the lowest MSE (0.1639) and forming five well-defined clusters. Cosine similarity performed poorly (MSE = 0.6742), making it unsuitable for numerical datasets.

Key takeaways:

Euclidean & Manhattan distances are best for customer segmentation.
Cosine similarity is better suited for high-dimensional text data.
Choosing the right distance metric is crucial for effective clustering.

How to Run the Code:
Clone the repository:

git clone - https://github.com/SaiVaraPrasadL/MachineLearningIndividualAssignment
cd MachineLearningIndividualAssignment

Install dependencies:
pip install -r requirements.txt
Run the clustering script:
python kmeans_clustering.py

Requirements:
Python 3.x
NumPy
Pandas
Scikit-learn
Matplotlib
Seaborn

Acknowledgments:
This project is based on customer segmentation using k-Means clustering and explores how different distance metrics impact clustering performance.
