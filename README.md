# Implementation of Multivariate Linear Regression
## Aim
To write a python program to implement multivariate linear regression and predict the output.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
### Step1
Start and import the required libraries — pandas for data handling and linear_model from sklearn for regression.

### Step2
Load the dataset from the CSV file using pd.read_csv() and store it in a DataFrame df.

### Step3
Select features and target: Set X = [['Weight', 'Volume']] (independent variables). Set y = ['CO2'] (dependent variable).

### Step4
Create a Linear Regression model using linear_model.LinearRegression() and store it in regr.

### Step5
Train the model using regr.fit(X, y) and display the model’s coefficients and intercept.

## Program:
```
# Developed By: G.MUTHU MANIKKAM
# Register Number:25016274

import pandas as pd
from sklearn import linear_model
df = pd.read_csv(r'C:\Users\Junaid Sardar\Downloads\car (1).csv')
X = df[['Weight', 'Volume']]
y = df['CO2']
regr = linear_model.LinearRegression()
regr.fit(X, y)
print('Coefficients:', regr.coef_)
print('Intercept:', regr.intercept_)
predictedCO2 = regr.predict(pd.DataFrame([[3300, 1300]], columns=['Weight', 'Volume']))
print('Predicted CO2 for the corresponding weight and volume:',predictedCO2)

```
## Output:
<img width="1012" height="492" alt="Screenshot 2026-01-06 221842" src="https://github.com/user-attachments/assets/b0d1c233-9693-4161-b42f-6ff2a34370c9" />

## Result
Thus the multivariate linear regression is implemented and predicted the output using python program.
