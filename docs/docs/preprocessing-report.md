# Preprocessing Report

## 1. Dataset Files
Raw Data: Titanic-Dataset.csv
Cleaned Data: clean_titanic_data.csv
Development Notebook: feature_engineering.ipynb

## 2. Pipline Execution steps
Step 1 : Categorical Variable Encoding
- Nominal Featuers: Transformed using One-Hot Encoding to create seperate binary columns. This prevents model from assuming an artificial mathematical hierarchy between categories
Step 2 : Feature Scaling
- Standarization: Numerical Variables were normalized using Scikit-learn StandardScaler to scale them to a mean of 0 and a standard deviation of 1
Step 3 : Feature Engineering & Selection
- Feature Selection: Removed high-cardinalty metadata identifiers(PassengerId, Name, Ticket) that do not posses predective power
Step 4 : Tran-Test Split & Data Leakage Prevention
- The preprocessed dataset was partitioned into an 80% training set and a 20% testing set prior to scaling
- Anti-Leakage control: The scaling parameters were calculated strictly on the training set
step 5 : Export Final Dataset
- The Final cleaned, engineered, and scaled training and testing features were exported as CSV files

## 3. Impact
Preprocessing improves machine learning model performance by reducing missing data issues and ensuring consistent feature scale 

