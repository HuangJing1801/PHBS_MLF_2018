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
Data size:42.7 MB
## 2.3 Data visualization
id	member_id	loan_amnt	funded_amnt	funded_amnt_inv	term	int_rate	installment	grade	sub_grade	...	hardship_payoff_balance_amount	hardship_last_payment_amount	disbursement_method	debt_settlement_flag	debt_settlement_flag_date	settlement_status	settlement_date	settlement_amount	settlement_percentage	settlement_term
0	NaN	nan	5000.00000	5000.00000	4975.00000	36 months	10.65%	162.87000	B	B2	...	nan	nan	Cash	N	NaN	NaN	NaN	nan	nan	nan
1	NaN	nan	2500.00000	2500.00000	2500.00000	60 months	15.27%	59.83000	C	C4	...	nan	nan	Cash	N	NaN	NaN	NaN	nan	nan	nan
2	NaN	nan	2400.00000	2400.00000	2400.00000	36 months	15.96%	84.33000	C	C5	...	nan	nan	Cash	N	NaN	NaN	NaN	nan	nan	nan
3	NaN	nan	10000.00000	10000.00000	10000.00000	36 months	13.49%	339.31000	C	C1	...	nan	nan	Cash	N	NaN	NaN	NaN	nan	nan	nan
4	NaN	nan	3000.00000	3000.00000	3000.00000	60 months	12.69%	67.79000	B	B5	...	nan	nan	Cash	N	NaN	NaN	NaN	nan	nan	nan
5 rows × 145 columns
# 3. Data preprocessing
## 3.1 Deal with the null value
Here I drop all columns and rows that contains null value.<br>
![null-num]
![null-obj]
5 rows × 40 columns 
## 3.2 Drop the meaningless columns
Feature engineering is a challenge. I will try some method and check the feature importances.<br>
After checking the data dictionary provided by LendingClub, I reduce the number of columns from 40 to 8.
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
## 5.3 AUC
# 6. Conclusion
I didn't try every classification model introduced by professor and our textbook within limited time.<br>
There are some points that influence the result:<br>
* Drop columns and rows. ( fill in )
* Select features. (feature engineering)
* Model choose. 
