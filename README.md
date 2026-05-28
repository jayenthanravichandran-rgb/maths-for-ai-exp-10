# Implementation of Multivariate Linear Regression
## Aim
To write a python program to implement multivariate linear regression and predict the output.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
Import libraries and load dataset
Import pandas and LinearRegression, then read the CSV file using pd.read_csv().
Select input and output variables
Store Volume and Weight in X and CO2 in y.
Create and train the model
Initialize LinearRegression() and train it using fit(X, y).
Predict CO₂ emission
Give new input values (3300, 1300) and use predict() to display the predicted CO₂ value.
## Program:
#exp-10(maths for ai)
import pandas as pd
from sklearn import linear_model


df = pd.read_csv("car (1).csv")


X = df[["Volume", "Weight"]]
y = df["CO2"]

regression = linear_model.LinearRegression()
regression.fit(X, y)


print("Coefficients (Volume, Weight):", regression.coef_)
print("Intercept:", regression.intercept_)

new_data = pd.DataFrame([[3300, 1300]], columns=["Volume", "Weight"])


prediction = regression.predict(new_data)

print("Predicted CO2:", prediction[0])
## Output:
<img width="1912" height="1013" alt="Screenshot 2026-05-28 102525" src="https://github.com/user-attachments/assets/7ef0cb87-b212-4bfa-bbee-143a5ea5b4c8" />


## Result
Thus the multivariate linear regression is implemented and predicted the output using python program.
