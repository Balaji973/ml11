# Implementation-of-SVM-For-Spam-Mail-Detection.

## AIM:
To write a program to implement the SVM For Spam Mail Detection.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Import required libraries (pandas, chardet, sklearn, etc.).

2.Detect the encoding of the CSV file using chardet.

3.Read the CSV file with the correct encoding.

4.Check the data for structure and missing values.

5.Split the data into input (x = messages) and output (y = labels).

6.Divide the data into training and testing sets.

7.Convert text data into numbers using CountVectorizer.

8.Train an SVM model, make predictions, and calculate accuracy.
 

## Program:
```
/*
Program to implement the SVM For Spam Mail Detection..
Developed by: BALAJI J
RegisterNumber: 212224040042

import chardet
file='spam.csv'
with open(file,'rb')as rawdata:
    result=chardet.detect(rawdata.read(100000))
result

import pandas as pd
data=pd.read_csv("spam.csv",encoding='windows-1252')
data.head()

data.info()

data.isnull().sum()

x=data["v2"].values
y=data["v1"].values
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=0)

from sklearn.feature_extraction.text import CountVectorizer
cv=CountVectorizer()
x_train=cv.fit_transform(x_train)
x_test=cv.transform(x_test)

from sklearn.svm import SVC
svc=SVC()
svc.fit(x_train,y_train)
y_pred=svc.predict(x_test)
y_pred

from sklearn import metrics
accuracy=metrics.accuracy_score(y_test,y_pred)
accuracy 
*/
```

## Output:

## Result output

<img width="1243" height="38" alt="image" src="https://github.com/user-attachments/assets/2d8dabc6-5213-4383-9489-0cdc14cf78ae" />

## data.head()

<img width="1243" height="227" alt="image" src="https://github.com/user-attachments/assets/92e1886f-09fc-42a2-9168-61641668cb55" />

## data.info()

<img width="1231" height="257" alt="image" src="https://github.com/user-attachments/assets/50a39f42-6b8e-44a3-87c1-b80e3501b88d" />

## data.isnull().sum()

<img width="1231" height="130" alt="image" src="https://github.com/user-attachments/assets/a0e4c2f0-06fb-4518-ba6d-3f2faf38c7ca" />

## y_pred

<img width="1243" height="37" alt="image" src="https://github.com/user-attachments/assets/8f5469f8-e023-4ab8-9a45-4583e4426a36" />

## accuracy()

<img width="1243" height="38" alt="image" src="https://github.com/user-attachments/assets/caaa056b-257b-4165-871a-4dccc92190e2" />



## Result:
Thus the program to implement the SVM For Spam Mail Detection is written and verified using python programming.
