# Logistic regression based online loan credit evaluation
### Huang Jing  1801213537
# 1. Project Description
This project is my summary of PHBS course "Machine Learning for Finance".<br>
* Use online loan application data to train the logistic regression model.<br>
* Predict whether the applicants will get the loan.<br>

# 2. Dataset Description
## 2.1 Dataset Source
Download from LendingClub <br>
Webpage:https://www.lendingclub.com/info/download-data.action
## 2.2 Dataset Information
Loan data for Q2 of 2018<br>
Format:csv<br>
Data size:42.7 MB<br>
LendingClub provide a formal data dictionary, Please check it in folder "data".
## 2.3 Data visualization
5 rows × 145 columns
# 3. Data preprocessing
## 3.1 Deal with the null value
Here I drop all columns and rows that contains null value.<br>
![null-num]
![null-obj]
5 rows × 40 columns 
## 3.2 Drop the meaningless columns
Feature engineering is a challenge. I will try some method and check the feature importances below.<br>
In order to simplify the project, I just drop the meaningless columns after checking the data dictionary provided by LendingClub.<br>
Reduce the number of columns from 40 to 8.
## 3.3 Prepare the data for sklearn
Ordinal data: map_dic & replace<br>
Nominal data: one-hot encoding<br>
8 columns to 40 columns including both x matrix and y vector.
## 3.4 Peature scaling
Standardization
## 3.5 Feature selecting
After seperate x and y, I choose RFE strategy based on logistic regression classifier to select features.(15 out of 39 features)<br>
For more information of RFE strategy, please search online.<br>
This graph shows the importances of 15 features selected.
!()
# 4. SMOTE method to solve the imbalanced data
# 5. Split the data and train 
* Logistic regression
# 5. Validation
## 5.1 Accuracy 
## 5.2 Confusion Matrix
!()
## 5.3 AUC
# 6. Conclusion
I didn't try every classification model introduced by professor and our textbook within limited time.<br>
There are some points that influence the result:<br>
* Drop columns and rows. ( fill in )
* Select features. (feature engineering)
* Model choose. 
