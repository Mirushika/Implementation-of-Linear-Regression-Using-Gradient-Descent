# Implementation-of-Linear-Regression-Using-Gradient-Descent

## AIM:
To write a program to predict the profit of a city using the linear regression model with gradient descent.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
```
1.Import necessary libraries. 
2.Compute predictions using the formula: predictions = X.dot(theta). 
3.Load the dataset using pd.read_csv() 
4.Compute the prediction using the formula:
         \text{prediction} = \text{dot product of } (\text{new_data and } \theta). 
5.Print the predicted value (pre), representing the estimated profit based on input features.
```
## Program:
```
/*
Program to implement the linear regression using gradient descent.
Developed by:mirushika.t 
RegisterNumber:24901203  
*/
```
```
import numpy as np
import pandas as pd
from sklearn.preprocessing import StandardScaler
def linear_regression(X1,y,learning_rate=0.01,num_iters=1000):
    X=np.c_[np.ones(len(X1)),X1]
    theta=np.zeros(X.shape[1]).reshape(-1,1)
    for _ in range(num_iters):
        predictions=(X).dot(theta).reshape(-1,1)
        errors=(predictions-y).reshape(-1,1)
        theta=learning_rate*(1/len(X1))*X.T.dot(errors)
    return theta
data=pd.read_csv('50_Startups.csv',header=None)
X=(data.iloc[1:, :-2].values)
X1=X.astype(float)
scaler=StandardScaler()
y=(data.iloc[1:,-1].values).reshape(-1,1)
X1_Scaled=scaler.fit_transform(X1)
Y1_Scaled=scaler.fit_transform(y)
print(data.head())

theta=linear_regression(X1_Scaled, Y1_Scaled)
new_data=np.array([165349.2,136897.8,471784.1]).reshape(-1,1)
new_Scaled=scaler.fit_transform(new_data)
prediction=np.dot(np.append(1, new_Scaled),theta)
prediction=prediction.reshape(-1,1)
pre=scaler.inverse_transform(prediction)
print(f"Predicted value: {pre}") ```
```
## Output:
![linear regression using gradient descent](sam.png)





![Screenshot 2024-11-13 222114](https://github.com/user-attachments/assets/4b6ab6ce-2e31-414d-a5f8-603453b44ce6)



## Result:
Thus the program to implement the linear regression using gradient descent is written and verified using python programming.
