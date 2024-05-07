# Music Genre Classification Using Decision Trees and Logistic Regression

This project aims to classify songs into two genres: Hip-Hop and Rock, using machine learning models. We will explore data cleaning, exploratory data visualization, feature reduction, and ultimately, model building using decision trees and logistic regression.

## 1. Preparing our dataset

We will start by loading the track metadata and the track metrics compiled by The Echo Nest. These datasets contain musical features such as `danceability`, `acousticness`, and other attributes scaled from -1 to 1. Our main goal in this section is to merge these datasets to combine the features (`X`) and labels (`y`) for our classification later.

## 2. Pairwise relationships between continuous variables

Before proceeding with model building, it's crucial to identify if there are any strongly correlated features in our dataset. Strong correlations between features can lead to redundancy and may affect the model's performance. We will use the `pandas` package to compute and visualize these correlations.

## 3. Splitting our data

We will split our data into features and labels. Then, the data will be divided into a training set and a testing set. This separation is essential for training our models and subsequently evaluating their performance on unseen data.

## 4. Normalizing the feature data

Since the range of values in features can vary widely, we need to standardize the features using `StandardScaler` from `sklearn`. This process adjusts the features so that they have a mean of 0 and a standard deviation of 1.

## 5. Principal Component Analysis (PCA) on our scaled data

We will use PCA to reduce the dimensionality of our data. This step helps in decreasing the computational cost and improving the performance of our machine learning models. We will determine the number of components to retain by using scree-plots and cumulative explained variance plots.

## 6. Training the Models

After preprocessing and transforming the data using PCA, we will train two different models:
- A Decision Tree Classifier
- A Logistic Regression

We will use these models to classify the songs into either Hip-Hop or Rock.

## 7. Model Evaluation

We will evaluate our models based on precision, recall, and f1-score. These metrics will help us understand the effectiveness of our models in classifying the songs correctly.

## 8. Balancing the Dataset

To improve our model's ability to generalize and reduce any potential bias due to imbalanced classes, we will balance our dataset. This means adjusting the number of samples from each class to be equal.

## 9. Cross-validation

To ensure the robustness of our models, we will employ K-fold cross-validation. This method splits the data into K smaller sets and evaluates the model K times, each time with a different set as the test set and the remaining as the training set.

## Conclusion

The project concludes with insights gained from the model performances and their implications in the field of music genre classification.
