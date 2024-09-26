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
Developed by: VINOTH M P
RegisterNumber:  212223240182

import numpy as np
import matplotlib.pyplot as plt

X=np.array(eval(input()))
Y=np.array(eval(input()))
```
![image](https://github.com/user-attachments/assets/c52ef4fa-1ad2-485e-9ccd-d0de7a41b650)

```
X_mean=np.mean(X)
print(X_mean)


Y_mean=np.mean(Y)
print(Y_mean)
num=0
denum=0
for i in range(len(X)):
  num+=(X[i]-X_mean)*(Y[i]-Y_mean)
  denum+=(X[i]-X_mean)**2
m=num/denum
print(m)
```
![image](https://github.com/user-attachments/assets/ee697820-9bbf-403f-90ad-ce3d2a1af87b)

```
b=Y_mean - m*X_mean
print(b)
```
![image](https://github.com/user-attachments/assets/b4a267bf-e296-4a9e-bd3e-91db9916df44)

```
Y_pred=m*X+b
print(Y_pred)
```
![image](https://github.com/user-attachments/assets/981f93cb-4b57-443c-8531-e563efc15b98)

```
plt.scatter(X,Y,color='blue')
plt.plot(X,Y_pred,color='yellow') 
plt.show()

```

## Output:

![image](https://github.com/user-attachments/assets/6a0978e4-ba04-4a6e-bde6-413b1b3f58d7)




## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
