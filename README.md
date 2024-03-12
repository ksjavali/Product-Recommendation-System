# Product-Recommendation-System

## Objective
The objective of this project is to estimate the purchasing power of a customer given different parameters/characteristics of the customer, thereby helping the company to improve the sales of specific products.

## Data Selection
Sourced from Kaggle: [Link Here](https://www.kaggle.com/datasets/pranavuikey/black-friday-sales-eda)

The dataset used in this analysis contains transaction information in a store on Black Friday, including customers' demographic features and transaction details.

## Data Preprocessing
### Data Assessment
1. Check for necessary missing values using data.isnull().sum()
2. Check for duplicate values using df[col_name].unique() → Result: None
   
### Data Transformation
1. Age Column: Transforming range values into categorical labels
2. Product_Category_2 Column: Filled missing values with 0 indicating no product from category 2 was purchased
3. Product_Category_3 Column: Filled missing values with 0 indicating no product from category 3 was purchased
4. Applied One Hot Encoding for ‘Gender’, ‘Age’, ‘City_Category’, ‘Stay_In_Current_City_Years’ columns in the dataset to train the regression model.
   
## Data Mining Method
The model was trained using the following algorithms:
1. Random Forest: This model can be used for selecting the most informative set of features and building each tree accordingly. It employs an ensemble-based Bagging approach.
2. Lasso & Ridge Linear Regression: Simple & Intuitive model that predicts the target values based on the existing dataset.
3. Gradient Boosting: It also selects the necessary feature set using a weak learner to improve the accuracy of existing weak learners.
4. Elastic Net: It’s a technique that combines both the lasso and ridge regression methods by learning from their shortcomings to improve the regularization of statistical models.
