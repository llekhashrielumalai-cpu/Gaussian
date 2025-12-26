# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
step1: Import the numpy module to use the built-in functions for calculation

Step 2: Prepare the lists from each linear equations and assign in np.array()

Step 3: Using the np.linalg.solve(), we can find the solutions.

Step 4: End the program

## Program:
```
 import numpy as np
from decimal import Decimal,ROUND_HALF_UP
n=int(input())
a=np.zeros((n,n+1))
x=np.zeros(n)
for i in range(n):
    for j in range(n+1):
        a[i][j]=float(input())
for i in range(n):
    if a[i][i]==0.0:
        sys.exit("divide by zero detected!")
    for j in range(i+1,n):
        ratio=a[j][i]/a[i][i]
        for k in range(n+1):
            a[j][k]=a[j][k]-ratio*a[i][k]
x[n-1]=a[n-1][n]/a[n-1][n-1]
for i in range(n-2,-1,-1):
    x[i]=a[i][n]
    for j in range(i+1,n):
        x[i]=x[i]-a[i][j]*x[j]
    x[i]=x[i]/a[i][i]
for i in range (n):
    print('X%d = %0.2f'%(i,x[i]), end=' ')
```

## Output:
<img width="1920" height="1080" alt="Screenshot (107)" src="https://github.com/user-attachments/assets/9d305e1b-07cc-4c3b-bcf3-a4a75bf58320" />
<img width="1920" height="1080" alt="Screenshot (108)" src="https://github.com/user-attachments/assets/94ee9801-d569-4682-a85f-39bc74b2140e" />



## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

