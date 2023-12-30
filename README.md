# Sales Prediction

This Python code is related to the analysis and prediction of sales data for a Big Mart. Here's a breakdown of the code:

1. **Data Loading and Exploration:**
   - The code begins by importing necessary libraries such as NumPy, Pandas, Matplotlib, Seaborn, and Scikit-Learn, along with the XGBoost library for regression.
   - It reads a CSV file ('Sales_Train.csv') into a Pandas DataFrame named `big_mart_data`.
   - The shape of the DataFrame is printed using `big_mart_data.shape`.
   - The number of missing values in each column is displayed using `big_mart_data.isnull().sum()`.

2. **Data Cleaning:**
   - The mean of the 'Item_Weight' column is calculated and used to fill in missing values in that column.
   - The mode of 'Outlet_Size' is determined based on the 'Outlet_Type', and missing values in 'Outlet_Size' are filled using this information.

3. **Data Visualization:**
   - Several Seaborn and Matplotlib visualizations are created to explore the distributions and counts of various features in the dataset. These include visualizations for item weight, item visibility, item MRP (Maximum Retail Price), outlet establishment year, item outlet sales, item fat content, item type, outlet size, and more.

4. **Data Preprocessing:**
   - The code performs label encoding on categorical columns using `LabelEncoder` from Scikit-Learn. Categorical variables such as 'Item_Fat_Content', 'Item_Type', 'Outlet_Identifier', 'Outlet_Size', 'Outlet_Location_Type', and 'Outlet_Type' are transformed into numerical values.

5. **Feature Matrix and Target Vector Preparation:**
   - The dataset is split into the feature matrix `X` (independent variables) and the target vector `Y` (dependent variable), where 'Item_Outlet_Sales' is the target variable.

6. **Train-Test Split:**
   - The data is split into training and testing sets using `train_test_split` from Scikit-Learn.

7. **XGBoost Regression Model:**
   - An XGBoost Regressor is instantiated and trained on the training data.

8. **Model Evaluation:**
   - The model is evaluated on the training set using the R-squared metric (`metrics.r2_score`).
   - The trained model is then used to make predictions on the test set, and the R-squared value for the test set is calculated.

9. **Prediction on Input Data:**
   - Finally, the code selects a subset of data from the test set (`X_test[115:120]`) and predicts the corresponding 'Item_Outlet_Sales' using the trained XGBoost Regressor. The predicted values are printed.

Overall, this code involves data cleaning, exploratory data analysis (EDA), preprocessing, and training an XGBoost regression model to predict sales for items in a Big Mart.
