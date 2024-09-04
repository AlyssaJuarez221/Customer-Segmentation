![StoreSales (440 × 388 px)](https://user-images.githubusercontent.com/111559921/233491120-9ec8d472-d54e-4295-bccc-57a12a131c89.png)

# Customer Segmentation Analysis

**One Sentence Summary:** This repository aims to segment customers to better understand shopping behaviors using the dataset from [Customer Personality Analysis on Kaggle](https://www.kaggle.com/datasets/imakash3011/customer-personality-analysis).

## Overview

- **Definition of the Tasks / Challenge:** The task is to segment customers to identify distinct groups based on shopping behaviors, income, and demographics, enabling targeted marketing strategies and product offerings.
- **Your Approach:** We used unsupervised learning models, including K-Means, K-Modes, and Agglomerative Clustering, to categorize customers into meaningful groups. Data preprocessing involved feature engineering, scaling, and dimensionality reduction to improve model performance and interpretability.
- **Summary of Performance Achieved:** The K-Means model provided the most insightful and well-organized clusters. K-Modes and Agglomerative Clustering yielded less useful results due to less clear group distinctions and overlap in clustering outcomes.

## Summary of Workdone

- **Data:**
  - **Type:** CSV file with 29 features related to customer demographics, spending habits, and other attributes.
  - **Size:** Original dataset contained 2240 features, reduced to 29 for analysis. Post-cleaning, the dataset had 2205 instances.
  - **Instances (Train, Test, Validation Split):** Entire dataset used for clustering with no separate train/test split.

- **Preprocessing / Clean up:** Removed null values and outliers (e.g., age > 120, income > 600K). Created new features such as Customer_For, Age, Spent, Adult, Children, and Household_Size. Encoded categorical variables and performed PCA for dimensionality reduction.

- **Data Visualization:** Visualized clusters using graphs to understand the distribution and characteristics of each segment.

## Problem Formulation

- **Input / Output:** Input features include customer demographics, spending habits, and other attributes. Output is customer segmentation into distinct groups.
- **Models:**
  - **K-Means:** Chose 4 clusters; provided well-organized groups with actionable insights.
  - **Agglomerative Clustering:** Used 5 clusters; results were less organized and detailed.
  - **K-Modes:** Results were identical to Agglomerative Clustering, showing overlap in clustering results.
- **Loss, Optimizer, Other Hyperparameters:** Details of hyperparameters used for each model were adjusted based on validation results.

## Training

- **How You Trained:** Implemented models using Python libraries. Training involved running each algorithm and evaluating cluster quality through visual and quantitative assessments.
- **Training Curves:** Not applicable as clustering does not involve training curves.
- **Stopping Criteria:** Based on cluster validity and interpretability.
- **Difficulties:** Handling large number of features and ensuring meaningful cluster separation.

## Performance Comparison

- **Key Performance Metrics:** Clarity of clusters, interpretability, and usefulness for targeted marketing.
- **Results:**
  - **K-Means:** Best performance with clear and actionable clusters.
  - **Agglomerative Clustering and K-Modes:** Provided less useful results with overlapping clusters.
- **Visualizations:** Included cluster distribution and characteristics.

## Conclusions

- **Summary:** K-Means was the most effective model for segmenting customers, providing the best insights into shopping behaviors. K-Modes and Agglomerative Clustering were less effective, with overlapping or less distinct clusters.

## Future Work

- **Next Steps:** Use larger datasets to refine clusters and improve segmentation accuracy. Explore other clustering algorithms and validation techniques.
- **Further Studies:** Investigate additional features and external data sources to enhance customer understanding and segmentation.

## How to Reproduce Results

- **Instructions:** Follow the preprocessing steps outlined, apply K-Means, Agglomerative Clustering, and K-Modes models, and evaluate clusters based on the provided metrics.
- **Resources:** Recommended platforms include Jupyter Notebook or Google Colab for running the analysis.

## Overview of Files in Repository

- **utils.py:** Functions for data cleaning and visualization.
- **preprocess.ipynb:** Handles data cleaning, feature engineering, and preprocessing.
- **visualization.ipynb:** Creates visualizations for data exploration and cluster analysis.
- **models.py:** Contains implementations of K-Means, Agglomerative Clustering, and K-Modes.
- **training-models.ipynb:** Runs clustering algorithms and evaluates results.
- **performance.ipynb:** Compares and visualizes clustering performance.

## Software Setup

- **Required Packages:** numpy, pandas, scikit-learn, matplotlib, seaborn.
- **Installation Instructions:** Install packages using pip (`pip install numpy pandas scikit-learn matplotlib seaborn`).

## Data

- **Download Link:** [Customer Personality Analysis Dataset](https://www.kaggle.com/datasets/imakash3011/customer-personality-analysis).
- **Preprocessing Steps:** Follow cleaning, feature engineering, and PCA steps as described in the preprocessing notebook.

## Training

- **Training Instructions:** Apply clustering algorithms as detailed in the training notebook.

## Performance Evaluation

- **Evaluation Instructions:** Use visualization and comparison metrics to assess clustering quality.

## Citations

- Patel, Akash. “Customer Personality Analysis.” Kaggle, 22 Aug. 2021, [link](https://www.kaggle.com/datasets/imakash3011/customer-personality-analysis).
