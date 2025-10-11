# THEORY:-

UNSUPERVISED LEARNING: Unsupervised learning is a type of machine learning that analyzes and models data without labelled responses or predefined categories. Unlike supervised learning, where the algorithm learns from input-output pairs, unsupervised learning algorithms work solely with input data and aim to discover hidden patterns, structures or relationships within the dataset independently, without any human intervention or prior knowledge of the data's meaning.

CLUSTERING: Clustering is a data mining technique which groups unlabeled data based on their similarities or differences. Clustering algorithms are used to process raw, unclassified data objects into groups represented by structures or patterns in the information. Clustering algorithms can be categorized into a few types, specifically exclusive, overlapping, hierarchical, and probabilistic. There are a great many clustering algorithms. They differ primarily in how they measure "similarity" or "proximity" and in what kinds of features they work with. 

K-MEANS CLUSTERING: K-means clustering measures similarity using ordinary straight-line distance (Euclidean distance, in other words). It creates clusters by placing a number of points, called centroids, inside the feature-space. Each point in the dataset is assigned to the cluster of whichever centroid it's closest to. The "k" in "k-means" is how many centroids (that is, clusters) it creates. K-means, is intuitive and easy to apply in a feature engineering context. Depending on your application another algorithm might be more appropriate.


# PROBLEM STATEMENT:-

In today’s highly competitive business environment, companies interact with a diverse customer base that varies in preferences, purchasing behaviors, and spending capacity. Treating all customers the same often leads to ineffective marketing strategies, poor resource allocation, and reduced customer satisfaction.
To overcome this challenge, businesses need to understand and categorize their customers into distinct groups based on behavioral and demographic similarities. However, manually identifying such patterns in large customer datasets is impractical and prone to bias.
This project aims to develop an unsupervised machine learning model using K-Means Clustering to automatically segment customers into meaningful groups based on key attributes such as annual income, spending score, and other behavioral metrics. The goal is to enable data-driven marketing strategies and enhance customer relationship management.

# OBJECTIVES:-

Data Acquisition and Preprocessing:

1) Import and explore the customer dataset.
  
2) Handle missing values, outliers, and normalize numerical features for better clustering performance.

Exploratory Data Analysis (EDA):

1) Visualize relationships between customer attributes (e.g., income vs. spending score).
   
2) Identify underlying patterns and data distribution using statistical and graphical methods.

Model Development using K-Means Clustering:

1) Apply the K-Means algorithm to group customers based on selected features.

2) Determine the optimal number of clusters using methods like the Elbow Method and Silhouette Score.

Cluster Interpretation and Profiling:

1) Analyze each cluster’s characteristics (e.g., high-income–high-spending, low-income–low-spending).

2) Assign descriptive labels to each cluster for marketing interpretation.

Visualization and Insights:

1) Present clustering results through visualizations (2D/3D plots, heatmaps).

2)  Derive actionable insights to help businesses tailor marketing campaigns, loyalty programs, and customer engagement strategies.

Conclusion and Future Scope:

1) Summarize findings and discuss how segmentation improves marketing efficiency.

2) Suggest extensions such as using hierarchical or DBSCAN clustering for comparison or incorporating more features (e.g., age, gender, purchase frequency).


# DATASET AND FEATURES:-

DATASET DESCRIPTION:

The dataset used in this project is taken from Kaggle’s notebook “Clustering with K-Means” by Ryan Holbrook. It contains information about mall customers and their spending habits. The data is ideal for demonstrating clustering techniques because it includes both demographic and behavioral attributes, allowing us to group customers with similar characteristics.
Each record in the dataset represents an individual customer. The dataset is relatively small, containing around 200–300 entries, making it suitable for visual and intuitive clustering analysis.

FEATURES DESCRIPTION:-

The dataset includes several key features that describe each customer:

1) CustomerID – This is a unique identification number assigned to each customer. It helps to distinguish between different records but does not carry any analytical meaning. Therefore, it is excluded from the clustering process.

2) Gender – Indicates whether the customer is male or female. Although it provides demographic information, gender is often not used in K-Means clustering because it is categorical and does not directly influence numerical distance calculations. However, it can be considered for extended analysis if encoded numerically.

3) Age – Represents the age of the customer in years. This feature helps understand how customer preferences vary across different age groups. For example, younger customers might have different spending behaviors compared to older ones.

4) Annual Income (k$) – Denotes the customer’s yearly income in thousands of dollars. This is one of the most significant features used for clustering since income level often affects spending behavior. It helps separate customers into high-income, medium-income, and low-income groups.

5)  Spending Score (1–100) – A score assigned to each customer by the mall based on factors such as purchasing frequency, loyalty, and total expenditure. A higher score indicates that a customer is more engaged and spends more frequently. This feature, along with annual income, plays a central role in forming meaningful customer segments.

FEATURES USED FOR CLUSTERING:

Although the dataset includes multiple features, only the most relevant ones are used for the K-Means clustering process. Typically, Annual Income and Spending Score are selected because they capture both the customer’s financial capacity and spending behavior. In some variations of the analysis, Age is also included to study the influence of age on purchasing patterns.
Before clustering, these numerical features are normalized or standardized to ensure that they contribute equally to the distance calculations used by the K-Means algorithm.

HOW THE FEATURES CONTRIBUTE TO CLUSTERING?

By combining these attributes, the algorithm identifies distinct groups of customers such as:

1) High-income, high-spending individuals (potential premium customers)

2) Low-income, low-spending individuals (budget-conscious customers)

3) High-income, low-spending individuals (customers with untapped potential)

4) Low-income, high-spending individuals (impulsive or trend-driven buyers)

5) Average-income, moderate-spending individuals (steady and reliable customers)

These clusters allow businesses to design personalized marketing strategies, allocate resources efficiently, and improve customer engagement.
