# insurance-policy-clustering-svd
Customer segmentation and clustering analysis using the Insurance Policy dataset to group profiles by policy type.

# Insurance Policy Customer Segmentation & Clustering Analysis

## 1. Business Problem
### 1.1. What is the business objective?
The primary objective is to analyze customer demographic and policyholder details from the Insurance Policy dataset to group individuals into distinct clusters based on shared characteristics. By identifying natural customer segments, the insurance company can design personalized insurance plans, offer appropriate coverage tiers, and optimize cross-selling and underwriting strategies.

### 1.2. Are there any constraints?
* **Mixed Feature Types:** Insurance datasets frequently combine numerical features (e.g., age, income, premium amounts) with categorical policy attributes, requiring careful pre-processing, encoding (one-hot or label encoding), and feature scaling.
* **Data Skewness:** Financial and demographic attributes often contain skewed distributions or outliers that need normalization so they do not distort distance-based clustering algorithms.
* **Actionable Interpretability:** The resulting segments must translate into clear risk profiles or buyer personas that underwriting and marketing teams can practically utilize.

---

## 2. Data Dictionary
*(Adjust or verify based on your specific columns in `Insurance Dataset.csv`)*

| Feature Name | Data Type | Description |
| :--- | :--- | :--- |
| **Customer ID** | Integer / String | Unique identifier for each policyholder. |
| **Age** | Numeric | Age of the insured customer. |
| **Income** | Numeric | Annual income of the policyholder. |
| **Premium** | Numeric | Amount paid for the insurance policy. |
| **Policy Type** | Categorical | Classification or category of the insurance policy held. |

---

## 3. Exploratory Data Analysis (EDA)
* **3.1. Summary:** Comprehensive statistical overview covering central tendencies, distributions, and missing-value checks across policy and customer features.
* **3.2. Univariate Analysis:** Exploring individual distributions, such as customer age brackets, income levels, and premium cost spreads.
* **3.3. Bivariate Analysis:** Examining correlations between income, premium costs, and policy choices to uncover behavioral patterns.

---

## 4. Data Pre-processing
* **4.1. Data Cleaning & Feature Engineering:** Managed missing values, encoded categorical policy variables using dummies/label encoding, and dropped irrelevant identifier columns.
* **Normalization:** Applied standard scaling techniques to ensure numerical variables are balanced and contribute equally to distance metrics.

---

## 5. Model Building
* **5.1. Scaled Data Modeling:** Implemented unsupervised clustering models on the pre-processed and normalized dataset.
* **5.2. K-Means Clustering & Scree Plot:** Applied the Elbow Method (Scree Plot of Within-Cluster Sum of Squares) to determine the optimum number of clusters ($k$).
* **5.3. Cluster Validation & Insights:** Validated cluster configurations across various values of $k$, assigned descriptive business labels, and derived key comparative insights.

---

## 6. Business Benefits & Impact
Providing this clustering solution gives the organization strategic advantages:
* **Personalized Offerings:** Enables the creation of customized insurance packages tailored to specific customer risk and income tiers.
* **Optimized Pricing & Underwriting:** Helps risk assessment teams understand cluster-based behaviors for more accurate premium pricing.
* **Targeted Retention:** Enhances customer relationship management by identifying high-value policyholder groups prone to specific coverage needs.
