# NBA Player Performance Prediction

## Overview
This project predicts NBA player performance (Points Per Game, or **PTS**) based on historical statistics such as:
- Minutes Per Game (**MP**)
- Field Goal Percentage (**FG%**)
- Three-Point Percentage (**3P%**)
- Free Throw Percentage (**FT%**)
- **Efficiency Rating (EFF)**: A new feature added to evaluate overall player efficiency.

The goal is to use these features to build a predictive model that can help us understand how various factors influence a player's scoring ability.

## Dataset
The dataset used in this project contains NBA player statistics for multiple seasons. The main columns of interest are:
- **MP** (Minutes Per Game)
- **FG%** (Field Goal Percentage)
- **3P%** (Three-Point Percentage)
- **FT%** (Free Throw Percentage)
- **PTS** (Points Per Game — target variable)
- **EFF** (Efficiency Rating — new feature added to the dataset)

You can download the dataset [here](https://www.kaggle.com/datasets/eduardopalmieri/nba-player-stats-season-2425) or use a similar dataset of NBA player stats.

## Libraries Used
The following libraries are used in this project:
- **pandas**: For data manipulation and analysis.
- **numpy**: For numerical operations.
- **matplotlib**: For data visualization.
- **seaborn**: For enhanced data visualization.
- **scikit-learn**: For machine learning algorithms and metrics.

## Steps Involved
The project can be divided into the following steps:

### 1. Data Collection
- The dataset is loaded into a pandas DataFrame from a CSV file (`nbastats.csv`).

### 2. Data Preprocessing
- The dataset is cleaned by handling missing data and removing any irrelevant columns.
- Relevant features are selected: `MP`, `FG%`, `3P%`, `FT%`, and the target variable `PTS`.
- **New Feature**: The **Efficiency Rating (EFF)** is calculated for each player to quantify their overall performance efficiency. This is added to the dataset for model prediction.

### 3. Data Splitting
- The data is split into two sets: one for training the model and another for testing the model's performance.

### 4. Model Training
- A **Linear Regression** model is used to predict the target variable `PTS`.
- The model is trained on the training data set, using features such as `MP`, `FG%`, `3P%`, `FT%`, and `EFF`.

### 5. Model Evaluation
- The model's performance is evaluated using **Mean Absolute Error (MAE)** and **Root Mean Squared Error (RMSE)**.
- These metrics are used to measure the accuracy of the predictions.

### 6. Model Visualization
- A scatter plot is created to compare the actual vs. predicted values of `PTS`.

### Results 
- MAE = 3.80
- RMSE = 5.08
- **Efficiency Rating Impact**: The addition of the **Efficiency Rating (EFF)** improved the model's performance by offering a better representation of the player's overall contribution.

### Future Work
- Use grid search or random search to optimize the model.
- Cross-validate the model for better performance.
- Investigate the effect of additional features like player position and team statistics on performance prediction.

## How to Run this Project

**Clone the repository**:
   ```bash
   git clone https://github.com/akilajuan/nba-player-performance.git
