# Implementation-of-Linear-Regression-Using-Gradient-Descent

## AIM:
To write a program to predict the profit of a city using the linear regression model with gradient descent.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. 
2. 
3. 
4. 

## Program:
```
/*
Program to implement the linear regression using gradient descent.
Developed by:mirushika.t 
RegisterNumber:24901203  
*/
```
import numpy as np 
import matplotlib.pyplot as plt
X=np.array(eval(input()))
Y=np.array(eval(input()))
X_mean =np.mean(X)
Y_mean =np.mean(Y)
num=0
denom=0
for i in range(len(X)):
    num+=(X[i]-X_mean)*(Y[i]-Y_mean)
    denom+=(X[i]-X_mean)**2
m=num/denom
b=Y_mean - m*X_mean
print(m,b)
Y_predicted=m*X+b
print(Y_predicted)
plt.scatter(X,Y)
plt.plot(X,Y_predicted,color='red')
plt.show()
## Output:
![linear regression using gradient descent](sam.png)
 8,2,11,6,5,4,12,9,6,1
 3,10,3,6,8,12,1,4,9,14

-1.1064189189189189 14.08108108108108
[ 5.22972973 11.86824324  1.91047297  7.44256757  8.54898649  9.65540541
  0.80405405  4.12331081  7.44256757 12.97466216]




![Screenshot 2024-10-17 204624](https://github.com/user-attachments/assets/7de4f0b2-f2b6-414d-83c3-9af4246559cb)


## Result:
Thus the program to implement the linear regression using gradient descent is written and verified using python programming.
