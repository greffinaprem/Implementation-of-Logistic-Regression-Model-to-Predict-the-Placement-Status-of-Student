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
![the Logistic Regression Model to Predict the Placement Status of Student](sam.png)

![268977157-de5d941c-4023-486a-b111-5e4e47c9fb7c-1](https://github.com/greffinaprem/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/119475603/ee855738-1895-4fdc-8efb-c243eeb2c92b)


![268977550-f4923b8e-3e29-4f8a-91b8-a62d75241216-1](https://github.com/greffinaprem/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/119475603/52e76697-3c26-45ab-b162-40e927728a46)


![268977806-681f2e45-11f3-436e-b280-eaebf3af1ddc](https://github.com/greffinaprem/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/119475603/2afc5f1e-2da1-41dc-834a-7c9097ba76e2)


![268978309-7c33b7d4-ed7a-457a-a0e0-42343e748bf1](https://github.com/greffinaprem/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/119475603/2788cd59-b3fa-4816-9377-7adb032ba10e)


![268978738-5559febb-524c-48b1-8866-c408c1bb5b6a](https://github.com/greffinaprem/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/119475603/48e187fd-00f3-4467-8233-ca803f235255)


![268979289-e6d0ce35-6e55-4eef-b11c-aeebb1356bc9](https://github.com/greffinaprem/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/119475603/17e577c1-c4be-4a19-bae4-f1922d600bab)


![268979573-fceb1521-b73b-4ae8-a975-b34cc4a69914](https://github.com/greffinaprem/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/119475603/4bd60717-57f4-44ed-8d6d-b6dcb62a6c27)


![268990921-8bc1429a-e26d-4dc4-a6b0-ad61d2a1a8dd](https://github.com/greffinaprem/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/119475603/aee0a765-a97f-4c1e-b21c-796799f62460)


![268982234-01c5a594-2c55-44bb-ac56-5f8b464ddb24](https://github.com/greffinaprem/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/119475603/e5afb98a-1b07-4fd4-85bd-ebb155d66d0d)


![268979982-c7ca28c2-5fa8-4819-a134-944b07073f3c](https://github.com/greffinaprem/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/119475603/0c34f960-6d41-4812-92c8-60eb6e73b31d)


![268987729-2d5cf1df-5666-40cb-a08c-e1551da7c517](https://github.com/greffinaprem/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/119475603/307affb6-f9d4-40c7-89e1-a33629e34f4e)




## Result:
Thus the program to implement the the Logistic Regression Model to Predict the Placement Status of Student is written and verified using python programming.
