# bank-churn using logistic regression.

the eda has been done on the power bi to gain the insights as fast as possible.

it has been observed that the attrition flag(output) is not balanced.

training data has been scaled using the standard scaler everytime and stratified option is enabled while making train test split

below are results - cross val score of accuracy and classfication report at each instance

## simple logistic regression - 


![image](https://user-images.githubusercontent.com/68850280/179797127-141723a0-b08d-4eb1-880a-e98ddbbb5741.png)

# logistic regression by undersampling the majority class

![image](https://user-images.githubusercontent.com/68850280/179797667-13dbc267-994f-4e13-8216-e17f8f49a398.png)

# logistic regression by oversampling the minority class

![image](https://user-images.githubusercontent.com/68850280/179797821-64535100-87d7-40ca-adc6-140d0d4d676a.png)

# logistic regression by using SMOTE with sampling_strategy='minority'

![image](https://user-images.githubusercontent.com/68850280/179798019-eb4868bd-080a-4f2e-b7f1-d4d35cbe79a1.png)

 -- at this point the results of SMOTE , oversampling the minority class , undersampling the majority class performing far better to the normal logistic regression.
we did all the above process with 23 features and i decided to do feature elimination.

# below are reults when RFECV and SMOTE used (rfecv REDUCED TO 20 FEATURES)

![image](https://user-images.githubusercontent.com/68850280/179798741-d6ee101c-08c0-4042-a192-037a556e9f66.png)

# below are reults when RFE and SMOTE used (allowed to use 10 features)

![image](https://user-images.githubusercontent.com/68850280/179799024-b408a8db-def6-4447-b682-1a394fcd1eab.png)


# below are reults when RFE and SMOTE used (allowed to use 15 features)

![image](https://user-images.githubusercontent.com/68850280/179799196-c66c54b3-2dd2-4c64-82f3-a1a99c5799a8.png)
