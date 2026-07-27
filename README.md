
```markdown
# ML PROJECT: Student Academic Performance Prediction

## Project Overview
This project focuses on predicting student academic performance (GPA) using Machine Learning techniques. The dataset was obtained from Kaggle and preprocessed using Pandas. The GPA column was selected as the target variable, while the remaining student-related features were used as input variables. The dataset was split into training and testing sets to evaluate model performance. Two regression algorithms, Linear Regression and Random Forest Regressor, were implemented and compared using Mean Squared Error (MSE) and R² Score metrics. The project also includes data visualization to compare actual and predicted GPA values, providing insights into the accuracy of the models. The objective of this project is to explore how machine learning can be used to analyze student data and predict academic outcomes effectively.

## Data Source
The dataset used in this project is the 'student-performance-data' from Kaggle, downloaded from the user 'muhammadazam121'. The file name is `Student_performance_data.csv`.

## Data Preparation
1.  **Data Separation**: The target variable, 'GPA', was separated from the feature set. `y` represents the 'GPA' and `x` contains all other features.
2.  **Data Splitting**: The dataset was split into training and testing sets using `train_test_split` from `sklearn.model_selection`, with a `test_size` of 0.2 and `random_state` set to 100.

## Model Building
Two regression models were implemented:

### Linear Regression
-   **Training**: A `LinearRegression` model was trained on the `x_train` and `y_train` datasets.
-   **Prediction**: Predictions were made on both the training (`y_lr_train_pred`) and testing (`y_lr_test_pred`) sets.
-   **Evaluation**: The model's performance was evaluated using Mean Squared Error (MSE) and R² Score.

### Random Forest Regressor
-   **Training**: A `RandomForestRegressor` model was trained with `max_depth = 2` and `random_state = 100` on the `x_train` and `y_train` datasets.
-   **Prediction**: Predictions were made on both the training (`y_rf_train_pred`) and testing (`y_rf_test_pred`) sets.
-   **Evaluation**: The model's performance was evaluated using Mean Squared Error (MSE) and R² Score.

## Model Comparison
The performance of both models was compared using their respective training and testing MSE and R² scores, summarized in a Pandas DataFrame:

| Method            | Training MSE | Training R2 | Test MSE   | Test R2    |
|:------------------|:-------------|:------------|:-----------|:-----------|
| Linear regression | 0.035252     | 0.957677    | 0.039097   | 0.954222   |
| Random Forest     | 0.140214     | 0.831662    | 0.167847   | 0.803471   |

## Data Visualization
A scatter plot was generated to visualize the actual vs. predicted GPA values for both training and testing data using `matplotlib.pyplot`, providing a clear comparison of the model's accuracy.
