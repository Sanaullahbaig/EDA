# 📊 Marketing Campaign Data Analysis (EDA)

This project performs a detailed Exploratory Data Analysis (EDA) on a marketing campaign dataset. The primary goal is to clean the data, analyze customer demographics and purchasing behavior, and identify relationships between key variables in preparation for potential segmentation or predictive modeling.

## 🛠️ Tools and Libraries Used

* **Python:** For data manipulation and analysis.
* **Pandas & NumPy:** For data handling and numerical operations.
* **Matplotlib & Seaborn:** For comprehensive data visualization.

## 🚀 Key Steps and Analysis

### 1. Data Loading and Initial Exploration

The dataset was loaded and examined using functions like `head()`, `tail()`, `shape`, `dtypes`, and `info()`.
* **Dataset Size:** 2240 rows and 30 columns.
* **Statistical Summary:** `describe()` provided initial insights into the central tendency, spread, and shape of the distributions for numerical columns.

### 2. Data Cleaning

| Issue | Column(s) | Action Taken (as per code) |
| :--- | :--- | :--- |
| **Missing Values** | `Income` (24 nulls) | Identified using `isnull().sum()`. The provided code demonstrated both `dropna()` and `fillna()` methods for handling them. |
| **Duplicates** | Entire dataset | Checked using `duplicated().sum()` and confirmed no duplicates were present. |
| **Outliers** | `Income`, `MntWines` | Visualized using `sns.boxplot()` to identify extreme values (e.g., in Income and product spending). |

### 3. Univariate Analysis (Single Variable)

* **Numerical:** Distributions of `Year_Birth` and `MntWines` were visualized using **Histograms** and **Boxplots**.
* **Categorical:** Frequencies of `Marital_Status` (using **Countplot**) and `Kidhome` (using **Pie Chart**) were displayed.

### 4. Bivariate Analysis (Two Variables)

| Relationship Type | Example Variables | Visualization Technique |
| :--- | :--- | :--- |
| **Num. vs. Num.** | `Year_Birth` vs. `Income` | **Scatterplot** and **Regplot** (to show trend). |
| **Cat. vs. Num.** | `Marital_Status` vs. `Income` | **Boxplot, Violin Plot, and Bar Plot** (to compare income distribution across groups). |
| **Cat. vs. Cat.** | `Education` vs. `Marital_Status` | **Heatmap** and **Crosstab Bar Plot** (to show co-occurrence). |

### 5. Multivariate Analysis & Correlation

* **Correlation Matrix:** A **Heatmap** was generated using `specific_columns.corr()` to quantify and visualize the linear relationship between key numerical variables (`Year_Birth`, `Income`, `Kidhome`, `Teenhome`).
* **Pair Plots:** Used `sns.pairplot()` for a high-level visualization of all pairwise relationships among the selected numerical columns.

### 6. Distribution and Feature Insights

* **Distribution Analysis:** `sns.distplot()` and `sns.kdeplot()` were used to understand the spread and shape of the `Income` variable.
* **Shape Metrics:** **Skewness** and **Kurtosis** were calculated to quantitatively describe the symmetry and tail-heaviness of the numerical distributions.
* **Grouped Insights:** The `groupby()` function was utilized to find the mean `Income` for different `Marital_Status` groups, providing summarized business insights.

---

