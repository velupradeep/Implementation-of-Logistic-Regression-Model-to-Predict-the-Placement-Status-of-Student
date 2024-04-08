

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

```




```
   

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
data1=data.copy()
data1=data1.drop(["sl_no","salary"],axis=1)
data1.head()
data1.isnull()
data1.duplicated().sum()
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
x=data1.iloc[:,:-1]
x
y=data1["status"]
y
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=0)
from sklearn.linear_model import LogisticRegression
lr=LogisticRegression(solver="liblinear")
lr.fit(x_train,y_train)
y_pred=lr.predict(x_test)
y_pred
from sklearn.metrics import accuracy_score
accuracy=accuracy_score(y_test,y_pred)
accuracy
from sklearn.metrics import classification_report
classification_report1=classification_report(y_test,y_pred)
print(classification_report1)
lr.predict([[1,80,1,90,1,1,90,1,0,85,1,85]])

```

```







```


## Output:
# Head
![image](https://github.com/velupradeep/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/150329341/cadafe0e-aa47-480d-b42e-a6d59b84bbb3)

# Head after dropping sl_n0 and Salary
![image](https://github.com/velupradeep/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/150329341/99d0e988-abd5-4093-9df7-6ef53c5bd361)
```


```

# isnull()
![image](https://github.com/velupradeep/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/150329341/acf9ae90-4d05-4a57-9cea-6058b2cd3a3e)

# Duplicated(),sum()
![image](https://github.com/velupradeep/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/150329341/18d68e5e-784c-496e-9945-416f3b3fd654)

```








```

# Data 1
![image](https://github.com/velupradeep/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/150329341/e245313e-8ea6-45cb-bc66-8caa421e8540)
```




```

# X
![image](https://github.com/velupradeep/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/150329341/450008c7-e5f2-4d90-adbf-ad21bc9de1bd)

```





```

# Y
![image](https://github.com/velupradeep/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/150329341/8e836549-e412-4135-8545-888541ec77b5)

# Y_pred
![image](https://github.com/velupradeep/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/150329341/a0ff7084-be66-4f2d-bb09-a7fee17ed913)

# Accuracy
![image](https://github.com/velupradeep/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/150329341/b8908446-0c1f-4cac-8e89-260424e97162)

# Classification report
![image](https://github.com/velupradeep/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/150329341/c3c8abb3-f13b-4fe7-806a-92237ab80ef2)

# Predict
![image](https://github.com/velupradeep/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/150329341/10450fb5-1f2c-4414-a205-7cad40e98396)

## Result:
Thus the program to implement the the Logistic Regression Model to Predict the Placement Status of Student is written and verified using python programming.
