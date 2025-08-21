# Customer Segmentation Using K-Means Clustering

## Project Overview
This project performs **customer segmentation** using the **K-Means clustering algorithm** based on customers' **Annual Income** and **Spending Score**. The goal is to identify distinct customer groups to support **targeted marketing, product optimization, and business strategy**.

The workflow is structured professionally, similar to a real-world ML project, with data exploration, preprocessing, cluster analysis, visualization, and predictions for new customers.

---

## Dataset
- **Source:** Mall_Customers.csv  
- **Features used:**
  - `Annual Income (k$)` – Customer income
  - `Spending Score (1-100)` – Customer spending behavior
- **Size:** [Add number of rows & columns]

**Sample data:**
| CustomerID | Annual Income (k$) | Spending Score (1-100) |
|------------|------------------|------------------------|
| 1          | 15               | 39                     |
| 2          | 15               | 81                     |
| 3          | 16               | 6                      |
| ...        | ...              | ...                    |

---

## Project Workflow

### 1. Data Understanding
- Displayed **first 5 rows** and **dataset info** using `df.head()` and `df.info()`.  
- Checked for **missing values** with `df.isnull().sum()`.

### 2. Feature Selection
- Selected **Annual Income** and **Spending Score** for clustering.  
- Converted data to NumPy array for K-Means.

### 3. Elbow Method
- Calculated **WCSS (Within-Cluster Sum of Squares)** for 1-10 clusters.  
- Plotted the **Elbow Graph** to determine the optimal number of clusters (5).

### 4. K-Means Clustering
- Applied **K-Means** with `n_clusters=5` and `init='k-means++'`.
- Assigned **cluster labels** to each customer.  
- Cluster labels were mapped to **descriptive names**:
  - Cluster 1: Average
  - Cluster 2: Premium
  - Cluster 3: Smart Savers
  - Cluster 4: Budget-Conscious
  - Cluster 5: Impulsive Buyers

### 5. Cluster Evaluation
- **Cluster Sizes:**
  - Average: 81  
  - Premium: 39  
  - Smart Savers: 35  
  - Budget-Conscious: 23  
  - Impulsive Buyers: 22  
- **Cluster Centroids:**
  | Cluster           | Annual Income | Spending Score |
  |------------------|---------------|----------------|
  | Average           | 55.30         | 49.52          |
  | Premium           | 86.54         | 82.13          |
  | Smart Savers      | 88.20         | 17.11          |
  | Budget-Conscious  | 26.30         | 20.91          |
  | Impulsive Buyers  | 25.73         | 79.36          |
- **Silhouette Score:** 0.5539 → moderately distinct clusters.

### 6. Visualization
- **Elbow Plot:** Identifies optimal clusters.  
- **Cluster Scatter Plot:** Visualizes all clusters with **descriptive labels** and **centroids in black**.

### 7. New Customer Prediction
- Example: `[[60, 50], [25, 80], [90, 20]]`  
- Predictions:  
  - Customer 1 → Average  
  - Customer 2 → Impulsive Buyers  
  - Customer 3 → Smart Savers  

---

## Key Insights
- Customers are grouped by **income and spending behavior**.  
- Marketing strategies can be **targeted per cluster**:  
  - **Premium:** High income, high spending → luxury products  
  - **Smart Savers:** High income, low spending → discount campaigns  
  - **Budget-Conscious:** Low income, low spending → affordable options  
  - **Impulsive Buyers:** Low income, high spending → bundle offers  
  - **Average:** Medium segment → general promotions  

---

## Tech Stack
- **Python 3.13**
- **Libraries:** pandas, numpy, matplotlib, seaborn, scikit-learn
- **Algorithm:** K-Means Clustering (Unsupervised ML)
- **Notebook:** Jupyter Notebook / Google Colab compatible

---

## How to Run
1. Clone the repository:  
```bash
git clone <repo_link>
````

2. Install dependencies:

```bash
pip install -r requirements.txt
```

3. Run the notebook:

```bash
jupyter notebook Customer_Segmentation.ipynb
```

4. Follow the notebook step-by-step to explore data, fit K-Means, visualize clusters, and predict new customers.

---

## Use Cases

* **Targeted Marketing & Promotions**
* **Customer Retention Programs**
* **Product & Pricing Strategy**
* **Revenue Forecasting & Business Insights**
* **Predicting Segments for New Customers**

---

## Notes

* Ensure the dataset `Mall_Customers.csv` is in the same directory.
* The notebook is **fully professional**, uses **descriptive labels, professional plots, and clean outputs** similar to industry standards.

---

