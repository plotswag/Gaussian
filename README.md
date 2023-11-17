# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm 


## Program:
```
Program to solve a matrix using Gaussian elimination without partial pivoting.
Developed by:jeevanesh 
RegisterNumber:23013802

import numpy as np
import sys
n = int(input())
a = np.zeros((n,n+1))
X = np.zeros(n)
for i in range (n):
    for j in range (n+1):
        a[i][j] = float(input())
for i in range(n):
    if a[i][i] == 0.0:
        sys.exit('divide by zero detected')
    for j in range(i+1,n):
        ratio = a[j][i]/a[i][i]
        for k in range(n+1):
            a[j][k] = a[j][k] - ratio * a[i][k]
X[n-1] = a[n-1][n]/a[n-1][n-1]
for i in range(n-2,-1,-1):
    X[i] = a[i][n]
    for j in range(i+1,n):
        X[i] = X[i]-a[i][j]*X[j]
    X[i] = X[i]/a[i][i]
for i in range(n):
    print('X%d = %00.2f' %(i,X[i]), end=' ')            
```
## Output:
![image](https://github.com/plotswag/Gaussian/assets/145822344/b1a813a0-f541-4c92-9041-7abe62846d6f)
## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

