# Credit Card Customer Segmentation 💳

A comprehensive data science project that segments credit card customers using K-means clustering to enable targeted business strategies and improve customer relationship management.

## 🎯 Project Overview

This project analyzes a dataset of 10,127 credit card customers to identify distinct customer segments based on their transaction behavior, demographics, and credit utilization patterns. The segmentation enables banks to:

- Apply different business strategies to each customer group
- Provide higher credit limits for high-usage, low-spending customers
- Offer targeted incentives to high-income, low-activity customers
- Optimize marketing campaigns and customer retention strategies

## 📊 Dataset Description

The dataset contains 14 features for each customer:

| Feature | Description |
|---------|-------------|
| `customer_id` | Unique identifier for each customer |
| `age` | Customer age in years |
| `gender` | Customer gender (M or F) |
| `dependent_count` | Number of dependents |
| `education_level` | Education level (High School, Graduate, etc.) |
| `marital_status` | Marital status (Single, Married, etc.) |
| `estimated_income` | Estimated annual income |
| `months_on_book` | Time as customer in months |
| `total_relationship_count` | Number of customer-company interactions |
| `months_inactive_12_mon` | Inactive months in last 12 months |
| `credit_limit` | Customer's credit limit |
| `total_trans_amount` | Total transaction amount |
| `total_trans_count` | Total number of transactions |
| `avg_utilization_ratio` | Average daily utilization ratio |

## 🔍 Key Findings

### Customer Segments Identified

The analysis revealed **6 distinct customer clusters**:

| Cluster | Size | Key Characteristics |
|---------|------|-------------------|
| **Cluster 1** | 16.5% | High-income customers ($114K avg) with moderate transaction activity |
| **Cluster 2** | 7.3% | Divorced customers with moderate spending patterns |
| **Cluster 3** | 28.6% | Single customers with average income and transaction behavior |
| **Cluster 4** | 7.3% | Unknown marital status, moderate activity |
| **Cluster 5** | 31.7% | Married customers with lower income, high utilization |
| **Cluster 6** | 8.6% | **High-value customers**: Highest transaction amounts and frequency, low utilization ratio |

### Key Insights

- **Cluster 6** represents premium customers with high spending but efficient credit usage
- **Income varies significantly** across clusters (from $46K to $115K average)
- **Transaction patterns** are the primary differentiating factor
- **Gender distribution** shows female customers concentrated in Clusters 3 and 5
- **Educational background** is fairly distributed across all segments

## 🛠️ Technical Implementation

### Libraries Used
```python
import pandas as pd
import numpy as np
import seaborn as sns
import matplotlib.pyplot as plt
from sklearn.cluster import KMeans
from sklearn.preprocessing import StandardScaler
```

### Methodology

1. **Exploratory Data Analysis (EDA)**
   - Statistical summaries and distributions
   - Correlation analysis
   - Missing value assessment

2. **Feature Engineering**
   - Binary encoding for gender
   - Ordinal encoding for education levels
   - One-hot encoding for marital status
   - Standard scaling for numerical features

3. **Model Selection**
   - Elbow method to determine optimal number of clusters
   - K-means clustering with k=6
   - Silhouette analysis for validation

4. **Results Analysis**
   - Cluster profiling and characterization
   - Business implications assessment
   - Visualization of customer segments

## 📈 Model Performance

- **Optimal Clusters**: 6 (determined via elbow method)
- **Feature Scaling**: StandardScaler applied to all numerical features
- **Key Differentiating Features**:
  - `estimated_income`
  - `credit_limit`
  - `total_trans_amount`
  - `total_trans_count`
  - `avg_utilization_ratio`

## 🚀 Business Applications

### Recommended Strategies by Cluster

**Cluster 1 (High-Income, Moderate Activity)**
- Premium product offerings
- Exclusive rewards programs
- Higher credit limit increases

**Cluster 6 (High-Value Transactors)**
- VIP customer treatment
- Cashback incentives
- Premium customer service

**Cluster 5 (High-Utilization Married)**
- Financial planning services
- Balance transfer offers
- Credit counseling programs

## 📊 Visualizations

The project includes comprehensive visualizations:
- Elbow curve for optimal cluster selection
- Pair plots showing cluster separation
- Distribution plots for key features
- Correlation heatmaps
- Cluster profile comparisons
