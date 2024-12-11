# Reducing Traffic Fatalities Through Data Science and ML
This project focuses on analyzing traffic accident data to develop strategies for reducing traffic-related fatalities in the United States. Using data wrangling, visualization, dimensionality reduction, and unsupervised clustering techniques, we aim to identify patterns and provide actionable insights for policymakers.
![Traffic dara science](https://github.com/user-attachments/assets/02ac7bae-f735-4275-845e-1878b02d4467)

## Project Objectives
1. Understand the variation in traffic accident demographics across states.
2. Group states with similar profiles to guide targeted interventions.
3. Use data-driven methods to recommend cost-effective and focused policy actions.

## Dataset
The dataset includes the following columns:
- `state`: U.S. state names.
- `drvr_fatl_col_bmiles`: Number of drivers involved in fatal collisions per billion miles.
- `perc_fatl_speed`: Percentage of fatal collisions caused by speeding.
- `perc_fatl_alcohol`: Percentage of fatal collisions caused by alcohol impairment.
- `perc_fatl_1st_time`: Percentage of drivers involved in fatal collisions who had no prior accidents.

## Steps and Methods
### 1. Data Overview
- **Input File:** `datasets/road-accidents.csv`
- Loaded and summarized using Python's pandas library.
- Dataset dimensions: 51 rows and 5 columns.

### 2. Data Visualization
- Summary statistics generated for all columns.
- Pairwise scatter plots were created using `seaborn` to explore relationships between variables.

### 3. Correlation Analysis
- Computed Pearson correlation coefficients to quantify relationships between features and target variables.
- Identified alcohol impairment as the most strongly correlated feature with traffic fatalities.

### 4. Multivariate Linear Regression
- Built a regression model to assess the relationship between features and the target variable (`drvr_fatl_col_bmiles`), adjusting for interactions between features.

### 5. Principal Component Analysis (PCA)
- Standardized features for dimensionality reduction.
- Reduced data to two principal components, capturing ~79% of the total variance.
- Visualized states in the reduced dimensional space.

### 6. Clustering Analysis
- Applied KMeans clustering to group states into three clusters.
- Used a scree plot to determine the optimal number of clusters.
- Visualized clusters in the PCA scatter plot.

### 7. Feature Comparison Between Clusters
- Analyzed differences in speeding, alcohol influence, and first-time accidents between clusters using violin plots.

### 8. Policy Recommendations
- Incorporated additional data on miles driven to compute total fatal accidents for each state.
- Provided insights into which cluster should be prioritized for interventions.

## Tools and Libraries
- **Python Libraries:** pandas, seaborn, matplotlib, sklearn
- **Techniques Used:** Data wrangling, correlation analysis, linear regression, PCA, KMeans clustering, data visualization.

## Key Findings
- States with higher percentages of alcohol-impaired accidents require targeted interventions.
- PCA and clustering revealed distinct groups of states, suggesting tailored strategies for each cluster.
- Combining accident rates with miles driven helps prioritize clusters for policy action.

## Visualizations
1. Pairwise scatter plots of variables.
2. PCA scree plot and scatter plot of principal components.
3. Clustering visualizations with KMeans.
4. Violin plots comparing feature distributions across clusters.

## Future Work
- Explore additional features like weather, road conditions, or enforcement policies.
- Test more advanced clustering methods, such as hierarchical clustering or DBSCAN.
- Develop predictive models to assess the impact of potential interventions.


