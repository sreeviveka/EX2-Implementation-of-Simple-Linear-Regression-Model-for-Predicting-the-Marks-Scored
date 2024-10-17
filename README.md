# EX2 Implementation of Simple Linear Regression Model for Predicting the Marks Scored
## DATE:
## AIM:
To implement simple linear regression using sklearn.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Get the independent variable X and dependent variable Y by reading the dataset.
2. Split the data into training and test data.
3. Import the linear regression and fit the model with the training data.
4. Perform the prediction on the test data.
5. Display the slop and intercept values.
6. Plot the regression line using scatterplot.
7. Calculate the MSE.

## Program:
```
/*
Program to implement univariate Linear Regression to fit a straight line using least squares.
Developed by: Sreeviveka V.S
RegisterNumber:  2305001031
*/
 import pandas as pd
 import numpy as np
 import matplotlib.pyplot as plt
 df=pd.read_csv('/content/ex1.csv')
 df.head()
 plt.scatter(df['X'],df['Y'])
 plt.xlabel('X')
 plt.ylabel('Y')
 x=df.iloc[:,0:1]
 y=df.iloc[:,-1]
 x
 from sklearn.model_selection import train_test_split
 X_train,X_test,Y_train,Y_test=train_test_split(x,y,test_size=0.2,random_state=0)
 from sklearn.linear_model import LinearRegression
lr=LinearRegression()
 lr.fit(X_train,Y_train)
 X_train
 Y_train
 plt.scatter(df['X'],df['Y'])
 plt.xlabel('X')
 plt.ylabel('Y')
 plt.plot(X_train,lr.predict(X_train),color='red')
 m=lr.coef_
 m
 b=lr.intercept_
 b
 pred=lr.predict(X_test)
 pred
 X_test
 Y_test
 from sklearn.metrics import mean_squared_error
 mse=mean_squared_error(Y_test,pred)
 print(f"Mean Squared Error (MSE): {mse}")
```

## Output:
![Screenshot 2024-10-03 135532](https://github.com/user-attachments/assets/ac92ed53-a92a-46e5-935f-85a6cefbc77f)
![Screenshot 2024-10-03 135629](https://github.com/user-attachments/assets/6611f171-3c0e-442c-afab-5f55630d6fe5)
![Screenshot 2024-10-03 135955](https://github.com/user-attachments/assets/86ebfe9b-c905-48ac-973c-585fce9855a0)
![Screenshot 2024-10-03 140108](https://github.com/user-attachments/assets/ddb2f79d-0d71-4c0f-bfc8-fee6b6ffd8c6)
![Screenshot 2024-10-03 140211](https://github.com/user-attachments/assets/87166a57-5227-4c6e-98d5-525fc82618ac)
![Screenshot 2024-10-03 140245](https://github.com/user-attachments/assets/c6a50abd-c62d-4b58-887d-daab9c927d46)
![Screenshot 2024-10-03 140410](https://github.com/user-attachments/assets/5aa21fd9-7c04-4829-8229-86afb8f8e4dd)
![Screenshot 2024-10-03 140425](https://github.com/user-attachments/assets/25128c9a-0eb2-4348-821c-58b0547f9abb)
![Screenshot 2024-10-03 140434](https://github.com/user-attachments/assets/4b30b1a1-6b93-49cc-9cdd-c95653d39985)




## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
