# Implementation-of-SVM-For-Spam-Mail-Detection

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
Developed by: LINCE GIYO L
RegisterNumber: 212225100023

import chardet

file = 'spam (1).csv'

with open(file, 'rb') as rawdata:
    result = chardet.detect(rawdata.read(100000))

print(result)

import pandas as pd

data = pd.read_csv('spam (1).csv', encoding='Windows-1252')

print(data.info())

print(data.isnull().sum())

# Correct columns
x = data["v2"].values   # message text
y = data["v1"].values   # spam/ham labels

from sklearn.model_selection import train_test_split

x_train, x_test, y_train, y_test = train_test_split(
    x, y, test_size=0.2, random_state=0
)

from sklearn.feature_extraction.text import CountVectorizer

cv = CountVectorizer()

x_train = cv.fit_transform(x_train)
x_test = cv.transform(x_test)

from sklearn.svm import SVC

svc = SVC()

svc.fit(x_train, y_train)

y_pred = svc.predict(x_test)

print(y_pred)

from sklearn import metrics

accuracy = metrics.accuracy_score(y_test, y_pred)

print("Accuracy:", accuracy)
*/
```

## Output:

Result output
<img width="1243" height="38" alt="image" src="https://github.com/user-attachments/assets/2ffe12ee-a8a0-45cf-9c12-673a82726f82" />

data.head():
<img width="1243" height="227" alt="image" src="https://github.com/user-attachments/assets/860bfc8e-6315-466c-bba8-29dffe54379a" />

data.info():
<img width="1231" height="257" alt="image" src="https://github.com/user-attachments/assets/038d1d55-43af-4fb9-8674-cc680ac3ca15" />

data.isnull().sum():
<img width="1231" height="130" alt="image" src="https://github.com/user-attachments/assets/94e6e5ac-7e6a-403c-a6ee-f6c901472b2c" />

y_pred:
<img width="1243" height="37" alt="image" src="https://github.com/user-attachments/assets/e840293c-6bd1-439c-a6b0-0aa4e4231ae4" />

accuracy():
<img width="1243" height="38" alt="image" src="https://github.com/user-attachments/assets/6a989139-62df-4c08-9938-f3485d5241ae" />


## Result:
Thus the program to implement the SVM For Spam Mail Detection is written and verified using python programming.
