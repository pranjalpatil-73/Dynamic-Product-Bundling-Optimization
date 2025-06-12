# Dynamic-Product-Bundling-Optimization


# Dynamic Bundling for Increased Average Order Value (AOV) Optimization

This project presents an end-to-end machine learning solution designed to optimize Average Order Value (AOV) by dynamically recommending product bundles. It leverages customer segmentation and association rule mining to identify popular product combinations and tailor recommendations to individual customer behaviors, ultimately enhancing sales and customer satisfaction.

## Features

### Comprehensive Data Preprocessing

* Handles missing customer IDs.
* Converts date fields to datetime objects.
* Removes invalid quantities and unit prices.
* Engineers new features such as TotalPrice and time-based attributes (Year, Month, Day, DayOfWeek, Hour) from transaction data.

### Exploratory Data Analysis (EDA)

* Visualizes top-selling products.
* Analyzes total sales by country.
* Displays monthly sales trends.

### Advanced Customer Segmentation (RFM + K-Means)

* Calculates Recency, Frequency, and Monetary (RFM) values.
* Applies StandardScaler to RFM features.
* Uses the Elbow Method to determine optimal number of customer segments.
* Applies K-Means clustering.
* Visualizes customer segments in 3D space.

### Association Rule Mining (Apriori Algorithm)

* Transforms transactional data using one-hot encoding.
* Identifies frequent itemsets.
* Generates association rules using metrics like lift and confidence.

### Dynamic Bundling Recommendation Engine

* Combines segmentation with association rules.
* Personalized recommendations based on customer\_id and purchased\_items.
* Filters out already purchased items from recommendations.

## Technologies Used

* **Python**: Core language.
* **Pandas**: Data manipulation.
* **NumPy**: Numerical operations.
* **Matplotlib & Seaborn**: Visualizations.
* **mlxtend**: Apriori algorithm and preprocessing.
* **Scikit-learn**: KMeans, StandardScaler.

## Getting Started

### Prerequisites

* Python 3.7 or higher.
* Jupyter Notebook or JupyterLab.

### Installation

1. **Download the Notebook**:

   * File: `Dynamic Bundling for Increased AOV Optimizationipynb.ipynb`
2. **Download the Dataset**:

   * File: `Online Retail.csv`
   * Ensure it's in the same directory or update the data loading path in the notebook.

```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
pip install pandas numpy matplotlib seaborn mlxtend scikit-learn
```

## Usage

### Open the Notebook

```bash
jupyter notebook "Dynamic Bundling for Increased AOV Optimizationipynb.ipynb"
```

### Run All Cells

* Load and clean data.
* Perform EDA.
* Segment customers using RFM and K-Means.
* Apply Apriori algorithm.
* Run bundling recommendation engine.

### Get Bundle Recommendations

```python
# Example
customer_id_example = 17850.0
purchased_items_example = ['WHITE HANGING HEART T-LIGHT HOLDER', 'WHITE METAL LANTERN']

recommended_bundles = recommend_bundle(customer_id_example, purchased_items_example)
print(f"Recommended Bundles for Customer {int(customer_id_example)}:")
if recommended_bundles:
    for bundle in recommended_bundles:
        print(f"- {bundle}")
else:
    print("No specific bundle recommendations at this time.")
```

## Screenshots/Demo

(Embed charts or output screenshots if available.)

## Future Enhancements

* Real-time API integration.
* A/B testing framework.
* Simple web interface.
* Advanced clustering (e.g., DBSCAN, Deep Learning).
* Time-series forecasting for inventory optimization.

## Contact

\[Pranjal Patil] - \[(https://www.linkedin.com/in/pranjal-patil07/)]

Project Link: \[(https://github.com/pranjalpatil-73/Dynamic-Product-Bundling-Optimization)]
