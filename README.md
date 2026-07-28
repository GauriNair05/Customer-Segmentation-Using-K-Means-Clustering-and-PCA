# Customer Segmentation Using K-Means Clustering and PCA

## Objective
The primary objective of this project is to segment shopping mall customers into distinct groups based on their annual income and spending behavior. This enables management to design targeted marketing campaigns, optimize promotional strategies, and improve customer satisfaction.

## Dataset Link
[Kaggle Mall Customer Segmentation Data](https://www.kaggle.com/datasets/vjchoudhary7/customer-segmentation-tutorial-in-python)

## Libraries Used
* **Pandas**: Data manipulation and exploratory analysis
* **NumPy**: Numerical computations
* **Matplotlib**: Basic plotting and visualization
* **Seaborn**: Statistical data visualization
* **Scikit-learn**: Data preprocessing (`StandardScaler`, `LabelEncoder`), clustering (`KMeans`), and dimensionality reduction (`PCA`)

## Methodology
1. **Data Understanding**: Loaded the dataset, inspected numerical (`Age`, `Annual Income (k$)`, `Spending Score (1-100)`) and categorical (`Gender`) features, and generated summary statistics.
2. **Data Preprocessing**: Checked for missing values, removed non-informative identifiers (`CustomerID`), categorical binary encoding for `Gender`, and standardized numerical features using `StandardScaler`.
3. **Model Development**: 
   * Applied the Elbow Method (evaluating Within-Cluster Sum of Squares, WCSS) to find the optimal number of clusters ($k$).
   * Trained a K-Means clustering model using the selected value ($k = 5$).
   * Transformed the standardized feature space to 2 dimensions using Principal Component Analysis (PCA) for visualization.
4. **Visualization**: Plotted the Elbow Curve, cluster distributions across income/spending metrics, and 2D PCA representations.

## Key Observations & Results
1. **Optimal Number of Clusters**: The Elbow Method indicated a clear bend at **$k = 5$**, demonstrating that five distinct customer segments effectively explain the variance without overfitting.
2. **Role of PCA in Visualization**: PCA compresses multidimensional customer data (Age, Gender, Income, Spending Score) into two uncorrelated principal components, making high-dimensional cluster boundaries simple to plot and interpret in a 2D space.
3. **Characteristics of Customer Groups**:
   * **High Income, High Spending (Target Group)**: Premium shoppers responsive to luxury products.
   * **High Income, Low Spending (Careful Shoppers)**: High earners who spend conservatively; ideal for value-focused targeted offers.
   * **Low Income, High Spending (Careless Shoppers)**: Budget-constrained customers with high spending habits.
   * **Low Income, Low Spending (Sensible Shoppers)**: Cost-conscious shoppers with low spending behavior.
   * **Average Income, Average Spending (Standard Shoppers)**: The moderate majority with balanced financial behavior.

## Conclusion
This project successfully segmented shopping mall customers into five actionable groups using K-Means clustering and PCA. These segments empower the marketing team to optimize campaign strategies, tailor product recommendations, and maximize ROI by delivering targeted promotions to specific customer profiles. A key advantage of PCA is its ability to reduce dimensionality while preserving maximal variance, simplifying complex dataset visualizations. However, a limitation of K-Means clustering is its sensitivity to initial centroid placement and its assumption of spherical clusters, which can lead to suboptimal groupings on non-linearly separable data.
