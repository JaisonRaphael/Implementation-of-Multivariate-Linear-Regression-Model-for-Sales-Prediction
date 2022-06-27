# Implementation-of-Multivariate-Linear-Regression-Model-for-Sales-Prediction

## AIM:
To write a program to implement the multivariate linear regression model for sales prediction.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm

## STEP 1:
Import the required libraries.
## STEP 2:
Read the csv file using pandas.
## STEP 3:
Declare X and Y variable with respect to the dataset.
## STEP 4:
Predict the values.
## STEP 5:
Using Mean Squared Error find the required line that fits the data.
## STEP 6:
Print the Mean Squared Error and R squared error.
## STEP 7:

## Program:
```
/*
Program to implement the multivariate linear regression model for sales prediction.
Developed by: Jaison Raphael.V
RegisterNumber:  212221230038
*/
```
~~~
import pandas as pd
import matplotlib.pyplot as plt
df = pd.read_csv('Advertising_data.csv')
df.head()
df.describe()
df.isnull().sum()
x = df[['TV','Radio','Newspaper']]
y = df["Sales"]
from sklearn.model_selection import train_test_split
x_train, x_test,y_train,y_test = train_test_split(x,y,test_size=0.2, random_state=101)
from sklearn.linear_model import LinearRegression
l = LinearRegression()
l.fit(x_train,y_train)
y_pred = l.predict(x_test)
print("Regression Slope: ",l.coef_[0])
print("Regression Intercept:",l.intercept_)
from sklearn import metrics
MSE = metrics.mean_squared_error(y_test,y_pred)
print("MSE is {}".format(MSE))
r2 = metrics.r2_score(y_test,y_pred)
print("R Squared Error is {} ".format(r2))
l.predict([[150.3,240.5,234.5]])
~~~

## Output:
![1 (3)](https://user-images.githubusercontent.com/94165957/175854169-3c6754f7-fb95-40b2-b3bf-c9f918c580f6.png)


## Result:
Thus the program to implement the multivariate linear regression model for sales prediction is written and verified using python programming.
