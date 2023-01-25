# Implementation of Multivariate Linear Regression
## Aim
To write a python program to implement multivariate linear regression and predict the output.

## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm:
Step1: 
Import pandas as pd

Step2:
Read the csv file.

Step3:
Get the value of X and y variables

Step4:
Create the linear regression model and fit

Step5:
Predict the CO2 emission of a car where the weight is 1000kg, and the volume is 1390cm3

## Program:
```
#Program to Implementation of Multivariate Linear Regression
#Developed by: Archana.k
#Register number: 22009150
import pandas as pd
from sklearn import linear_model
df = pd.read_csv("cars.csv")
X = df[['Weight', 'Volume']]
y = df['CO2']
regr = linear_model.LinearRegression()
regr.fit(X, y)
print('Coefficients:', regr.coef_)
print('Intercept:',regr.intercept_)
predictedCO2 = regr.predict([[1000, 1390]])
print('Predicted CO2 for the corresponding weight and volume',predictedCO2)
```
## Output:
![Screenshot 2023-01-25 205022](https://user-images.githubusercontent.com/118708624/214602427-0b7bd314-4d3b-480f-8a13-70c8e25ae2d3.png)
![Screenshot 2023-01-25 205247](https://user-images.githubusercontent.com/118708624/214603005-5836001e-be80-4ba2-9f5b-d45193c4a272.png)

## Result
Thus the multivariate linear regression is implemented and predicted the output using python program.
