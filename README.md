# Implementation of Multivariate Linear Regression
## Aim
To write a python program to implement multivariate linear regression and predict the output.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm:

### Step1: Import pandas for data manipulation and linear_model from sklearn for regression.


### Step2: Load the CSV file carsemission.csv into a dataframe using pd.read_csv


### Step3: Define X as a dataframe containing the weight and volume columns. Define y as the CO2 column which is the value to predict.


### Step4: Create a linear regression model instance using linear_model.LinearRegression(). Train the model with the data by calling regr.fit(X,y)


### Step5: Access model coefficients with regr.coef_,showing the weight of each feature. Access the intercept term with regr.intercept_,representing the baseline CO2

### Step6: Create a dataframe input_data with new values for weight and volume. Use the regr.predict(input_data) to predict CO2 for the input features.

### Step7: End the program.


## Program:
''' 
Program to QR decomposition using the Gram-Schmidt method
Developed by: JAYANI N
RegisterNumber: 24900024
'''

    import pandas as pd
    from sklearn import linear_model
    df = pd.read_csv("carsemission.csv")
    X = df[['Weight', 'Volume']]
    y = df['CO2']
    regr = linear_model.LinearRegression()
    regr.fit(X, y)
    print('Coefficients:', regr.coef_)
    print('Intercept:',regr.intercept_)
    predictedCO2 = regr.predict([[3300, 1300]])
    print('Predicted CO2 for the corresponding weight and volume',predictedCO2)

## Output:

![alt text](image.png)

## Result
Thus the multivariate linear regression is implemented and predicted the output using python program.