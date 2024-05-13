# Implementation of Univariate Linear Regression
## Aim:
To implement univariate Linear Regression to fit a straight line using least squares.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
1.	Get the independent variable X and dependent variable Y.
2.	Calculate the mean of the X -values and the mean of the Y -values.
3.	Find the slope m of the line of best fit using the formula.
 ![eqn1](./eq1.jpg)
4.	Compute the y -intercept of the line by using the formula:
![eqn2](./eq2.jpg)  
5.	Use the slope m and the y -intercept to form the equation of the line.
6.	Obtain the straight line equation Y=mX+b and plot the scatterplot.
## Program
#Program to implement univariate Linear Regression to fit a straight line using least squares.

#Developed by: BAUDHIGAN D

#register number: 212223230028
```
import numpy as np 
import matplotlib.pyplot as plt
x = np.array([0,1,2,3,4,5,6,7,8,9])
y = np.array([1,3,2,5,7,8,8,9,10,12])
plt.scatter(x,y)
plt.show()
xmean = np.mean(x)
ymean = np.mean(y)
num=0
den=0
for i in range(len(x)):
    num+=(x[i]-xmean)*(y[i]-ymean)
    den+=(x[i]-xmean)**2
m = num/den
b = ymean - m*xmean
print(m,b)
ypred = m*x+b
print(ypred)


plt.scatter(x,y,color='Red')
plt.plot(x,ypred,color='Blue')
plt.show()

```
## Output
![Screenshot 2024-05-13 065339](https://github.com/baudhigan/Univariate-Linear-Regression/assets/151921158/c9cb5e35-3d7b-4064-bcb1-484938a698da)
![Screenshot 2024-05-13 065355](https://github.com/baudhigan/Univariate-Linear-Regression/assets/151921158/e6ddf367-12cb-4ab0-abe8-f5c762fe3a10)
![Screenshot 2024-05-13 065421](https://github.com/baudhigan/Univariate-Linear-Regression/assets/151921158/27c7ea70-b4ca-4bf3-97c3-4378d7b4f481)

## Result
Thus the univariate Linear Regression was implemented to fit a straight line using least squares.
