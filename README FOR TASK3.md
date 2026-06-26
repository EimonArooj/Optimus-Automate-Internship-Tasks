# Customer Segmentation using K-Means Clustering Report

## Project Overview

This project applies the **K-Means Clustering** algorithm to segment customers based on their purchasing behavior using **RFM (Recency, Frequency, Monetary)** analysis. The objective is to group customers with similar characteristics, enabling businesses to better understand customer value and develop targeted marketing strategies.

## Data Preprocessing

The dataset was cleaned by removing records with missing **Customer IDs**, invalid **Invoice Dates**, and transactions containing non-positive quantities or unit prices. This ensured that only valid customer transactions were used for analysis.

## Feature Engineering

Three RFM features were created for each customer:

* **Recency:** Number of days since the customer's last purchase.
* **Frequency:** Number of unique purchases made by the customer.
* **Monetary:** Total amount spent by the customer.

Since these features have different scales, **Min-Max Scaling** was applied to normalize the data before clustering.

## Model Development

The **Elbow Method** was used to determine the optimal number of clusters by analyzing the Within-Cluster Sum of Squares (WCSS). Based on the results, **K = 2** was selected, and the K-Means algorithm was applied to divide customers into two segments:

* **High-Value Customers**
* **Low-Value Customers**

The trained K-Means model and Min-Max Scaler were saved using **Pickle** for future predictions and deployment.

## Key Findings

* Customers were successfully grouped based on their purchasing behavior using RFM analysis.
* **High-Value Customers** generally have recent purchases, higher purchase frequency, and greater overall spending.
* **Low-Value Customers** tend to purchase less frequently, spend less money, or have not made purchases recently.
* The generated customer segments can support personalized marketing campaigns, customer retention strategies, and business decision-making.

## Conclusion

The K-Means clustering model successfully segmented customers into meaningful groups using RFM features. These insights enable businesses to identify their most valuable customers, improve customer engagement, and optimize marketing efforts through targeted promotional strategies.
