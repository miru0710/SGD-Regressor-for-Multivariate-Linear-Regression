# SGD-Regressor-for-Multivariate-Linear-Regression

## AIM:
To write a program to predict the price of the house and number of occupants in the house with SGD regressor.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import the required libraries and create the input features and output values.
2. Create an SGDRegressor model and use MultiOutputRegressor for predicting multiple outputs.
3. Train the model using the given input and output data.
4. Predict the outputs for the given data and a new sample.
5. Display the actual and predicted values and plot the results. 

## Program:
```
/*
Program to implement the multivariate linear regression model for predicting the price of the house and number of occupants in the house with SGD regressor.
Developed by: MIRUDHULA.N
RegisterNumber: 212225220063
from sklearn.linear_model import SGDRegressor
from sklearn.multioutput import MultiOutputRegressor
import numpy as np
import matplotlib.pyplot as plt

X = np.array([
    [1, 2],
    [2, 1],
    [3, 4],
    [4, 3],
    [5, 5],
    [6, 7],
    [7, 6]
])


Y = np.array([
    [5, 8],
    [6, 9],
    [9,12],
    [10,13],
    [13,16],
    [16,20],
    [17,21]
])

sgd = SGDRegressor(
    max_iter=1000,
    eta0=0.01,
    learning_rate='constant',
    random_state=42
)

model = MultiOutputRegressor(sgd)

model.fit(X, Y)

Y_pred = model.predict(X)

print("\nActual Outputs")
print(Y)

print("\nPredicted Outputs")
print(np.round(Y_pred,2))

new_sample = np.array([[8, 7]])
prediction = model.predict(new_sample)

print("\nPrediction for", new_sample)
print(prediction)


plt.figure(figsize=(6,4))
plt.scatter(Y[:,0], Y_pred[:,0], color='blue')
plt.plot([Y[:,0].min(), Y[:,0].max()],
         [Y[:,0].min(), Y[:,0].max()],
         'r--')
plt.xlabel("Actual Output 1")
plt.ylabel("Predicted Output 1")
plt.title("Output 1: Actual vs Predicted")
plt.grid(True)
plt.show()

plt.figure(figsize=(6,4))
plt.scatter(Y[:,1], Y_pred[:,1], color='green')
plt.plot([Y[:,1].min(), Y[:,1].max()],
         [Y[:,1].min(), Y[:,1].max()],
         'r--')
plt.xlabel("Actual Output 2")
plt.ylabel("Predicted Output 2")
plt.title("Output 2: Actual vs Predicted")
plt.grid(True)
plt.show()

 
*/
```

## Output:
<img width="1090" height="742" alt="image" src="https://github.com/user-attachments/assets/2c529631-835f-4eb1-8503-9f6e3be653d2" />
<img width="627" height="401" alt="image" src="https://github.com/user-attachments/assets/15b5b2d0-0251-438d-afb1-683a4082616a" />


## Result:
Thus the program to implement the multivariate linear regression model for predicting the price of the house and number of occupants in the house with SGD regressor is written and verified using python programming.
