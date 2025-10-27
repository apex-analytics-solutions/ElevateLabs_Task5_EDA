# 📊 Task 5: Exploratory Data Analysis (EDA)

## Data Analyst Internship - Elevate Labs

### 🎯 Objective
The primary goal of this task was to perform a comprehensive Exploratory Data Analysis (EDA) on a transactions dataset to extract meaningful insights, identify patterns, trends, and anomalies, and prepare the data for subsequent machine learning modeling.

### 📁 Dataset Used
**Credit Card Fraud Detection Data**

* [cite_start]**Total Transactions:** 3544[cite: 133].
* **Key Target Variable:** `is_fraud` (0 for non-fraud, 1 for fraud).

### 🛠️ Tools and Libraries
* **Language:** Python
* **Environment:** Google Colab (Jupyter Notebook)
* **Libraries:** Pandas, NumPy, Matplotlib, Seaborn

---

### 📝 Key Steps Performed

1.  [cite_start]**Data Loading & Inspection:** The dataset contained **3544 rows** and **27 columns**[cite: 133].
2.  **Missing Value Identification:** Missing values were found in multiple columns:
    * [cite_start]`merch_zipcode` had **572 missing values** (3544 total - 2972 non-null)[cite: 126, 133].
    * [cite_start]Columns like `city`, `state`, `zip`, `lat`, `long`, `city_pop`, `job`, `dob`, `unix_time`, and `Age` each had **1 missing value** [cite: 156-175, 185].
3.  [cite_start]**Data Cleaning:** Missing values were addressed using imputation (Median/Mode) [cite: 188-193]. [cite_start]The single missing value in `is_fraud` was also filled with 0[cite: 202].
4.  [cite_start]**Analysis & Visualization:** Standard EDA plots (Histograms, Boxplots, Count Plots, Heatmap) were generated [cite: 318-427].

---

### 💡 Summary of Key Findings (Results)

* [cite_start]**Class Imbalance:** The data exhibits **significant class imbalance** [cite: 327-330].
    * [cite_start]Non-Fraud (0): **2547 transactions**[cite: 298].
    * [cite_start]Fraud (1): **997 transactions**[cite: 300].
    * [cite_start]The fraud class constitutes approximately **28.13%** of the total transactions[cite: 281].
* [cite_start]**Transaction Amount:** The `amt` distribution is **heavily right-skewed** [cite: 319-323]. [cite_start]The boxplot visual suggests that the **median transaction amount for fraud cases is slightly higher** than for non-fraud cases[cite: 354].
* [cite_start]**High-Risk Categories:** Based on the generated visual analysis, the categories with the highest absolute fraud frequency are **`shopping_net`** and **`shopping_pos`** [cite: 401-402, 420].
* [cite_start]**Correlation:** The **Correlation Heatmap** shows **no significant strong linear correlations** (values are near 0, e.g., `is_fraud` to `Age` is -0.02 [cite: 497][cite_start]) between the primary numeric features [cite: 434-510].

---

### 📦 Files in this Repository

* `credit_card_transactions.ipynb`: The complete Python code and analysis notebook.
* `credit_card_transactions.ipynb - Colab.pdf`: The final PDF report containing all visuals and observations.
* `credit_card_transactions.csv`: The raw dataset used for the analysis.
