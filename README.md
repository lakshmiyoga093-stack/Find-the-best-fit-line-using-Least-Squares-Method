# Implementation of Univariate Linear Regression
# AIM:
To implement univariate Linear Regression to fit a straight line using least squares.

# Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

# Algorithm
1. Get the independent variable X and dependent variable Y.
2. Calculate the mean of the X -values and the mean of the Y -values.
3. Find the slope m of the line of best fit using the formula. 
<img width="231" alt="image" src="https://user-images.githubusercontent.com/93026020/192078527-b3b5ee3e-992f-46c4-865b-3b7ce4ac54ad.png">
4. Compute the y -intercept of the line by using the formula:
<img width="148" alt="image" src="https://user-images.githubusercontent.com/93026020/192078545-79d70b90-7e9d-4b85-9f8b-9d7548a4c5a4.png">
5. Use the slope m and the y -intercept to form the equation of the line.
6. Obtain the straight line equation Y=mX+b and plot the scatterplot.

# Program:
```
import numpy as np
import matplotlib.pyplot as plt
```
## Step 1: Input data
```
X = np.array([1, 2, 3, 4, 5])
Y = np.array([2, 4, 5, 4, 5])
```
## Step 2: Calculate mean
```
x_mean = np.mean(X)
y_mean = np.mean(Y)
```
## Step 3: Calculate numerator and denominator
```
num = 0
denom = 0

for i in range(len(X)):
    num += (X[i] - x_mean) * (Y[i] - y_mean)
    denom += (X[i] - x_mean) ** 2
```
## Step 4: Calculate slope and intercept
```
m = num / denom
b = y_mean - m * x_mean
```
## Step 5: Predict Y values
```
Y_predicted = m * X + b
```
## Step 6: Display results
```
print("Slope:", m)
print("Intercept:", b)
print("Predicted Y values:", Y_predicted)
```
## Step 7: Plot the results
```
plt.scatter(X, Y, label="Actual Data")
plt.plot(X, Y_predicted, color="red", label="Regression Line")

plt.xlabel("X values")
plt.ylabel("Y values")
plt.title("Univariate Linear Regression")
plt.legend()
plt.show()
```

# Output:
<img width="1045" height="647" alt="image" src="https://github.com/user-attachments/assets/877bde56-fb76-4698-ba41-dab4cae09a00" />



# Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
