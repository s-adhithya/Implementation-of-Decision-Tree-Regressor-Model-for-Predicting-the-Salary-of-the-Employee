# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs

2. Anaconda – Python 3.7 Installation / Jupyter notebook
## Algorithm
### Step 1.
Import the libraries and read the data frame using pandas.

### Step 2.
Calculate the null values present in the dataset and apply label encoder.

### Step 3.
Determine test and training data set and apply decison tree regression in dataset.

### Step 4.
Calculate Mean square error,data prediction and r2.

## Program:
```
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: Adhithya.S
RegisterNumber: 212222240003
import pandas as pd
data=pd.read_csv("Salary.csv")
data.head()
data.info()
data.isnull().sum()
from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
data["Position"]=le.fit_transform(data["Position"])
data.head()
x=data[["Position","Level"]]
x.head()
y=data[["Salary"]]
from sklearn.model_selection import train_test_split
x_train, x_test, y_train, y_test=train_test_split(x,y,test_size=0.2,random_state=2)
from sklearn.tree import DecisionTreeRegressor
dt=DecisionTreeRegressor()
dt.fit(x_train,y_train)
y_pred=dt.predict(x_test)
from sklearn import metrics
mse=metrics.mean_squared_error(y_test, y_pred)
mse
r2=metrics.r2_score(y_test,y_pred)
r2
dt.predict([[5,6]])
```
## Output:
### data.head()
![image](https://github.com/s-adhithya/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/113497423/83b6100f-6440-41fe-8cb0-278ea9feb1ab)


### data.info()
![image](https://github.com/s-adhithya/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/113497423/1a0f7020-2d22-4527-b075-e00b220191cc)


### isnull() and sum()
![image](https://github.com/s-adhithya/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/113497423/6e5678b0-1b19-4291-a1b1-f25a73928217)


### data.head() for salary
![image](https://github.com/s-adhithya/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/113497423/872a9681-ead5-46c2-9526-595a53fe286e)


### data.head() for salary
![image](https://github.com/s-adhithya/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/113497423/f0489802-d806-4ea6-89d6-19098907eeff)


### MSE value
![image](https://github.com/s-adhithya/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/113497423/e09b9ae6-c41b-42a7-bb16-1de87cb30fc7)


### R2 value
![image](https://github.com/s-adhithya/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/113497423/5fd4d2d3-4478-4675-ab8e-1df0f53c176d)


### prediction value
![image](https://github.com/s-adhithya/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/113497423/73ae7813-524e-4391-b813-32a91eabb9c9)

## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
