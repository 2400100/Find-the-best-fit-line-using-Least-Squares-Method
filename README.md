# Implementation of Univariate Linear Regression
## AIM:
To implement univariate Linear Regression to fit a straight line using least squares.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Get the independent variable X and dependent variable Y.
2. Calculate the mean of the X -values and the mean of the Y -values.
3. Find the slope m of the line of best fit using the formula. 
<img width="231" alt="image" src="https://user-images.githubusercontent.com/93026020/192078527-b3b5ee3e-992f-46c4-865b-3b7ce4ac54ad.png">
4. Compute the y -intercept of the line by using the formula:
<img width="148" alt="image" src="https://user-images.githubusercontent.com/93026020/192078545-79d70b90-7e9d-4b85-9f8b-9d7548a4c5a4.png">
5. Use the slope m and the y -intercept to form the equation of the line.
6. Obtain the straight line equation Y=mX+b and plot the scatterplot.

## Program:
```

Program to implement univariate Linear Regression to fit a straight line using least squares.
Developed by: SUBIKSHA K
RegisterNumber: 212224040332


import numpy as np
import matplotlib.pyplot as plt
x = np.array(eval(input()))
y = np.array(eval(input()))
plt.scatter(x,y)
plt.show()

xmean = np.mean(x)
ymean = np.mean(y)
num=0
den=0

for i in range(len(x)):
    num+=(x[i]-xmean)*(y[i]-ymean)
    den+=(x[i]-xmean)**2

m = num/den
b = ymean - m*xmean
print(m,b)

ypred = m*x+b
print(ypred)

plt.scatter(x,y,color='Red')
plt.plot(x,ypred,color='Blue')
plt.show()

```

## Output:
[5.5,6.6,7.7,8.8,9.9]
[6.1,7.2,8.3,9.4,6.4]

<img width="547" height="413" alt="image" src="https://github.com/user-attachments/assets/e71c29e7-8d45-4cf8-9806-62510fb3db0c" />

0.2545454545454547 5.519999999999999

[6.92 7.2  7.48 7.76 8.04]

<img width="547" height="413" alt="image" src="https://github.com/user-attachments/assets/6e8a8199-c202-4bba-b28b-b875b8c941fa" />


​



## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
