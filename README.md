# Implementation of Univariate Linear Regression
## AIM:
To implement univariate Linear Regression to fit a straight line using least squares.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Get the independent variable X and dependent variable Y.
2. Calculate the mean of the X -values and the mean of the Y -values.
3. Find the slope m of the line of best fit using the formula. 
<img width="231" alt="image" src="https://user-images.githubusercontent.com/93026020/192078527-b3b5ee3e-992f-46c4-865b-3b7ce4ac54ad.png">
4. Compute the y -intercept of the line by using the formula:
<img width="148" alt="image" src="https://user-images.githubusercontent.com/93026020/192078545-79d70b90-7e9d-4b85-9f8b-9d7548a4c5a4.png">
5. Use the slope m and the y -intercept to form the equation of the line.
6. Obtain the straight line equation Y=mX+b and plot the scatterplot.

## Program:
```
Program to implement univariate Linear Regression to fit a straight line using least squares.
Developed by: SHRIRAM S
RegisterNumber:  212222240098
```
```
#univariant linear regission
import numpy as np
import matplotlib.pyplot as plt
x=np.array(eval(input("Enter a x value:")))
y=np.array(eval(input("enter a y value:")))
x1=np.mean(x)
y1=np.mean(y)
num=0
den=0
#formula=sumation(xi-xmean)(yi-ymean)/sumation(xi-xmean)**2
for i in range(len(x)):
  num=num+(x[i]-(x1))*(y[i]-y1)
  den=den+(x[i]-x1)**2
m=num/den
print(m)
#b=y`-mx`
b=y1-m*x1
print(b)
y_pred=m*x+b
import seaborn as sns
plt.scatter(x,y)
plt.plot(x,y_pred,color='red')
plt.show()
```

## Output:
![best fit line](sam.png)


## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
