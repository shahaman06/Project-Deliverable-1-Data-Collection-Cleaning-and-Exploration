# Project-Deliverable-1-Data-Collection-Cleaning-and-Exploration

## Project Overview
This project is part of Advanced Data Mining for Data-Driven Insights and Predictive Modeling.  
The goal of this deliverable is to perform data collection, cleaning, and exploratory data analysis (EDA) on a real-world dataset to prepare it for predictive modeling.

---

## Dataset Summary
- **Dataset Name:** Wine Quality (Red Wine)
- **Source:** [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/Wine+Quality)
- **Instances:** 1,598
- **Attributes:** 11 physicochemical features + quality score (total 12)
- **Description:** The dataset includes numeric features such as acidity, sugar, pH, sulfur dioxide levels, density, alcohol, and wine quality (score from 0–10).

**Justification for Selection:**  
- Dataset has more than 500 records and 12 attributes, fulfilling the project requirements.  
- Features are continuous, allowing for robust EDA and feature analysis.  
- Wine quality is a meaningful target variable for regression or classification models.  
- Widely used in academic research and publicly available.

---

## Data Cleaning Steps
1. **Missing Values:**  
   - Checked for missing data; none were found.  
   - No imputation was necessary.  
2. **Duplicates:**  
   - Checked for duplicate rows; removed duplicates to ensure unique observations.  
3. **Outliers:**  
   - Outliers were detected using the Z-score method (threshold = 3).  
   - Rows with extreme values in any numeric feature were removed.  
   - This prevents extreme values from distorting statistical analyses and models.

**Explanation:**  
These steps ensure the dataset is clean, consistent, and reliable for EDA and subsequent modeling.

---

## Exploratory Data Analysis (EDA) Highlights

### Distributions
- `alcohol` and `citric acid` show roughly normal distributions.  
- `residual sugar` is right-skewed.  
- Understanding distributions helps identify features that may require scaling or transformation for modeling.

### Boxplots by Quality
- Higher `alcohol` and `citric acid` levels are associated with higher wine quality.  
- `volatile acidity` tends to decrease as quality increases.  
- Boxplots helped detect outliers and visualize feature trends across quality scores.

### Correlation Insights
- Positive correlation: `alcohol` ↔ `quality`  
- Negative correlation: `volatile acidity` ↔ `quality`  
- Strong correlation between `free sulfur dioxide` and `total sulfur dioxide`  
- Correlation analysis informs feature selection for predictive modeling.

### Pairwise Relationships
- Scatterplots reveal interactions between key features like `alcohol`, `citric acid`, and `quality`.  
- Patterns indicate potential predictive power for quality modeling.

---

## Challenges Encountered
- Skewed distributions in some features may affect modeling performance.  
- Quality scores overlap across several feature values, suggesting that simple linear models may not fully capture relationships.  
- Outlier handling required careful consideration to remove extreme cases without discarding valuable data.

---

## Next Steps
1. Feature scaling or normalization for modeling.  
2. Explore feature engineering, including interaction terms.  
3. Decide whether to model wine quality as regression (continuous score) or classification (grouped quality categories).  
4. Prepare data splits and cross-validation strategy for predictive modeling in subsequent project deliverables.
