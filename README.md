# Implementation of Multivariate Linear Regression
## Aim
To write a python program to implement multivariate linear regression and predict the output.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
Step1

import pandas as pd.

Step2

Read the csv file.

Step3

Get the value of X and y variables

Step4

Create the linear regression model and fit.

Step5

Predict the CO2 emission of a car where the weight is 2300kg, and the volume is 1300cm cube.

## Program:
```
# Developed by : JAYAPRADAN M
# Reg No : 21224240061
import pandas as pd
from sklearn import linear_model

# Use the correct path and filename
try:
    df = pd.read_csv("/content/car (1).csv")
    X = df[['Weight', 'Volume']]
    y = df['CO2']

    regr = linear_model.LinearRegression()
    regr.fit(X, y)
    print('Coefficients:', regr.coef_)
    print('Intercept:', regr.intercept_)

    predictedCO2 = regr.predict(pd.DataFrame([[3300, 1300]], columns=['Weight', 'Volume']))
    print('Predicted CO2 for the corresponding weight and volume:', predictedCO2)

except FileNotFoundError:
    print("Error: The file '/content/car (1).csv' was not found. Please ensure the file exists at this path.")
except KeyError as e:
    print(f"Error: Column not found: {e}. Please check that 'Weight', 'Volume', and 'CO2' columns exist in your CSV file.")
except Exception as e:
    print(f"An unexpected error occurred: {e}")





```
## Output:
<img width="1134" height="626" alt="image" src="https://github.com/user-attachments/assets/d61316f2-e31f-4ffb-af42-0584a552d55f" />


## Result
Thus the multivariate linear regression is implemented and predicted the output using python program.
