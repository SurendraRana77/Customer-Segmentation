# Customer Segmentation Using K-Means Clustering

A beginner-friendly machine learning project that groups mall customers according to their **annual income** and **spending score** using the K-Means clustering algorithm.

## Project Overview

Businesses have customers with different spending habits. Customer segmentation helps identify groups with similar characteristics so that marketing teams can explore more relevant campaigns and offers.

This project uses unsupervised machine learning to discover customer groups from the Mall Customer Segmentation dataset.

## Objectives

- Explore and understand customer data.
- Visualize customer demographics and spending patterns.
- Apply K-Means clustering to annual income and spending score.
- Use the Elbow Method and silhouette score to assess cluster choices.
- Visualize clusters and centroids.
- Summarize customer groups and export the cluster assignments.

## Dataset

**Dataset:** Mall Customer Segmentation Data  
**File:** `Mall_Customers.csv`  
**Records:** 200 customers  
**Columns:** 5

| Column | Description |
|---|---|
| `CustomerID` | Unique customer identifier |
| `Gender` | Recorded gender category |
| `Age` | Customer age |
| `Annual Income (k$)` | Annual income in thousands of dollars |
| `Spending Score (1-100)` | Mall-assigned score representing spending behaviour |

The model uses **Annual Income (k$)** and **Spending Score (1-100)** as its main features. `CustomerID` is excluded because it is an identifier, not a customer behaviour feature. Gender and age are used for exploratory analysis.

### Dataset source

- Kaggle notebook/reference: https://www.kaggle.com/code/kushal1996/customer-segmentation-k-means-analysis

Download the dataset from the source and place `Mall_Customers.csv` in the project folder, or upload it when running the notebook in Google Colab.

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook / Google Colab

## Project Workflow

1. Import the required libraries.
2. Load the dataset.
3. Inspect the data and check for missing values and duplicates.
4. Perform exploratory data analysis (EDA).
5. Visualize gender, age, income, and spending-score distributions.
6. Select annual income and spending score for clustering.
7. Standardize the selected features using `StandardScaler`.
8. Use the Elbow Method to inspect inertia for different values of K.
9. Calculate silhouette scores to assess cluster separation.
10. Fit the final K-Means model with **K = 5**.
11. Visualize clusters and centroids.
12. Review cluster profiles and export the segmented dataset.

## How to Run

### Option 1: Google Colab

1. Download `Customer_Segmentation_KMeans.ipynb` from this repository.
2. Open https://colab.research.google.com/.
3. Select **File → Upload notebook** and upload the `.ipynb` file.
4. Run the notebook cells from top to bottom.
5. If the dataset does not load automatically, upload `Mall_Customers.csv` when prompted.

### Option 2: Run locally

1. Clone this repository:

   ```bash
   git clone https://github.com/SurendraRana77/Customer-Segmentation.git
   cd Customer-Segmentation
   ```

2. Create and activate a virtual environment (optional but recommended):

   **Windows**
   ```bash
   python -m venv .venv
   .venv\Scripts\activate
   ```

   **macOS / Linux**
   ```bash
   python3 -m venv .venv
   source .venv/bin/activate
   ```

3. Install dependencies:

   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn jupyter
   ```

4. Start Jupyter:

   ```bash
   jupyter notebook
   ```

5. Open `Customer_Segmentation_KMeans.ipynb`, make sure `Mall_Customers.csv` is available or use the notebook's upload option, then run all cells.

## Results

In the reproduced run using the 200-row dataset, the K-Means model used **5 clusters** and obtained a **silhouette score of approximately 0.555**. The cluster labels are arbitrary identifiers; they do not represent rankings.

The notebook generates:

- Gender distribution plot
- Age, income, and spending-score distributions
- Correlation heatmap
- Customer scatter plot before clustering
- Elbow Method plot
- Silhouette score comparison
- Final customer cluster plot with centroids
- Cluster profile summaries and comparison plots

The notebook exports the results as:

```text
Customer_Segmentation_Results.csv
```

## Understanding the Evaluation

- **Inertia / WCSS:** Measures the sum of squared distances between data points and their assigned centroids. The Elbow Method looks for a practical bend in the curve.
- **Silhouette score:** Measures how well-separated clusters are. A score closer to 1 generally indicates better separation; a score near 0 suggests overlapping groups.
- **K = 5:** Used as a practical starting point for this dataset. The choice should be reviewed alongside the Elbow Method, silhouette scores, plots, and business context.

## Limitations

- The dataset is small and intended for learning.
- The detailed calculation behind the mall's spending score is not provided.
- K-Means is sensitive to feature selection, scaling, initialization, and the chosen number of clusters.
- Suggested marketing interpretations are hypotheses, not guaranteed predictions.
- Real-world use would require more customer, transaction, and campaign-outcome data.

## Future Improvements

- Compare clustering using age and spending score.
- Compare clustering using age, annual income, and spending score.
- Add an interactive dashboard for exploring customer segments.
- Compare K-Means with other clustering algorithms.
- Validate marketing strategies against real campaign results.

## Repository

GitHub: https://github.com/SurendraRana77/Customer-Segmentation.git

## Author

**Surendra Kumar Rana**  
ERP / Student ID: **6605507**  
Rungta College of Engineering & Technology  
Department of Computer Science and Engineering

## Acknowledgements

Thanks to the creators of the Mall Customer Segmentation dataset and the open-source Python libraries used in this project.

## License

The dataset source lists its license as **“Other (specified in description)”**. Check the source dataset's licensing terms before redistributing the data. No separate software license is specified here.
