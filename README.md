# Breast Cancer Wisconsin Dataset Analysis

## Project Overview

This project analyzes the Breast Cancer Wisconsin (Diagnostic) Dataset to classify breast masses as benign or malignant. It includes data preprocessing, exploratory data analysis, and implementation of both Artificial Neural Network (ANN) and Logistic Regression models.

## Dataset

The dataset used is the Breast Cancer Wisconsin (Diagnostic) Dataset, available from the UCI Machine Learning Repository:
[https://archive.ics.uci.edu/ml/datasets/Breast+Cancer+Wisconsin+%28Diagnostic%29](https://archive.ics.uci.edu/ml/datasets/Breast+Cancer+Wisconsin+%28Diagnostic%29)

## Project Structure

The project is structured as a Jupyter notebook (`AYUBA_ABIOLA_30079606_ML.ipynb`) containing all the analysis steps.

## Installation

1. Clone this repository
2. Install required libraries:
   ```
   pip install pandas numpy matplotlib sklearn plotly seaborn tensorflow keras zipfile
   ```

## Data Preprocessing

1. Loaded data from a zip file
2. Checked for missing values
3. Encoded the target variable ('M' column) using LabelEncoder
4. Split the data into training and test sets
5. Performed feature scaling using StandardScaler

## Exploratory Data Analysis

1. Visualized the distribution of the target variable
2. Created correlation heatmaps to check for multi-collinearity
3. Identified and removed highly correlated features

## Models

### Artificial Neural Network (ANN)

- Architecture:
  - Input layer: 31 neurons
  - Two hidden layers with 16 neurons each, ReLU activation
  - Output layer: 1 neuron, sigmoid activation
- Dropout layers (rate=0.01) to prevent overfitting
- Compiled with 'adam' optimizer and 'binary_crossentropy' loss
- Trained for 30 epochs with a batch size of 32

### Logistic Regression

- Implemented from scratch using gradient descent
- Used sigmoid activation function
- Trained for 40,000 iterations with a learning rate of 0.001

## Dimensionality Reduction

- Performed Principal Component Analysis (PCA)
- Used Recursive Feature Elimination with Cross-Validation (RFECV) to identify optimal number of features

## Results

### ANN Results

- Plotted training and validation loss
- Plotted training and validation accuracy
- Evaluated using accuracy, precision, recall, and F1 score
- Generated ROC curve and confusion matrix
- - Achieved an accuracy of [97.37] %

### Logistic Regression Results

- Plotted cost change over iterations
- Generated ROC curve
- Produced classification report and confusion matrix
- Achieved an accuracy of [97.66] %

## Visualizations

- Correlation heatmaps
- Feature importance plots
- ROC curves for both models
- Confusion matrices

## Contact

[Abiola Ayuba] - [abiolaayubam@gmail.com]

Project Link: [https://github.com/your-username/breast-cancer-analysis](https://github.com/your-username/breast-cancer-analysis)
