# 🛒 E-Commerce Customer Segmentation Using Machine Learning

## 📌 Project Overview

This project focuses on segmenting e-commerce customers based on their purchasing behavior using **K-Means and DBSCAN clustering algorithms**.

The project uses the RFM (Recency, Frequency, Monetary) model to understand customer behavior, applies PCA for dimensionality reduction, and uses t-SNE to visualize customer segments. Finally, actionable marketing personas are derived to help businesses improve customer retention, engagement, and sales.

## 🎯 Objectives

* Analyze customer purchasing behavior using RFM analysis.
* Segment customers using K-Means clustering.
* Identify customer groups and potential outliers using DBSCAN.
* Apply Principal Component Analysis (PCA) for dimensionality reduction.
* Visualize customer segments using t-SNE.
* Evaluate clustering performance using the Silhouette Score.
* Develop actionable marketing personas for different customer segments.

## 📊 Dataset

**Dataset Name:** Online Retail Dataset

**Source:** UCI Machine Learning Repository

**Download Dataset:** https://archive.ics.uci.edu/static/public/352/online+retail.zip

The dataset contains transactions from a UK-based online retailer between December 2010 and December 2011.

It includes approximately 541,909 transaction records.

### Dataset Features

| Feature     | Description                              |
| ----------- | ---------------------------------------- |
| InvoiceNo   | Unique transaction or invoice identifier |
| StockCode   | Unique product identifier                |
| Description | Product description                      |
| Quantity    | Number of items purchased                |
| InvoiceDate | Date and time of the transaction         |
| UnitPrice   | Price per item                           |
| CustomerID  | Unique customer identifier               |
| Country     | Customer's country                       |

**Note:** The dataset contains missing customer IDs, cancelled transactions, and returns. These are handled during preprocessing.

## 🛠️ Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* Google Colab
* Jupyter Notebook

## 🧠 Methodology

### 1. Data Collection

Download the Online Retail dataset from the UCI Machine Learning Repository.

### 2. Data Preprocessing

* Handle missing customer IDs.
* Remove cancelled transactions.
* Filter invalid quantities and prices.
* Convert transaction dates into datetime format.
* Calculate the total transaction amount.

### 3. RFM Analysis

Three customer-level features are calculated:

* **Recency:** Number of days since the customer's most recent purchase. Lower values indicate more recent activity.
* **Frequency:** Number of distinct invoices associated with the customer.
* **Monetary:** Total amount spent by the customer.

### 4. Feature Transformation and Scaling

Apply logarithmic transformation to reduce skewness and use RobustScaler to scale RFM features.

### 5. K-Means Clustering

Use the Elbow Method to help select the number of clusters and segment customers according to their RFM characteristics.

### 6. DBSCAN Clustering

Apply density-based clustering to identify customer groups and detect potential noise points or outliers.

### 7. Dimensionality Reduction Using PCA

Reduce the three RFM features to two principal components for visualization.

### 8. Customer Visualization Using t-SNE

Project customer data into two dimensions to visualize local patterns and relationships between customer segments.

### 9. Model Evaluation

Evaluate the clustering results using the Silhouette Score, cluster sizes, and RFM profiles.

### 10. Marketing Persona Development

Interpret customer segments and recommend targeted marketing strategies.

## 📈 Expected Marketing Personas

The actual personas depend on the clusters discovered in the dataset.

| Customer Persona     | Characteristics                                      | Marketing Strategy                          |
| -------------------- | ---------------------------------------------------- | ------------------------------------------- |
| Champions            | Recent purchases, frequent orders, high spending     | VIP rewards and exclusive offers            |
| Loyal Customers      | Frequent and relatively recent purchases             | Loyalty programs and referral rewards       |
| Potential Loyalists  | Promising spending or engagement but fewer purchases | Personalized recommendations                |
| At-Risk Customers    | Customers who have not purchased recently            | Win-back campaigns and targeted discounts   |
| Developing Customers | Lower engagement or spending                         | Introductory offers and relevant promotions |

These personas are illustrative examples. Final labels should be assigned after examining the actual cluster profiles.

## 📊 Visualizations

The project includes:

* Elbow Method plot for selecting K-Means cluster count.
* K-Means customer segmentation using PCA.
* DBSCAN customer segmentation using PCA.
* K-Means cluster visualization using t-SNE.
* DBSCAN cluster visualization using t-SNE.
* Cluster summaries based on Recency, Frequency, and Monetary value.

## 📏 Evaluation Metrics

**Silhouette Score:** Measures how well customers fit within their assigned clusters compared with other clusters.

Additional interpretation includes:

* Cluster sizes and balance.
* Differences in RFM characteristics.
* DBSCAN noise-point proportion.
* Practical usefulness of the resulting customer segments.

## 💼 Business Applications

This project can help e-commerce businesses:

* Identify valuable and loyal customers.
* Improve customer retention.
* Create personalized marketing campaigns.
* Identify inactive customers who may need re-engagement.
* Design targeted promotions.
* Improve customer relationship management.

## 🚀 How to Run the Project

### Step 1: Download the Dataset

Download the dataset from the official UCI link:

https://archive.ics.uci.edu/static/public/352/online+retail.zip

Extract the ZIP file to obtain `Online Retail.xlsx`.

### Step 2: Open Google Colab

Visit https://colab.research.google.com/

Create a new notebook.

### Step 3: Upload the Dataset

Upload `Online Retail.xlsx` using the Files panel in Google Colab.

### Step 4: Install Dependencies

```python
!pip install pandas numpy matplotlib seaborn scikit-learn openpyxl
```

### Step 5: Load the Dataset

```python
import pandas as pd

df = pd.read_excel('/content/Online Retail.xlsx')

print(df.head())
print(df.shape)
print(df.info())
```

### Step 6: Run the Analysis

Execute the notebook cells in order to perform data preprocessing, RFM analysis, clustering, dimensionality reduction, visualization, and marketing persona development.

## 📁 Suggested Project Structure

```text
ecommerce-customer-segmentation/
│
├── README.md
├── Online Retail.xlsx
├── customer_segmentation.ipynb
├── customer_segmentation_results.csv
│
└── visualizations/
    ├── elbow_method.png
    ├── kmeans_pca.png
    ├── dbscan_pca.png
    ├── kmeans_tsne.png
    └── dbscan_tsne.png
```

The CSV and visualization files will be generated when you save the corresponding outputs from your notebook.

## 🔮 Future Improvements

* Compare additional clustering algorithms.
* Tune DBSCAN parameters using neighborhood-distance analysis.
* Develop automated customer persona labeling.
* Build an interactive customer segmentation dashboard.
* Analyze customer purchasing patterns over time.
* Integrate customer lifetime value estimation.

## 📝 Conclusion

This project demonstrates how unsupervised machine learning can transform raw e-commerce transactions into meaningful customer segments.

By combining RFM analysis, K-Means, DBSCAN, PCA, and t-SNE, businesses can better understand customer behavior and develop data-driven marketing strategies.

## 📚 References

1. Chen, D. (2015). *Online Retail*. UCI Machine Learning Repository.
2. Dataset: https://doi.org/10.24432/C5BW33
3. Scikit-learn documentation: https://scikit-learn.org/

## 📄 License and Attribution

The Online Retail dataset is distributed under the **Creative Commons Attribution 4.0 International (CC BY 4.0)** license. Please credit the original dataset source when using or redistributing it.

Dataset attribution: Chen, D. (2015). Online Retail. UCI Machine Learning Repository. https://doi.org/10.24432/C5BW33
