# Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn

## AIM:
To write a program to implement the Decision Tree Classifier Model for Predicting Employee Churn.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
Step 1:Start

Step 2:Import pandas and read the csv file.

Step 3:Import Decision tree classifier.

Step 4:Fit the data in the model.

Step 5:Find the accuracy score

Step 6:STOP
## Program:
```
/*
Program to implement the Decision Tree Classifier Model for Predicting Employee Churn.
Developed by: Abinav Sankar S
RegisterNumber: 212222040002

import pandas as pd
df=pd.read_csv("CSVs/Employee.csv")
df.head()
df.info()
df.isnull().sum()
df['left'].value_counts()
from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
df["salary"]=le.fit_transform(df['salary'])
df.head()
x=df[['satisfaction_level','last_evaluation','number_project','average_montly_hours',
      'time_spend_company','Work_accident','promotion_last_5years','salary']]
x.head()
y=df['left']
from sklearn.model_selection import train_test_split as tts
Xtrain,Xtest,Ytrain,Ytest=tts(x,y,test_size=0.2,random_state=100)








from sklearn.tree import DecisionTreeClassifier
dt=DecisionTreeClassifier(criterion='entropy')
dt.fit(Xtrain,Ytrain)
Ypred=dt.predict(Xtest)
from sklearn import metrics
accuracy=metrics.accuracy_score(Ytest,Ypred)
accuracy
dt.predict([[0.5,0.8,9,260,6,0,1,2]])

*/
```

## Output:
## df.head():
![image](https://github.com/Abinavsankar/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/119103734/32a2706b-f753-4e59-9ef5-5bcc652a4a44)

## df.info():
![image](https://github.com/Abinavsankar/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/119103734/5600a66e-a229-4c4c-8799-723b87a3cc31)

## df.isnull().sum():
![image](https://github.com/Abinavsankar/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/119103734/ca7661fa-d860-4f33-8591-b033828b67d3)

## df['left'].value_counts():
![image](https://github.com/Abinavsankar/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/119103734/53475c45-778f-45bf-8781-50a5ca987e53)

## df["salary"]:
![image](https://github.com/Abinavsankar/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/119103734/20a4a4d5-bdd6-4892-a8e5-f793ccf705d2)

## x.head():
![image](https://github.com/Abinavsankar/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/119103734/18b58e97-9203-46d3-bef4-775350516640)

## Accuracy:
![image](https://github.com/Abinavsankar/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/119103734/8aaa5e98-7e3f-4b78-866c-3d8f0543a2b5)

## dt.predict:
![image](https://github.com/Abinavsankar/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/119103734/f1565669-c894-4714-9bc8-c61b7683c0b9)

## Result:
Thus the program to implement the  Decision Tree Classifier Model for Predicting Employee Churn is written and verified using python programming.
