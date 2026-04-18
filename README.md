# Customer Segmentation using K-Means Clustering

## Project Overview
This project performs customer segmentation using the **Customer Purchasing Behaviors** dataset from Kaggle. The main goal is to group customers with similar purchasing patterns so that businesses can better understand customer behavior and design more targeted strategies.

The workflow follows a practical machine learning pipeline:
- loading the dataset from Kaggle inside Notebook
- checking and cleaning the data
- exploring customer behavior using charts
- preprocessing numeric and categorical features
- finding the best number of clusters
- building a K-Means clustering model
- interpreting the resulting customer segments
- saving the clustered output and trained files

## Problem Statement
Businesses often have customers with different income levels, purchase habits, loyalty levels, and shopping frequency. Treating all customers the same makes marketing less effective. This project uses unsupervised learning to divide customers into meaningful groups based on shared characteristics.

## Dataset
**Source:** Kaggle – Customer Purchasing Behaviors  
The dataset is downloaded directly in the notebook using `kagglehub`.

Main features used in the project:
- age
- annual_income
- purchase_amount
- purchase_frequency
- loyalty_score
- region

## Tools and Libraries
- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- KaggleHub
- Joblib

## Project Workflow

### 1. Data Loading
The dataset is downloaded from Kaggle and the CSV file is loaded into a Pandas DataFrame.

### 2. Data Understanding
Basic checks are performed:
- dataset shape
- column names
- data types
- missing values
- duplicate rows

### 3. Data Cleaning
Column names are standardized into a clean format. Missing values are handled and duplicate rows are removed.

### 4. Exploratory Data Analysis
The notebook studies the distribution of important variables and checks relationships such as:
- annual income vs purchase amount
- purchase frequency vs loyalty score

### 5. Feature Preparation
Relevant features are selected for clustering. Numerical columns are scaled and categorical columns are one-hot encoded using a preprocessing pipeline.

### 6. Choosing the Best Number of Clusters
The project tests multiple values of **k** and compares them using:
- Elbow Method
- Silhouette Score

### 7. Model Building
A final K-Means model is trained using the selected value of **k**, and each customer is assigned a cluster label.

### 8. Cluster Analysis
The average values of important features are calculated for each cluster. This helps describe the behavior of every customer segment.

### 9. Visualization
PCA is used to reduce the processed feature space into 2 dimensions so the clusters can be visualized clearly.

### 10. Business Interpretation
Each cluster is given a simple human-readable segment name based on spending, purchase frequency, and loyalty patterns.

### 11. Output Saving
The notebook saves:
- clustered customer dataset
- cluster profile table
- trained K-Means model
- preprocessing pipeline
- metadata file

## Output Files
After running the notebook, the following files are saved inside the output folder:
- `customer_segments.csv`
- `cluster_profile.csv`
- `kmeans_model.joblib`
- `preprocessor.joblib`
- `metadata.json`

## Expected Outcome
At the end of the project, customers are grouped into meaningful segments that can support:
- targeted marketing
- customer retention planning
- loyalty improvement strategies
- better business decision-making

## Conclusion
This project shows how unsupervised learning can be used to understand customer purchasing behavior in a simple and practical way. By combining EDA, preprocessing, K-Means clustering, and business interpretation, the notebook produces a complete end-to-end customer segmentation workflow suitable for learning and demonstration.
