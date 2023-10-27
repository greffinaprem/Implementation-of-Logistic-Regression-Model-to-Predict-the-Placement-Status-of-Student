# Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student

## AIM:
To write a program to implement the the Logistic Regression Model to Predict the Placement Status of Student.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import the standard libraries.
2. Upload the dataset and check for any null or duplicated values using .isnull() and .duplicated() function respectively.
3. Import LabelEncoder and encode the dataset.
4. Import LogisticRegression from sklearn and apply the model on the dataset.
5. Predict the values of array.
6. Calculate the accuracy, confusion and classification report by importing the required modules from sklearn.
7. Apply new unknown values. 

## Program:
```
/*
Program to implement the the Logistic Regression Model to Predict the Placement Status of Student.
Developed by:GREFFINA SANCHEZ P 
RegisterNumber: 212222040048


#import modules
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt

#reading the file
dataset=pd.read_csv('Placement_Data_Full_Class.csv')
dataset
dataset.head(20)
dataset.tail(20)

#droping tha serial no salary col
dataset = dataset.drop('sl_no',axis=1)
#dataset = dataset.drop('salary',axis=1)
dataset

dataset = dataset.drop('gender',axis=1)
dataset = dataset.drop('ssc_b',axis=1)
dataset = dataset.drop('hsc_b',axis=1)
dataset

dataset.shape
(215, 10)

dataset.info()

#catgorising for further labeling
dataset["degree_t"]=dataset["degree_t"].astype('category')
dataset["specialisation"]=dataset["specialisation"].astype('category')
dataset["status"]=dataset["status"].astype('category')
dataset["hsc_s"]=dataset["hsc_s"].astype('category')
dataset["workex"]=dataset["workex"].astype('category')
dataset.dtypes

dataset.info()

dataset["degree_t"]=dataset["degree_t"].cat.codes
dataset["specialisation"]=dataset["specialisation"].cat.codes
dataset["status"]=dataset["status"].cat.codes
dataset["hsc_s"]=dataset["hsc_s"].cat.codes
dataset["workex"]=dataset["workex"].cat.codes
dataset
dataset.info()
dataset

x = dataset.iloc[:,:-1].values
y = dataset.iloc[:,-1].values
y

from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test = train_test_split(x, y,test_size=0.2)
dataset.head()
x_train.shape
x_test.shape
y_train.shape
y_test.shape

from sklearn.linear_model import LogisticRegression
clf= LogisticRegression()
clf.fit(x_train,y_train)
clf.score(x_test,y_test)

clf.predict([[0, 87, 0, 95, 0, 2, 78, 2, 0]])

*/
```

## Output:

1. Placement data
   
   ![image](https://github.com/greffinaprem/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/119475603/55e25998-74d0-46da-a0ae-8dd167456d14)

2. Salary data

   ![image](https://github.com/greffinaprem/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/119475603/6f0a68f7-b3a5-47a8-847f-3de62afcdb21)

3. Checking the null function()

   ![image](https://github.com/greffinaprem/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/119475603/2453e526-eb31-4c71-bf42-d57c2ab08aa3)

4. Data duplicate

   ![image](https://github.com/greffinaprem/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/119475603/64196b82-c1e4-4ac6-b7ea-95ecc21f3370)

5. Print data

   ![image](https://github.com/greffinaprem/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/119475603/1631f2f4-7419-42de-8f2c-3fc616b5067d)

6. Data status 

   ![image](https://github.com/greffinaprem/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/119475603/0b78d472-d532-4bde-bc98-b7100496cad9)

7. y_prediction array

   ![image](https://github.com/greffinaprem/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/119475603/a7d998e9-d28f-4c4e-90c8-33c2ed0d2cc3)

8. Accuracy value

   ![image](https://github.com/greffinaprem/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/119475603/c88bc71e-01cd-4736-8ecb-ffca90bc2ff8)

9. Confusion matrix

   ![image](https://github.com/greffinaprem/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/119475603/72dbfe36-9c21-4166-a2b1-a06bcf4a2c6d)

10. Classification report

   ![image](https://github.com/greffinaprem/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/119475603/ed04478f-a0d8-42c4-a5e4-323df0910740)

11. Prediction of LR

   ![image](https://github.com/greffinaprem/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/119475603/3b41928e-1a8c-4c60-abe0-d31df21c3b25)


## Result:
Thus the program to implement the the Logistic Regression Model to Predict the Placement Status of Student is written and verified using python programming.
