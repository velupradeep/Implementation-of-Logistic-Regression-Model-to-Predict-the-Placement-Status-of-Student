# EX-04 Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student

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
data=pd.read_csv("C:/Users/admin/Downloads/Placement_Data.csv")
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
lr=LogisticRegression(solver='liblinear')
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
# head
![320196507-a1ddf9ac-987f-413e-9e1d-b1f4eb701291](https://github.com/velupradeep/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/150329341/1b13cb70-9941-4dd9-a5c0-1167b5bdf46d)
# head after dropping sl_n0 and Salary
![320196553-4cbe1341-7068-4673-b57b-7fd5a49dd0ab](https://github.com/velupradeep/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/150329341/dc0e1d61-bffa-4816-ad46-2df42064ad12)
# isnull()
![320196581-ad3d675c-b756-4625-a35c-b688cd8385e0](https://github.com/velupradeep/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/150329341/eb1f0408-1a71-4663-b143-ac6d094ce2ac)
# duplicated(),sum()
![320196601-05f7731b-1526-4a5f-89ae-e289ed729e49](https://github.com/velupradeep/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/150329341/ea6df0f8-3ccc-4059-81a8-527ad17353cd)
# data 1
![320196640-135e89f6-649f-4960-8096-3b1c498b5e3d](https://github.com/velupradeep/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/150329341/fc8c119b-739c-4265-92c3-29b790f19a64)
# X
![320196620-503a0d02-9a5c-4414-97e5-f4d7ab095144](https://github.com/velupradeep/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/150329341/aae697b5-9a0a-4c51-850a-e5fc82b7e870)
# Y
![320196649-eac0513a-7d91-4215-85e2-04e9678f38b6](https://github.com/velupradeep/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/150329341/f0a49f9b-6126-4dd3-b3af-f91655bd8efb)
# Y_pred
![320196671-f04cc7ea-233a-4a2a-9e01-8be72732b26c](https://github.com/velupradeep/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/150329341/19f983bb-b8cf-4343-9473-92a756d9c3bd)
# Accuracy
![320196725-03b4af28-c99a-42eb-927c-376aaebf3866](https://github.com/velupradeep/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/150329341/a7b1cb35-e430-4288-a9d9-5245a31e0988)
# Classification report
![320196705-14fc1bad-f245-4531-971d-282c049711d1](https://github.com/velupradeep/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/150329341/c234ed41-ef23-4da4-9282-2885a3034e33)
# Predict
![320196720-4b0e911d-9017-488e-88bc-903791e5a413](https://github.com/velupradeep/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/150329341/6422aa82-5862-4787-a1d9-bb17d14b94d6)
## Result:
Thus the program to implement the the Logistic Regression Model to Predict the Placement Status of Student is written and verified using python programming.
