# EX2 Implementation of Simple Linear Regression Model for Predicting the Marks Scored
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
Developed by: 
RegisterNumber:  
*/
df=pd.read_csv('/content/ex1.csv')
df.head(10)

plt.scatter(df['X'],df['Y'])
plt.xlabel('X')
plt.ylabel('Y')

x=df.iloc[:,:-1]
y=df.iloc[:,-1]

learn.model_selection import trainfrom sk_test_split
X_train,X_test,Y_train,Y_test=train_test_split(x,y,test_size=0.2,random_state=0)

from sklearn.linear_model import LinearRegression


lr=LinearRegression()
lr.fit(X_train,Y_train)

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
mse
```

## Output:
![Screenshot 2024-10-03 135532](https://github.com/user-attachments/assets/64b9b4ab-434b-46f2-ae51-23df6dd33a77)
![Screenshot 2024-10-03 135629](https://github.com/user-attachments/assets/0a02164e-1bb3-4a20-920e-1ae114b04eef)
![Screenshot 2024-10-03 135955](https://github.com/user-attachments/assets/c49aec37-5e14-404c-9e01-90be39bf202e)
![Screenshot 2024-10-03 140108](https://github.com/user-attachments/assets/3cc57195-3f9e-4218-8e9d-7af02fe1b36b)
![Screenshot 2024-10-03 140211](https://github.com/user-attachments/assets/fe7f86b5-9978-4bad-8939-1982d31e1c29)
![Screenshot 2024-10-03 140245](https://github.com/user-attachments/assets/2d8172b1-fdf6-4926-9941-a6d09dc6ea8f)
![Screenshot 2024-10-03 140410](https://github.com/user-attachments/assets/40c639bf-981a-45ba-bda0-7ff21d391fc7)
![Screenshot 2024-10-03 140425](https://github.com/user-attachments/assets/361fc4db-23fc-4ab5-8d50-48055fba5ad6)
![Screenshot 2024-10-03 140434](https://github.com/user-attachments/assets/f392223d-a7d5-4a11-b1f3-75e0b25facab)



## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
