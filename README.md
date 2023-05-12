# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import the required packages.
2. Read the data set.
3. Apply label encoder to the non-numerical column inoreder to convert into numerical values.
4. Determine training and test data set.
5. Apply decision tree regression on to the dataframe and get the values of Mean square error, r2 and data prediction.

## Program:
```
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by : D.vishnu vardhan reddy
Register Number :  212221230023
```
```
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
#### 1. data.head()

![image](https://github.com/vishnudorigundla/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/94175324/dbdfeeeb-8ca1-46b1-be89-9231678ef68d)

#### 2. data.info()

![image](https://github.com/vishnudorigundla/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/94175324/376bf700-e4ce-48a3-a463-1cc6c403c5b2)

#### 3. Null values

![image](https://github.com/vishnudorigundla/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/94175324/5b3b4d1f-5fd7-4281-b4ba-fb8a6b271c58)

#### 4. data.head() for position

![image](https://github.com/vishnudorigundla/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/94175324/40a43f9e-d197-47b0-8cb8-38cb80f8de3c)

#### 5. x.head()

![image](https://github.com/vishnudorigundla/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/94175324/b169da74-a801-4698-9e37-8222161ecdc5)

#### 6. Mean squared error(mse) value

![image](https://github.com/vishnudorigundla/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/94175324/7cee22fb-6cac-4dd6-a39f-1c73dd8bac7b)


#### 7. r2 value

![image](https://github.com/vishnudorigundla/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/94175324/376b8e2f-65ed-4dac-a696-eb010213b2c0)


#### 8. prediction value

![image](https://github.com/vishnudorigundla/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/94175324/3abf3990-0897-4859-9601-17e213c8764a)


## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
