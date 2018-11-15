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
Format: csv<br>
Data size: 42.7 MB<br>
LendingClub provide a formal data dictionary, please check it in folder "data".
## 2.3 Data visualization
 ![image]()
5 rows × 145 columns
# 3. Data preprocessing
## 3.1 Deal with the null value
These two pictures below show the proportion of missing data:<br>
 ![image](https://github.com/HuangJing1801/PHBS_MLF_2018/blob/master/images/output_6_1.png)
 ![image](https://github.com/HuangJing1801/PHBS_MLF_2018/blob/master/images/output_7_1.png)
Here I drop all columns and rows that contains null value.<br>
 ![image]()
5 rows × 40 columns 
## 3.2 Drop the meaningless columns
Feature engineering is a challenge. I will try some method and check the feature importances below.<br>
In order to simplify the project, I just drop the meaningless columns after checking the data dictionary provided by LendingClub.<br>
Reduce the number of "obj" columns from 40 to 8.<br>
Here are the 8 features I choosed:
 ![image]()
## 3.3 Prepare the data for sklearn
Ordinal data: defining a map_dic & replacing<br>
Nominal data: one-hot encoding<br>
The picture below shows the pre-processed data:
 ![image]()
## 3.4 Peature scaling
Standardization
## 3.5 Feature selecting
After seperate x and y, I choose RFE strategy based on logistic regression classifier to select features.(15 out of 39 features)<br>
For more information of RFE strategy, please search online.<br>
This graph shows the importances of 15 features selected.
 ![image](https://github.com/HuangJing1801/PHBS_MLF_2018/blob/master/images/output_8_0.png)
# 4. SMOTE method to solve the imbalanced data
* SMOTE is a method to deal with the imbalanced data. 
* In this project, it is not necessary because the sample size is enough.
* I still keep the code in ipynb file as a reference.
# 5. Split the data and train 
* I use Logistic regression model to do the classifiction in this project.
# 5. Validation
## 5.1 Accuracy 
## 5.2 Confusion Matrix
![image](https://github.com/HuangJing1801/PHBS_MLF_2018/blob/master/images/output_16_1.png)
## 5.3 AUC
# 6. Conclusion
I didn't try every classification model introduced by professor and our textbook within limited time.<br>
There are some points that influence the result:<br>
* Dealing with the missing data: I just drop all columns and rows that contain null value instead of filling in.
* Selecting features. Feature engineering is a big challenge in reality. In my project, I just try my best to make the selection meaningful and interpretable for the model.
* Model choose. The result may be a little bit different if I try to fit other models. But since the result of regression model is not that good, and also I find out that other people's results on this case online is not good either, so I decide to stop here.
