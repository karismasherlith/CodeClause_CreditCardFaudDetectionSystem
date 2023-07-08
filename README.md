# CodeClause_CreditCardFaudDetectionSystem
Python Code for Credit Card Fraud Detection System
The data set used for the project is available on: https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud

1. IMPORTING MODULES
   - pandas: This library is used for data manipulation and analysis on structured datasets such as CSV files.
   - train_test_split: Used for splitting a large data frame into training and testing subsets.
   - RandomForestClassifier: This library is used for creating algorithms for classification tasks
   - classification_report: Provides a classification report for the prediction model
   - accuracy_score: Calculates the accuracy of the model created
   - confusion_matrix: Provides a matrix comparing the true and predicted values.
        
2. LOADING DATASET
   - The dataset is loaded into the 'credit_data' data frame using the read_csv function.
     
3. STRUCTURE OF DATASET
   - .head() function helps to get the 1st 5 rows of the data frame.
     
4. INFORMATION
   - The .info() function helps you to get the summary of the entire data frame including names of columns, number of null values, memory usage etc.
   - It helps to understand the composition of the data frame.
     
5. SHAPE OF DATASET
   - The .shape() function helps you to get the number of rows and columns in the data frame.
     
6. DROP NULL VALUES
   - The empty valued rows within the data frame are removed from the data frame by using the dropna() function.
     
7. COUNT FRAUD AND NON-FRAUD CASES
   - We then count the number of occurrences of each unique value in the 'Class' column of the data frame.
   - Returns the count for each unique value with the help of the value_counts() function.
     
8. PREPARING DATA FOR TRAINING
   - We first create a new data frame named 'X' by dropping the 'Class' column.
   - We then assign the 'Class' columns to another data frame named 'Y'
   - Then we split the dataset into training and testing subsets with 20% of the dataset for training and 80% for testing.
   - We also set a random state of 42 so as to reproduce the same split in every program run.
     
9. TRAINING RANDOM FOREST CLASSIFIER
    - The classifier is created with an estimator which specifies the number of decision trees to be used in the random forest ensemble.
    - The random state specifies the state for reproducibility.
      The classifier is then fit to the training data by training the model by finding patterns and relationships.
      The model is used to learn predictions from the training data.
      
10. MAKING PREDICTIONS
    - We then predict the output values (Y) for the input value (X).
      
11. ACCURACY. CONFUSION MATRIX AND CLASSIFICATION REPORT
    - An accuracy score is calculated by comparing predicted values to the true values and prints the percentage.
    - The confusion matrix provides a summary of the model's performance by showing the number of true positives, true negatives, false positives, and false negatives.
    - A classification report is produced which includes the metrics such as precision, recall, F1-Score, and support for each class.
      
12. MANUAL TESTING
     - We create a function which takes time and amount as the input.
     - The dataset is loaded first into a data frame named 'data'.
     - We then calculate the closest transaction in the dataset which matches the values entered by the user.
     -  It computes the absolute differences between each transaction's amount and time with the entered values, sums them up, and finds the index of the row with the minimum sum.
     -  Then we retrieve the row corresponding to this transaction and check if the 'Class' columns value is 1 or not.
     -  If it matches 1, the function prints 'Fraud Case' else otherwise.
     -  The function also asks the user if they want to continue checking, if user input is 'y' the function continues.
