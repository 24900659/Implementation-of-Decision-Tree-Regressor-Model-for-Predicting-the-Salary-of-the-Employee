# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Import pandas 

2.Import Decision tree classifier 

3.Fit the data in the model 

4.Find the accuracy score


## Program:
```
/*
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by:Mohana K.V.S.L
RegisterNumber:24900659
*/
import pandas as pd
data=pd.read_csv("C:\\Users\\admin\\Desktop\\Salary.csv")
data.head()
data.info()
data.isnull().sum()
from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
data["Position"]=le.fit_transform(data["Position"])
data.head()
x=data[["Position","Level"]]
y=data["Salary"]
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=2)
from sklearn.tree import DecisionTreeRegressor
dt=DecisionTreeRegressor()
dt.fit(x_train,y_train)
y_pred=dt.predict(x_test)
from sklearn import metrics
mse=metrics.mean_squared_error(y_test,y_pred)
mse
r2=metrics.r2_score(y_test,y_pred)
r2
dt.predict([[5,6]])




```

## Output:
![Screenshot (42)](https://github.com/user-attachments/assets/b6ef59d3-73b3-4336-9b20-372872147f06)
![Screenshot (45)](https://github.com/user-attachments/assets/3c89982b-224f-47c2-901b-5faee5861fae)
![Screenshot (46)](https://github.com/user-attachments/assets/a8d4b488-ea2f-42d9-b9c5-b8f21fb42e20)
![Screenshot (47)](https://github.com/user-attachments/assets/7bba53a5-3ba3-4c6f-955b-ec9118ca4ddb)
![Screenshot (47)](https://github.com/user-attachments/assets/bcfff974-0cb3-47ae-978d-fb46f3862a31)
![Screenshot (48)](https://github.com/user-attachments/assets/2dcfcbc1-383e-40f7-836e-7cdea1138c07)
![Screenshot (48)](https://github.com/user-attachments/assets/d8a24e81-a1ef-4009-a891-72cdd81b369d)










## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
