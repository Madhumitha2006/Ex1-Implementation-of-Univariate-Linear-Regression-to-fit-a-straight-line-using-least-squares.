# EX1 Implementation of Univariate Linear Regression to fit a straight line using Least Squares
## DATE:
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
Developed by: Madhu Mitha V 
RegisterNumber:  2305002013
import numpy as np
import matplotlib.pyplot as plt
x=np.array([2,9,5,5,3,7,1,8,6,2])
y=np.array([69,98,82,77,71,84,55,94,84,64])
xmean=np.mean(x)
ymean=np.mean(y)
num,den=0,0
for i in range(len(x)):
  num+=(x[i]-xmean)*(y[i]-ymean)
  den+=(x[i]-xmean)**2
m=num/den
c=ymean-m*xmean
print(m,c)
y_pred=m*x+c
plt.scatter(x,y)
plt.plot(x,y_pred,color="blue")
plt.show()
```

## Output:

![image](https://github.com/user-attachments/assets/e256416f-9293-4f28-b89e-86b5593b2d5d)


## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
