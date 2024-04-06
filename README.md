                                                        #NAME:PRADEEP V
                                                        #REG N0:212223240119

# Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student

## AIM:
To write a program to implement the the Logistic Regression Model to Predict the Placement Status of Student.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import pandas library to read CSV or excel files.
2. Import LabelEncoder using sklearn.preprocessing library.
3. Import LabelEncoder using sklearn.preprocessing library.
4. Import Logistic regression module from sklearn.linear_model library to predict the values.
5. Find accuracy, confusion matrix ,and classification report using sklearn.metrics library.
6. Predict for the new given values. End of the program.
   

## Program:
```
/*
Program to implement the the Logistic Regression Model to Predict the Placement Status of Student.
Developed by: PRADEEP V
RegisterNumber:  212223240119
*/
```
```
import pandas as pd
data=pd.read_csv("C:/Users/PRADEEP V/Desktop/Placement_Data.csv")
data.head()
```
```
data1=data.copy()
data1=data1.drop(["sl_no","salary"],axis=1)
data1.head()
```
```
data1.isnull()
```
```
data1.duplicated().sum()
```
```
from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
data1["gender"]=le.fit_transform(data1["gender"])
data1["ssc_b"]=le.fit_transform(data1["ssc_b"])
data1["hsc_b"]=le.fit_transform(data1["hsc_b"])
data1["hsc_s"]=le.fit_transform(data1["hsc_s"])
data1["degree_t"]=le.fit_transform(data1["degree_t"])
data1["workex"]=le.fit_transform(data1["workex"])
data1["specialisation"]=le.fit_transform(data1["specialisation"])
data1["status"]=le.fit_transform(data1["status"])
data1
```
```
x=data1.iloc[:,:-1]
x
```
```
y=data1["status"]
y
```
```
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=0)
```
```
from sklearn.linear_model import LogisticRegression
lr=LogisticRegression(solver="liblinear")
lr.fit(x_train,y_train)
y_pred=lr.predict(x_test)
y_pred
```
```
from sklearn.metrics import accuracy_score
accuracy=accuracy_score(y_test,y_pred)
accuracy
```
```
from sklearn.metrics import classification_report
classification_report1=classification_report(y_test,y_pred)
print(classification_report1)
```
```
lr.predict([[1,80,1,90,1,1,90,1,0,85,1,85]])
```


## Output:

![image](https://github.com/velupradeep/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/150329341/8f1a2f1c-26f8-40ec-ab83-488e87cfda4e)

![image](https://github.com/velupradeep/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/150329341/01415065-bafd-411d-9dfa-55613d2a3774)

![image](https://github.com/velupradeep/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/150329341/a4e5c22d-099e-4fae-a79a-15c2b6311eb8)

![image](https://github.com/velupradeep/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/150329341/684f1f6c-f893-4fbc-8f4c-d220a55c8213)

![image](https://github.com/velupradeep/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/150329341/97a1a1af-622f-430c-bb86-fa85b2862bb8)

![image](https://github.com/velupradeep/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/150329341/2e77797f-6e92-4497-a759-44fe45a314e1)

![image](https://github.com/velupradeep/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/150329341/f61e62b6-cbb4-468b-8161-6d4b3dae457a)

![image](https://github.com/velupradeep/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/150329341/fa3a6204-d076-4044-a8fc-7b80a437f54d)

![image](https://github.com/velupradeep/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/150329341/0cce6c02-bd39-466b-b879-243a61473c8b)


## Result:
Thus the program to implement the the Logistic Regression Model to Predict the Placement Status of Student is written and verified using python programming.
