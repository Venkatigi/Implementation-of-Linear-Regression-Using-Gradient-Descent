# Implementation-of-Linear-Regression-Using-Gradient-Descent

## AIM:
To write a program to implement the linear regression using gradient descent.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1. 1.Use the standard libraries in python for finding linear regression.
2. Set variables for assigning dataset values.
3. Import linear regression from sklearn.
4. Assign the points for representing in the graph
5. Predict the regression for marks by using the representation of the graph.
6. Compare the graphs and hence we obtained the linear regression for the given datas.

## Program:
```
Program to implement the linear regression using gradient descent.
Developed by   : Venkatesh E
RegisterNumber : 212221230119

import pandas as pd
import matplotlib.pyplot as plt
data=pd.read_csv('/content/student_scores - student_scores.csv')
data.head()
data.isnull().sum()
x=data.Hours
x.head()
y=data.Scores
y.head()
n=len(x)
m=0
c=0
L=0.01
loss=[]
for i in range(10000):
  ypred=m*x+c
  MSE=(1/n)*sum((ypred-y)*2)
  dm=(2/n)*sum(x*(ypred-y))
  dc=(2/n)*sum(ypred-y)
  c=c-L*dc
  m=m-L*dm
  loss.append(MSE)
print(m,c)
y_pred=m*x+c
plt.scatter(x,y,color='black')
plt.plot(x,y_pred)
plt.xlabel('Study Hours')
plt.ylabel('Scores')

plt.title('Study Hours vs Scores')
plt.plot(loss)
plt.xlabel('Iterations')
plt.ylabel('Loss')
```

## Output:
![OUTPUT](1.jpg)
![output](2.jpg)

## Result:
Thus the program to implement the linear regression using gradient descent is written and verified using python programming.
