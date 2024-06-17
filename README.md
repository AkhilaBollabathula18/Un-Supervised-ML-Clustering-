### Report on Hierarchical Clustering and PCA Analysis of Country Data

*** Introduction:

In this report, we explore the application of hierarchical clustering and principal component analysis (PCA) on country data using Python's scientific libraries such as 
pandas, numpy, matplotlib, seaborn, and scikit-learn. The dataset used contains socio-economic indicators for various countries.

*** Data Overview:

The dataset (`Country-data.csv`) includes socio-economic indicators for countries, such as GDP per capita, income, and mortality rates among others.

  ***Loading and Exploring the Data:
  - We loaded the dataset using pandas and examined its structure using `df.head()`, `df.describe()`, `df.info()`, and `df.shape` to understand its dimensions, columns,
    and basic statistics.

  ***Data Preprocessing:
  - Checked for missing values (`df.isnull().sum()`).
  - Extracted numerical features for clustering, dropping non-numeric columns (`df.drop(["country"], axis=1)`).
  - Standardized the data using `StandardScaler` to ensure all variables contribute equally to the analysis.

*** Hierarchical Clustering:

  ***Clustering Methodology:
  - Applied hierarchical clustering using `scipy.cluster.hierarchy`.
  - Created a dendrogram to visualize the clustering structure (`shc.dendrogram`).

  ***Cluster Identification:
  - Determined clusters using complete linkage (`linkage(x_scale_df, method="complete", metric="euclidean")`).
  - Assigned clusters using `cut_tree` and added cluster labels to the scaled data.

*** Principal Component Analysis (PCA):

  ***Dimensionality Reduction:**
  - Implemented PCA using `IncrementalPCA` to reduce the dimensionality of the dataset while retaining variance (`pca.fit_transform(x_scale)`).

  ***Visualization:
  - Plotted scatter plots to visualize relationships between variables after PCA (`sns.scatterplot`).

*** Insights and Visualizations:

  ***Hierarchical Clustering:
  - Identified clusters based on socio-economic indicators such as GDP, income, and mortality rates.
  - Visualized the dendrogram to understand the hierarchical structure of the data.

  ***PCA Analysis:
  - Reduced the dimensionality to 5 principal components and visualized relationships among variables.
  - Scatter plots helped visualize how countries grouped based on GDP, income, and mortality rates.

 **** Conclusion:
 
In conclusion, hierarchical clustering and PCA are powerful techniques for exploring patterns and relationships within socio-economic data. Hierarchical clustering revealed
natural groupings of countries based on similarity in socio-economic indicators. PCA facilitated dimensionality reduction and visualization of complex data relationships.
These techniques provide valuable insights into socio-economic similarities and disparities among countries, which can aid further analysis and policy-making.

Overall, this analysis provides a foundational understanding of how clustering and PCA can be applied to socio-economic data, offering insights into global economic trends 
and disparities among countries.
