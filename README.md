# Sales Prediction

This Python code is a machine learning script that uses the Support Vector Machine (SVM) algorithm to classify instances of Parkinson's disease based on a dataset. Here is a step-by-step description of the code:

1. **Importing Libraries:**
   - The code starts by importing necessary libraries, including NumPy, Pandas, and scikit-learn modules for data manipulation, analysis, and machine learning.

2. **Loading the Dataset:**
   - The Parkinson's disease dataset is loaded from a CSV file named 'parkinsons.csv' using Pandas. The first few rows of the dataset are displayed using `head()`.

3. **Dataset Exploration:**
   - The shape and information of the dataset are printed using `shape` and `info()` to understand its dimensions and data types. The number of missing values in each column is also printed using `isnull().sum()`.

4. **Data Scaling:**
   - The features are separated into X (independent variables) and the target variable 'status' is assigned to Y. Standard scaling is applied to normalize the feature values using `StandardScaler()` from scikit-learn.

5. **Train-Test Split:**
   - The dataset is split into training and testing sets using `train_test_split()` from scikit-learn. The split is done with 80% for training and 20% for testing. Stratification is applied based on the target variable 'status' to maintain the distribution of classes in both sets.

6. **Model Training:**
   - An SVM (Support Vector Machine) model is created using `svm.SVC()` from scikit-learn, and it is trained on the scaled training data with `fit()`.

7. **Training Accuracy:**
   - The accuracy of the model on the training set is calculated using `accuracy_score()` from scikit-learn. This accuracy is printed.

8. **Testing Accuracy:**
   - The model is used to predict the target variable on the test set, and the accuracy of the predictions is calculated and printed.

9. **New Input Prediction:**
   - A subset of the test set (rows 15 to 30) is selected as new input (`new_input`). The model is then used to predict the target variable for this new input, and the predictions are printed along with the actual values from the dataset.

Overall, this code demonstrates the process of loading a dataset, preprocessing it, splitting it into training and testing sets, training an SVM model, and evaluating its accuracy on both the training and testing sets. Additionally, it makes predictions on a subset of the test set and compares the predictions with the actual values.
