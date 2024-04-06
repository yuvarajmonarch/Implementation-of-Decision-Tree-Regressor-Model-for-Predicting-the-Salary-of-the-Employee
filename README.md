# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import the libraries and read the data frame using pandas.
2. Calculate the null values present in the dataset and apply label encoder.
3. Determine test and training data set and apply decison tree regression in dataset.
4. calculate Mean square error,data prediction and r2.

## Program:
```
/*
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: YUVARAJ B
RegisterNumber:  212222040186

import pandas as pd
data=pd.read_csv("/content/Salary.csv")
data.head()

data.info()

data.isnull().sum()

from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
data['Position']=le.fit_transform(data['Position'])
data.head()

x=data[['Position','Level']]
y=data['Salary']

from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=2)

from sklearn.tree import DecisionTreeClassifier
dt=DecisionTreeClassifier()
dt.fit(x_train,y_train)
y_predict=dt.predict(x_test)

from sklearn import metrics
mse=metrics.mean_squared_error(y_test,y_predict)
mse

r2=metrics.r2_score(y_test,y_predict)
r2

dt.predict([[5,6]])

*/
```

## Output:


## Data.Head():

![image](https://github.com/yuvarajmonarch/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/122221735/7c00ae3d-ffc3-414f-9888-87532d870aa7)




## Data.info():

![image](https://github.com/yuvarajmonarch/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/122221735/d838f4ec-c4f5-4443-a688-4e88c30fb2b6)


## isnull() and sum():

![image](https://github.com/yuvarajmonarch/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/122221735/eaf226be-1b68-476e-9edb-4bad22684a92)



## Data.Head() for salary:

![image](https://github.com/yuvarajmonarch/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/122221735/db074ebc-1ab7-4024-810a-ee57e7c5165d)



## MSE Value:

![image](https://github.com/yuvarajmonarch/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/122221735/83d0784e-a359-4687-8044-1f3aa8e78088)




## r2 Value:

![image](https://github.com/yuvarajmonarch/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/122221735/79fc1a65-b40e-4dc3-9bbf-f0861379bd29)



## Data Prediction:

![image](https://github.com/yuvarajmonarch/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/122221735/01af8c9d-4b9f-4c56-ae0f-21756730faf6)

## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
