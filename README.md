# Breast Cancer Wisconsin (Diagnostic) Dataset Analysis

## Dataset Overview

This project utilizes the Breast Cancer Wisconsin (Diagnostic) Dataset. The features are computed from digitized images of fine needle aspirates (FNA) of breast masses, describing characteristics of cell nuclei present in the images.

**Dataset Source:** [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/Breast+Cancer+Wisconsin+%28Diagnostic%29)

## Features

The dataset consists of 32 features, including:

1. ID number
2. Diagnosis (M = malignant, B = benign)
3. Radius (mean of distances from center to points on the perimeter)
4. Texture (standard deviation of gray-scale values)
5. Perimeter
6. Area
7. Smoothness (local variation in radius lengths)
8. Compactness (perimeter^2 / area - 1.0)
9. Concavity (severity of concave portions of the contour)
10. Concave points (number of concave portions of the contour)
11. Symmetry
12. Fractal dimension ("coastline approximation" - 1)

For each feature, the mean, standard error, and "worst" (mean of the three largest values) were computed, resulting in 30 features. All feature values were recorded with four significant digits.

## Data Exploration

1. Inspected the first 5 and last 5 rows of each feature.
2. Checked the dataset shape to determine the number of rows.
3. Verified feature names and total number of features against the documentation.
4. Checked for consistency and non-empty values in all columns using the mean method.

## Target Feature

The target feature is the "Diagnosis" column, containing categorical values (M for malignant, B for benign).

## Data Visualization

Visualized the distribution of classes in the target column, revealing two classes:
- B: Benign
- M: Malignant

The distribution between classes was found to be relatively balanced.

## Data Preprocessing

1. Converted categorical values in the "Diagnosis" column to numerical values using LabelEncoder:
   - 0: Benign
   - 1: Malignant

2. Performed bivariate analysis to understand relationships between features and the target feature.
3. Identified and removed correlated features to improve model performance.

## Next Steps

- Feature selection based on correlation analysis
- Model training and evaluation
- Performance optimization
