I made use the  Breast Cancer Wisconsin (Diagnostic) Dataset, the features are computed from a digitized image of a fine needle aspirate (FNA) of a breast mass. They describe characteristics of the cell nuclei
 present in the image in the 3-dimensional space. This database is downloaded from this; Repository: https://archive.ics.uci.edu/ml/datasets/Breast+Cancer+Wisconsin+%28Diagnosti c%29.
The dataset consist of 32 features, some of these features as described by the name file attached to the dataset file are as follow;
1. ID number
2. Diagnosis (M = malignant, B = benign) 3-32)
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

The mean, standard error and "worst" or largest (mean of the three largest values) of these features were computed for each image, resulting in 30 features. For instance, field 3 is Mean Radius, field 13 is 
Radius SE, field 23 is Worst Radius. All feature values were recoded with four significant digits.

The dataset consists of 32 features with all the features being in numerical form except for the diagnosis column which has categorical values for the different samples recorded. I inspected how all the 
features of the dataset by viewing the first 5 and the last 5 rows for each of features.

It is always good to know the depth of the dataset, so I checked for the shape of the dataset to have clue of the number of rows present in the dataset.

I need to confirm that the feature name and total number of feature present is consistent with the documentation about the dataset. I therefore print out a list of all the features and the number of features 
present in the dataset.

The dataset has a depth of 568, hence the need to check for consistency of every column and
ensure all the rows in each column is non-empty. I used the mean method to check for emptiness in every column in the dataset.

The target feature for this problem is the Diagnosis(M) column in the dataset, this is the only column with categorical values and there is need to visualize the distribution of values contained in this column, 
so I visualise different classes in the diagnosis column as shown below;

After visualisation of the classes in the target column, I see that the column consists of 2 classes; class B for benign and class M for malignant and the distribution is relatively good, each of the two classes
 were sufficiently represented.

Since categorical value might not perform well in machine learning models, hence the need to convert the categorical column values to numerical values. I used the LabelEncoder model to fit the categorical values 
and it transform the values to numerical values of 0 for benign and 1 for malignant.

There is need to use the right features when training a model to solve a problem, this is important to ensure the model only learn from features that is correlated with the target feature. Therefore, I carried 
out bivariate analysis to understand the relationships between the features and the target feature, this analysis also ensure that the features are not correlated among themselves and features that are 
correlated were dropped before training the model.
