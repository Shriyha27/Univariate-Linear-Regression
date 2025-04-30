# Implementation of Univariate Linear Regression
## Aim:
To implement univariate Linear Regression to fit a straight line using least squares.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
1.	Get the independent variable X and dependent variable Y.
2.	Calculate the mean of the X -values and the mean of the Y -values.
3.	Find the slope m of the line of best fit using the formula.
4.	![eqn1](./eq1.jpg)
5.	Compute the y -intercept of the line by using the formula:
6.	![eqn2](./eq2.jpg)  
7.	Use the slope m and the y -intercept to form the equation of the line.
8.	Obtain the straight line equation Y=mX+b and plot the scatterplot.
## Program
```
Developed by: V.Shriyha
Reg.no: 212224230267

import numpy as np
X=np.array(eval(input()))
Y=np.array(eval(input()))
X_mean=np.mean(X)
Y_mean=np.mean(Y)
num=0
denom=0
for i in range(len(X)):
    num+=(X[i]-X_mean)*(Y[i]-Y_mean)
    denom+=(X[i]-X_mean)**2
m=num/denom
c=Y_mean-m*X_mean
print(m,c)
Y_Pred=m*X+c
print(Y_Pred)

import matplotlib.pyplot as plt
plt.scatter(X,Y,color='pink')
plt.plot(X,Y_Pred,color='blue')
plt.show()
```
## Output

![Screenshot 2025-04-30 112710](https://github.com/user-attachments/assets/3cac8169-1893-4e54-a4f0-92ddefd1917e)

## Result
Thus the univariate Linear Regression was implemented to fit a straight line using least squares.
