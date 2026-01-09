# E-Commerce Customer RFM Segmentation and K-Means Clustering

## Project Overview
This project aims to understand customer purchasing behavior through data-driven segmentation, combining **classic RFM analysis** with **K-means clustering**. The goal is not only to identify high- and low-value customers, but also to uncover behavioral patterns that support actionable business decisions in retention, reactivation, and market expansion.

## Problem Statement
In order to diversify and optimize marketing strategies and ultimately increase sales for the company, this project aims to:
* Identify distinct customer segments based on purchasing behavior
* Translate segmentation results into actionable business insights

## Dataset
The dataset includes transaction-level customer data between 2010 and 2011 from a UK-based online retailer, sourced from the [UCI Machine Learning Repository](http://archive.ics.uci.edu/ml/index.php).

Variable | Description
:--- | :---
**InvoiceNo** | Invoice number. Each corresponds to a unique transaction.
**StockCode** | Product code. Each corresponds to a unique product.
**Description** | Description of each product.
**Quantity** | Quantity of each product in a transaction.
**InvoiceDate** | Date and time of transaction.
**UnitPrice** | Unit price of the product.
**CustomerID** | Customer ID. Each corresponds to a unique customer.
**Country** | Country of the transaction.

## Methodology
The analysis follows a structured pipeline:

**1. Data Cleaning & Preparation**
  * Handling missing values, duplicates, anomalies and outliers

**2. Exploratory Data Analysis (EDA)**
  * Exploring top-sellers, geographic distribution, seasonality, revenue concentration and cancellation patterns

**3. RFM Analysis**
  * Transforming transaction-level data into a customer-centric dataset
  * Scoring customers on Recency, Frequency, and Monetary value
  * Segmenting customers into distinct groups (e.g. Champions, Churn Risks, Low-value, etc.)

**4. K-Means Clustering**
  * Feature engineering and scaling
  * Evaluating cluster quality using inertia and silhouette scores
  * Analyzing and profiling each cluster to develop marketing strategies and business recommendations

## Results
* **The RFM analysis** identifies seven distinct customer segments: Champions (30%), High-value churn risks (10%), New and promising customers (14%), Low frequency big spenders (10%), Frequent low spenders (6%) and Low-value customers (10%).
* **K-means clustering** uncovers three behaviorally distinct customer groups, which can be characterized as Core loyal customers (48.5%), Low-engagement/ dormant UK customers (41.9%), and High-value non-UK customers (9.6%).

## Business Recommendations
* Prioritize retention and experience optimization for **core loyal customers** and **champions**.
* Use targeted reactivation strategies for **high-value churn risks**.
* Develop onboarding strategies for **new and promising customers** to transform them into high-value segments.
* Tailor cross-border and region-sepecific marketing campaigns for **high-value non-UK customers**
* Avoid over-investing in consistently **low-value segments**.

## Next Steps
* **More thorough data cleaning**: The relationship between StockCode and Description is not strictly one-to-one, which may introduce noise in product-level analysis. Future work could further standardize StockCode and enhance Description consistency
* **Business-informed refinement of RFM segmentation**: RFM segmentation could be further refined by deeper understanding of business context to better reflect real-world operational and marketing needs.
* **Exploration of alternative clustering approaches**: Beyond K-means, other clustering techniques such as DBSCAN or Gaussian Mixture Models could be explored. Comparing multiple models may lead to more robust and interpretable customer groupings.

## Tech Stack
* Python (Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn)
* Jupyter Notebook

## File Descriptions
* `E-Commerce.ipynb`: Jupyter notebook containing all the codes of the project.
* `data.csv`: CSV file containing the dataset
* `README.md`: This file, providing an overview of the project
