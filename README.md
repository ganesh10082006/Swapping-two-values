# Swapping-two-values
## AIM:
To write a python program for swapping of two values
## EQUIPEMENT'S REQUIRED: 
PC
Anaconda - Python 3.7
## ALGORITHM: 
### Step 1:
Get the two values from the user
### Step 2: 
Assign the value of second variable to a temporary variable 
### Step 3: 
Assign the value of the first variable to the second variable.
### Step 4:  
Assign the value in temporary variable to the first variable
### Step 5: 
Print both the values it would be interchanged
### Step 6: 
End the program
## PROGRAM:
~~~
1.  Newton raphson

def f(x):
    return x**3 - x - 2

def f1(x):
    return 3 * x**2 - 1

xo = float(input("Enter the initial approximation: "))

for i in range(1, 10):
    xn = xo - f(xo) / f1(xo)
    xo = xn  # Update `xo` correctly here

print("The approximate root using Newton-Raphson method is %.4f" % xn)


2.  Gauss sendal method
x0 = 0
y0 = 0
z0 = 0

for i in range(1, 10):
    x = 1/4 * (1 - y0 - z0)
    x0 = x 
    
    y = 1/3 * (2 - x0 - z0)
    y0 = y  
    
    z = 1/5 * (3 - x0 - y0)
    z0 = z 

print(f"The approximate solution is x={x:.4f}, y={y:.4f}, z={z:.4f}")

3.  Lagrange

x = [0, 1, 2, 4, 5, 6]
y = [1, 14, 15, 5, 6, 19]

s = float(input("Enter the value of x to evaluate: "))

sum = 0
for i in range(6):
    prod = 1
    for j in range(6):
        if i != j:
            prod *= (s - x[j]) / (x[i] - x[j])
    sum += prod * y[i]

print("The functional value is %.4f" % sum)

4. Trapezoidal rule:

def f(x):
    return 1 / (1 + x**2)

a = float(input("Enter the lower limit: "))
b = float(input("Enter the upper limit: "))
h = float(input("Enter the step size: "))

n = int((b - a) / h)

sum = 0
for i in range(1, n):
    sum += f(a + i * h)

trap = h / 2 * (f(a) + f(b) + 2 * sum)

print("The Integral value is %.5f" % trap)

5. Runge kutta method
def f(x, y):
    return x + y**2

x0 = float(input("Enter the initial point of x: "))
y0 = float(input("Enter the initial point of y: "))
h = float(input("Enter the step value h: "))

k1 = h * f(x0, y0)
k2 = h * f(x0 + h / 2, y0 + k1 / 2)
k3 = h * f(x0 + h / 2, y0 + k2 / 2)
k4 = h * f(x0 + h, y0 + k3)

y = y0 + (k1 + 2 * k2 + 2 * k3 + k4) / 6

print("The value of y using RK method is %.4f" % y)

6.  Adams Predictor 

def f(x, y):
    return x**2 * (1 + y)

x0 = float(input("Enter x0: "))
y0 = float(input("Enter y0: "))
x1 = float(input("Enter x1: "))
y1 = float(input("Enter y1: "))
x2 = float(input("Enter x2: "))
y2 = float(input("Enter y2: "))
x3 = float(input("Enter x3: "))
y3 = float(input("Enter y3: "))

h = 0.1  # Step size

# Predictor formula
y4p = y3 + (h / 24) * (55 * f(x3, y3) - 59 * f(x2, y2) + 37 * f(x1, y1) - 9 * f(x0, y0))

# Compute x4
x4 = x3 + h

# Corrector formula
y4c = y3 + (h / 24) * (9 * f(x4, y4p) + 19 * f(x3, y3) - 5 * f(x2, y2) + f(x1, y1))

print("Approximate solution is %.4f" % y4c)









~~~

## OUTPUT:
![image](https://github.com/ganesh10082006/Swapping-two-values/assets/151981672/313a03ef-373e-4703-99ec-c9e56edf24ba)


## RESULT:
Thus the swapping of two values are successfully executed
