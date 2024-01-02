# Implementation of Univariate Linear Regression
## Aim:
To implement univariate Linear Regression to fit a straight line using least squares.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
## step 1:
Get the independent variable X and dependent variable Y.
## step 2:
Calculate the mean of the X -values and the mean of the Y -values.
## step 3:
Find the slope m of the line of best fit using the formula.
 ![eqn1](./eq1.jpg)
## step 4:
Compute the y -intercept of the line by using the formula:
![eqn2](./eq2.jpg)  
## step 5:	Use the slope m and the y -intercept to form the equation of the line.
6.	Obtain the straight line equation Y=mX+b and plot the scatterplot.
## Program
```
#Univariate linear regression
#Developed by:ajina joshpin
#Regster number:23013547

import numpy as np

import matplotlib.pyplot as plt

x=np.array([0,1,2,3,4,5,6,7,8,9])

y=np.array([1,3,2,5,7,8,8,9,10,12])

plt.scatter(x,y)

plt.show()

xmean=np.mean(x)

ymean=np.mean(y)

num=0

den=0

for i in range(len(x)):

    num+=(x[i]-xmean)*(y[i]-ymean)

    den+=(x[i]-xmean) **2

m=num/den

b=ymean-m*xmean

print(m,b)

ypred=m*x+b

print(ypred)

plt.scatter(x,y,color="Red")

plt.plot(x,ypred, color="Blue")

plt.show()


```
## ouput:
![Screenshot 2024-01-02 124303](https://github.com/ajinajoshpin/Univariate-Linear-Regression/assets/148514578/e03455c4-94cc-4170-b809-33f6568ebe3d)

![Screenshot 2024-01-02 124323](https://github.com/ajinajoshpin/Univariate-Linear-Regression/assets/148514578/9dd92f1a-8933-42aa-8e47-fdffb0ab75f1)

![Screenshot 2024-01-02 124405](https://github.com/ajinajoshpin/Univariate-Linear-Regression/assets/148514578/d251dd21-b4a7-4bdc-9f71-86131fe24c93)

![Screenshot 2024-01-02 124417](https://github.com/ajinajoshpin/Univariate-Linear-Regression/assets/148514578/6108c761-d137-44be-829a-e35cd983e408)


## Result
Thus the univariate Linear Regression was implemented to fit a straight line using least squares.
