# Student GPA Prediction — ML Project

## Overview

This project predicts student academic performance (GPA) using machine learning. It uses a student performance dataset from Kaggle, with GPA as the target variable and the remaining student attributes as input features. Two regression models — **Linear Regression** and **Random Forest Regressor** — are trained, evaluated, and compared to see how well each can predict GPA from the available features.

## Dataset

- **Source:** [Student Performance Dataset on Kaggle](https://www.kaggle.com/datasets/muhammadazam121/student-performance-data)
- **File:** `Student_performance_data.csv`
- **Target variable:** `GPA`
- **Features:** all remaining columns in the dataset

## Workflow

1. **Load Data**
   - Downloads the dataset from Kaggle via the Kaggle API (requires a `kaggle.json` API key).
   - Loads the CSV into a Pandas DataFrame.

2. **Data Preparation**
   - Separates the target (`GPA`) from the input features.
   - Splits the data into training and test sets (80/20 split, `random_state=100`).

3. **Model Building**
   - **Linear Regression** — trained on the training set, evaluated on train/test.
   - **Random Forest Regressor** — trained with `max_depth=2`, `random_state=100`, evaluated on train/test.

4. **Model Evaluation**
   - Metrics used: **Mean Squared Error (MSE)** and **R² Score**.
   - Results for both models are compiled into a comparison table.

5. **Data Visualization**
   - Scatter plot of actual vs. predicted GPA (training and test data) to visually assess model accuracy.

## Requirements

- Python 3
- pandas
- scikit-learn
- matplotlib
- kaggle (for dataset download)

## Setup & Usage

1. Get a Kaggle API token (`kaggle.json`) from your Kaggle account settings.
2. Run the notebook cells in order:
   - Upload `kaggle.json` when prompted (or place it in `~/.kaggle/`).
   - The notebook downloads and unzips the dataset automatically.
3. Run through data preparation, model training, evaluation, and visualization cells sequentially.

## Results

The notebook outputs a comparison table with Training/Test MSE and R² scores for both Linear Regression and Random Forest, along with a scatter plot comparing actual vs. predicted GPA values.
