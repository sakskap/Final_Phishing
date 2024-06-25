# Final_Phishing
Final Submission for Unsupervised learning Course CU Boulder 
# Phishing URL Detection

This repository contains the analysis and model-building process for detecting phishing URLs using the PhiUSIIL Phishing URL Dataset. The dataset was introduced in the paper "PhiUSIIL: A diverse security profile empowered phishing URL detection framework based on similarity index and incremental learning" by Arvind Prasad and Shalini Chandra.

## Dataset

The dataset includes 134,850 legitimate and 100,945 phishing URLs, with features derived from the URL and webpage source code. It is available in the file `phishing.csv`.

## Project Structure

- `phishing.csv`: The dataset used for analysis and model building.
- `notebook.ipynb`: The Jupyter notebook containing all the analysis, model training, and evaluation steps.
- `README.md`: This readme file.

## Analysis and Methods

### Data Loading and Preliminary Analysis

- **Loading Data**: The dataset is loaded using the pandas library.
- **Initial Exploration**: Display the first few entries and summary statistics to understand the data structure and feature types.
- **Missing Values**: Check for and handle any missing values.

### Unsupervised Learning

- **Clustering and PCA**: Apply clustering and PCA to identify patterns and group similar URLs without using labels. This helps enhance cybersecurity by differentiating legitimate from phishing URLs.

### Feature Selection

- **Importance**: Feature selection improves model performance by removing irrelevant data, reducing overfitting, and improving accuracy.
- **Normalization**: Numerical columns are normalized using StandardScaler.

### Encoding Categorical Data

- **Transformation**: Categorical data, such as the 'TLD' column, is converted to numerical codes using LabelEncoder.

### Dimensionality Reduction with PCA

- **PCA Application**: Reduce the dataset's dimensions while preserving 95% of its variance, reducing computational cost and mitigating issues like the curse of dimensionality.

### Optimal Number of Clusters with Elbow Method

- **Elbow Method**: Determine the optimal number of clusters for K-Means clustering by plotting inertia against the number of clusters.

### Clustering with K-Means

- **K-Means Clustering**: Apply K-Means clustering to the PCA-reduced data to understand the inherent groupings within the phishing dataset.

### Cluster Centers and Detailed Statistics

- **Examination**: Examine cluster centroids and detailed statistics to understand the defining characteristics of each cluster.

### Logistic Regression Model

- **Supervised Learning**: Train a logistic regression model to accurately predict phishing websites using labeled data.
- **Model Evaluation**: Evaluate the model's performance using metrics like accuracy, precision, and recall.

## Conclusion

Combining logistic regression with clustering offers a robust system for phishing detection. Logistic regression ensures high accuracy, while clustering helps identify new patterns, providing an effective, adaptive approach to cybersecurity.

## Results

- **Purity Score**: Achieved a high purity score of 0.9955, indicating that the clusters closely correspond to the actual labels.
- **Logistic Regression Performance**: High accuracy, precision, and recall in predicting phishing URLs.
