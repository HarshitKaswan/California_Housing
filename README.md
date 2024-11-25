# California Housing Price Prediction

This repository contains an end-to-end machine learning project that predicts California housing prices based on various features like income, population, and geographical location. The project uses the **California Housing Dataset** and implements data exploration, feature engineering, and hyperparameter-tuned **Random Forest Regression** to achieve an R² score of 0.8048.

---

## Project Workflow

### 1. Data Loading
- Loaded the **California Housing Dataset** using `fetch_california_housing` from `sklearn.datasets`.
- Converted the data into a Pandas DataFrame for easier manipulation.

### 2. Exploratory Data Analysis (EDA)
- Visualized the distribution of key features using histograms.
- Explored geographical patterns with scatter plots of latitude and longitude.
- Examined correlations between features and the target variable (`MedHouseVal`) using a heatmap.

### 3. Feature Engineering
- Derived new features for better predictive performance:
  - `RoomsPerBedroom` = `AveRooms` / `AveBedrms`
  - `PopulationPerRoom` = `Population` / `AveRooms`
- Checked the dataset for missing values and data types.

### 4. Model Selection
- Split the dataset into training and test sets using `train_test_split`.
- Used **Random Forest Regressor** for its robustness and ability to handle nonlinear relationships.

### 5. Hyperparameter Tuning
- Performed a grid search using **GridSearchCV** to find the best parameters for:
  - Number of estimators (`n_estimators`)
  - Maximum tree depth (`max_depth`)
  - Minimum samples required to split (`min_samples_split`)
- Achieved an optimized R² score of **0.8048**.

### 6. Model Evaluation
- Evaluated the model on the test set using R² score.
- Analyzed feature importance to understand the most influential predictors.

---

## Results

- **Final R² Score on Test Set:** `0.8048`
- **Key Insights:**
  - Higher median income (`MedInc`) strongly correlates with higher house values.
  - Population density features like `PopulationPerRoom` contributed significantly to predictions.

---
