# Customer Segmentation using K-Means Clustering

An unsupervised learning project that segments mall customers into distinct groups based on income and spending behavior.

## Objective
Businesses often want to group customers by behavior rather than by explicit labels, so they can target marketing or offers more effectively. This project uses K-Means clustering to discover natural customer segments from purchasing data, with no predefined categories.

## Dataset
- **Source:** [Mall Customer Segmentation dataset](https://www.kaggle.com/datasets/vjchoudhary7/customer-segmentation-tutorial-in-python) (Kaggle)
- **Features used:** Annual Income (k$) and Spending Score (1–100)

> Note: the raw dataset file isn't included here due to licensing — it's linked above and easy to download for anyone who wants to rerun the notebook.

## Approach
1. Loaded the dataset and selected Annual Income and Spending Score as the two clustering features.
2. Used the **elbow method** — plotting within-cluster sum of squares (WCSS) for k = 1 to 10 — to identify the optimal number of clusters.
3. Fit a K-Means model with the chosen number of clusters (`k=5`, using `k-means++` initialization).
4. Visualized the resulting clusters and centroids on a scatter plot.

## Tools
Python, pandas, scikit-learn (`KMeans`), Matplotlib

## Result
Identified **5 distinct customer segments**, ranging from low-income/low-spending customers to high-income/high-spending customers, with centroids plotted to show the center of each group.

## Notes / Next Steps
- The elbow point was chosen visually; a more rigorous approach would compute the silhouette score across candidate values of k to confirm the choice.
- Extending the feature set (e.g. adding Age) could reveal more nuanced segments beyond the two-dimensional view used here.
