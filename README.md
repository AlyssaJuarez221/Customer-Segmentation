![StoreSales (440 × 388 px)](https://user-images.githubusercontent.com/111559921/233491120-9ec8d472-d54e-4295-bccc-57a12a131c89.png)

# Customer Segmentation Analysis

**One Sentence Summary:** This repository aims to segment customers to better understand shopping behaviors using the dataset from [Customer Personality Analysis on Kaggle](https://www.kaggle.com/datasets/imakash3011/customer-personality-analysis).

## Overview

- **Objective:** The task is to segment customers based on their shopping behaviors, income, and demographics to tailor store offerings and marketing strategies effectively. This segmentation helps to ensure that stores are stocked with items that meet the needs of different customer groups, potentially increasing sales and customer satisfaction.
- **Approach:** We utilized unsupervised learning models, specifically K-Means, K-Modes, and Agglomerative Clustering, to group customers into distinct segments. The approach involved preprocessing the data by removing outliers, engineering new features, encoding categorical variables, and performing PCA for dimensionality reduction. This setup facilitated more efficient model processing and better clustering results.
- **Summary of Performance Achieved:** The K-Means model provided the most useful and interpretable clusters, revealing clear distinctions between customer groups. K-Modes and Agglomerative Clustering produced less informative results, with K-Modes replicating the Agglomerative Clustering results and Agglomerative Clustering providing more clusters than necessary.

## Summary of Workdone

- **Data:**
  - **Type:** CSV file containing 29 features related to customer demographics, spending habits, and other attributes.
  - **Size:** Original dataset had 2240 features, but analysis was based on 29 features. After cleaning, 2205 instances remained.
  - **Instances (Train, Test, Validation Split):** The entire dataset was used for clustering without a separate train/test split.

- **Preprocessing / Clean up:**
  - Removed null values and outliers, specifically addressing anomalies in age (e.g., 120 years old) and income (e.g., over 600K). This cleaning process reduced the dataset to 2205 instances.
  - Engineered new features including `Customer_For`, `Age`, `Spent`, `Adult`, `Children`, and `Household_Size`.
  - Encoded the categorical variable `Education` into numerical values (undergrad, grad, postgrad).
  - Applied PCA to reduce dimensionality and make the data more manageable for modeling.

- **Data Visualization:** Various visualizations were used to understand the distribution and characteristics of different customer segments. Detailed visualizations included the results of the clustering models.

## Problem Formulation

- **Input / Output:** Input features include demographic details, spending habits, and other relevant attributes. The output is customer segmentation into distinct groups.
- **Models:**
  - **K-Means:** Used 4 clusters. Performed efficiently with clear and actionable groupings:
    - **Group 1:** 20-65k income, highest spenders, mostly without kids, buys luxury items, majority of shoppers, coupon motivated.
    - **Group 2:** 20-80k income, 20-50 years old, spends the least, small new families, buys the least luxury items.
    - **Group 3:** Lowest income (10-50k), likely single-child matured families, buys luxury items.
    - **Group 4:** Largest income (0-100k), large families, less spending on luxury, coupon motivated, uses the most coupons per visit.
  - **Agglomerative Clustering:** Suggested 5 clusters, but resulted in less useful groupings:
    - **Group 1:** 0-80k income, second highest spenders, large family, purchases some luxury.
    - **Group 2:** 20-90k income, older family, buys more luxury, coupon motivated.
    - **Group 3:** Lowest income (0-50k), mostly young families, spends equally on grocery and luxury, buys cheaper meats.
    - **Group 4:** 30-100k income, older family, mainly purchases luxury items.
    - **Group 5:** 35-120k income, adults without kids, shops mainly at grocery stores, prefers groceries over luxury.
  - **K-Modes:** Results were identical to Agglomerative Clustering, indicating overlap in clustering results.

## Training

- **How the Models were Trained:** Models were implemented using Python libraries. Training involved applying each algorithm and evaluating cluster quality through visual inspection and clustering metrics.
- **Training Curves:** Not applicable as clustering does not involve training curves.
- **Stopping Criteria:** Based on the clarity and usefulness of clusters.
- **Difficulties:** Managing a large number of features and ensuring that clusters were meaningful and distinct.

## Performance Comparison

- **Key Performance Metrics:** Clarity of clusters, interpretability, and practical usefulness for marketing and store stocking.
- **Results:**
  - **K-Means:** Provided the most insightful and actionable clusters.
  - **Agglomerative Clustering and K-Modes:** Results were less distinct and overlapping.
- **Visualizations:** Included cluster distribution and characteristics for each model.

## Conclusions

- **Summary:** K-Means was the most effective model, providing the most useful and interpretable clusters. K-Modes and Agglomerative Clustering were less effective, with K-Modes results mirroring those of Agglomerative Clustering and Agglomerative Clustering resulting in less organized groups.

## Future Work

- **Next Steps:** Explore larger datasets and additional features to refine clusters and enhance segmentation accuracy. Consider evaluating other clustering algorithms and validation techniques to improve results.
- **Further Studies:** Investigate the impact of external data sources and additional features on customer segmentation.

## How to Reproduce Results

- **Instructions:** Follow the preprocessing steps described, apply K-Means, Agglomerative Clustering, and K-Modes models, and evaluate clusters based on visual and quantitative metrics.
- **Resources:** Recommended tools include Jupyter Notebook or Google Colab for running the analysis.

## Overview of Files in Repository

- **utils.py:** Functions for data cleaning and visualization.
- **preprocess.ipynb:** Handles data cleaning, feature engineering, and preprocessing.
- **visualization.ipynb:** Creates visualizations for data exploration and cluster analysis.
- **models.py:** Contains implementations of K-Means, Agglomerative Clustering, and K-Modes.
- **training-models.ipynb:** Executes clustering algorithms and evaluates results.
- **performance.ipynb:** Compares and visualizes clustering performance.

## Software Setup

- **Required Packages:** numpy, pandas, scikit-learn, matplotlib, seaborn.
- **Installation Instructions:** Install packages using pip (`pip install numpy pandas scikit-learn matplotlib seaborn`).

## Data

- **Download Link:** [Customer Personality Analysis Dataset](https://www.kaggle.com/datasets/imakash3011/customer-personality-analysis).
- **Preprocessing Steps:** Follow the cleaning, feature engineering, and PCA steps described in the preprocessing notebook.

## Citations

- Patel, Akash. “Customer Personality Analysis.” Kaggle, 22 Aug. 2021, [link](https://www.kaggle.com/datasets/imakash3011/customer-personality-analysis).
