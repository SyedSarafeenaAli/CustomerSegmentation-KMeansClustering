# THEORY:-

UNSUPERVISED LEARNING: Unsupervised learning is a type of machine learning that analyzes and models data without labelled responses or predefined categories. Unlike supervised learning, where the algorithm learns from input-output pairs, unsupervised learning algorithms work solely with input data and aim to discover hidden patterns, structures or relationships within the dataset independently, without any human intervention or prior knowledge of the data's meaning.

CLUSTERING: Clustering is a data mining technique which groups unlabeled data based on their similarities or differences. Clustering algorithms are used to process raw, unclassified data objects into groups represented by structures or patterns in the information. Clustering algorithms can be categorized into a few types, specifically exclusive, overlapping, hierarchical, and probabilistic. There are a great many clustering algorithms. They differ primarily in how they measure "similarity" or "proximity" and in what kinds of features they work with. 

K-MEANS CLUSTERING: K-means clustering measures similarity using ordinary straight-line distance (Euclidean distance, in other words). It creates clusters by placing a number of points, called centroids, inside the feature-space. Each point in the dataset is assigned to the cluster of whichever centroid it's closest to. The "k" in "k-means" is how many centroids (that is, clusters) it creates. K-means, is intuitive and easy to apply in a feature engineering context. Depending on your application another algorithm might be more appropriate.

STOCK CODE: 

StockCode is meant to follow the pattern [0-9]{5} but seems to have legit values for [0-9]{5}[a-zA-Z]+
Also contains other values: | Code | Description | Action | |---------------------|------------------------------------------------------------------------|-------------------------| | DCGS | Looks valid, some quantities are negative though and customer ID is null | Exclude from clustering | | D | Looks valid, represents discount values | Exclude from clustering | | DOT | Looks valid, represents postage charges | Exclude from clustering | | M or m | Looks valid, represents manual transactions | Exclude from clustering | | C2 | Carriage transaction - not sure what this means | Exclude from clustering | | C3 | Not sure, only 1 transaction | Exclude | | BANK CHARGES or B | Bank charges | Exclude from clustering | | S | Samples sent to customer | Exclude from clustering | | TESTXXX | Testing data, not valid | Exclude from clustering | | gift__XXX | Purchases with gift cards, might be interesting for another analysis, but no customer data | Exclude | | PADS | Looks like a legit stock code for padding | Include | | SP1002 | Looks like a special request item, only 2 transactions, 3 look legit, 1 has 0 pricing | Exclude for now| | AMAZONFEE | Looks like fees for Amazon shipping or something | Exclude for now | | ADJUSTX | Looks like manual account adjustments by admins | Exclude for now |

STANDARD SCALING:

Standard scaling, or z-score normalization, is a feature scaling technique that rescales numerical data so that each feature has a mean of 0 and a standard deviation of 1. This transformation is applied independently to each feature and is useful for machine learning algorithms sensitive to the scale of features. 

Standard Scaling = (value - mean) / standard deviation

SILHOUETTE SCORE: 

The silhouette score is a metric for evaluating the quality of cluster analysis in machine learning, measuring how well a data point fits into its assigned cluster compared to other clusters. It ranges from -1 to 1, where a score near +1 indicates that the point is well-clustered and far from other clusters, 0 suggests it's on a decision boundary between clusters, and a negative score implies the point may have been assigned to the wrong cluster. The overall silhouette score for a dataset is the average of the individual silhouette scores for all its data points. 

How it Works-

For each data point, the silhouette score quantifies its similarity to its own cluster versus the similarity to other clusters: 

a(i) (Intra-cluster distance): The average distance from a point i to all other points within the same cluster.

b(i) (Inter-cluster distance): The average distance from point i to all points in the nearest neighboring cluster.

Formula: The silhouette score for a single point i is calculated as (b(i) - a(i)) / max(a(i), b(i))
