# Housing Price Prediction Using Regression Models

This project explores regression techniques to predict the median house value for California districts based on 1990 census data. The dataset contains information on various housing attributes such as median income, house age, population, and location. The focus is on understanding the relationships between features and target values, evaluating model performance, and enhancing predictions using advanced techniques.

---

## Objectives

1. Understand the dataset and preprocess the data for analysis.
2. Explore and visualize input features and their relationships with the target variable.
3. Implement and evaluate regression models, including:
   - Ordinary Least Squares (OLS) Regression
   - Lasso Regression
   - Ridge Regression
4. Identify the best-performing model based on metrics like RMSE and R-squared.
5. Use feature engineering and transformations to improve model performance.

---

## Dataset Overview

The dataset provides information on residences in California districts based on the 1990 census. Key attributes include:
- **Input Features**: `median_income`, `households`, `housing_median_age`, `total_rooms`, `latitude`, `longitude`, `population`, `total_bedrooms`
- **Target Variable**: `median_house_value` (median house value in USD)

---

## Steps and Key Results

### 1. Data Exploration
- **Input Features**:
  - Summary statistics, data types, and distributions were examined.
  - Correlation analysis was performed to identify relationships between features.
  - Scatter plots and histograms visualized feature distributions and trends.
- **Target Variable**:
  - Distribution and summary statistics were analyzed.
  - Scatter plots revealed relationships between inputs and the target variable.

### 2. Regression Models
#### a. Ordinary Least Squares (OLS) Regression
- **Performance**:
  - Training RMSE: ~68857.71
  - Testing RMSE: ~70857.71
  - Training R-squared: 0.67
  - Testing R-squared: 0.61
- **Visuals**:
  - Residual plots showed the model's performance and error distribution.

#### b. Lasso Regression
- Lasso regularization applied for feature selection and sparsity.
- **Performance**:
  - Slightly improved predictions for certain test sets.
  - Regularization parameter (`alpha`) adjusted for optimal performance.

#### c. Ridge Regression
- Ridge regularization addressed multicollinearity issues.
- **Performance**:
  - Selected as the **best-performing model** based on lowest RMSE and balanced R-squared values.

---

## Feature Engineering
1. **Feature Scaling**:
   - Scaled `median_income` using `StandardScaler`.
2. **Interaction Terms**:
   - Created interaction terms between `housing_median_age` and `population`.
3. **Polynomial Features**:
   - Generated polynomial terms for `housing_median_age` to capture non-linear relationships.

---

## Model Evaluation

1. **Metrics**:
   - RMSE (Root Mean Squared Error)
   - R-squared (Coefficient of Determination)
2. **Residual Analysis**:
   - Residual plots indicated model accuracy and areas for improvement.

### Best Performing Model
- **Ridge Regression**:
  - Addressed overfitting and multicollinearity effectively.
  - Showed improved generalization on testing data.

---

## Conclusion

- The Ordinary Least Squares model provided moderate performance but struggled with multicollinearity.
- Ridge Regression outperformed OLS and Lasso by balancing bias and variance.
- Incorporating additional features like geographic, economic, and market data could further improve prediction accuracy.

---

## Tools and Libraries Used
- **Python**:
  - `pandas`, `numpy`: Data manipulation and exploration.
  - `matplotlib`, `seaborn`: Data visualization.
  - `scikit-learn`: Regression models, metrics, preprocessing.
- **Key Methods**:
  - `LinearRegression`, `Lasso`, `Ridge`
  - Train-test split, feature scaling, residual analysis.

---

