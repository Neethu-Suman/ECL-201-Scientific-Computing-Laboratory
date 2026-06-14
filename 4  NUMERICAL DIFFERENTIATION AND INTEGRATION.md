**EXP NO: 4**	

**NUMERICAL DIFFERENTIATION AND INTEGRATION**

**OBJECTIVE**

●	To perform numerical differentiation and integration

**LEARNING OUTCOMES**

After the completion of this experiment students will be able to Implement numerical integration and differentiation.

**SOFTWARE USED:** 

SPIDER

**THEORY**

The first derivative of the function f(x), which we write as df /dx , is the slope of the tangent line to the function at the point x. To put this in non-graphical terms, the first derivative tells us how whether a function is increasing or decreasing, and by how much it is increasing or decreasing .

The second derivative of a function is the derivative of the derivative of that function. We write it as  d2 f /dx2 . While the first derivative can tell us if the function is increasing or decreasing, the second derivative tells us if the first derivative is increasing or decreasing. If the second derivative is positive, then the first derivative is increasing, so that the slope of the tangent line to the function is increasing as x increases

sin – Sine of argument in radians

cos - cos of argument in radians


**Trapezoidal Method**

Trapezoidal Rule is a rule that evaluates the area under the curves by dividing the total area into smaller trapezoids rather than using rectangles. This integration works by approximating the region under the graph of a function as a trapezoid, and it calculates the area.
 
Let f(x) be a continuous function on the interval [a, b]. Now divide the intervals [a, b] into n equal subintervals with each of width,

Δx = (b-a)/n, Such that a = x0 < x1< x2< x3<…..<xn = b

Then the Trapezoidal Rule formula for area approximating the definite integral ∫ab f(x)dx is given by:
  
Where, xi = a+iΔx

If n →∞, R.H.S of the expression approaches the definite integral ∫ab f(x)dx.

simpsons rule

Formula:  (h/3)*[(y0+yn)+2*(y3+y5+..odd term)+4*(y2+y4+y6+...even terms)]

h= (b-a)/n

b is upper limit, a is lower limit and n is number of sub intervals. y0 and yn are first and last term.
 
1. Realize the functions sin t, cos t, sinht and cosht for the vector t = [-0, 10] with increment 0:01

import numpy as np

import matplotlib.pyplot as plt

#Define the vector t

t = np.arange(0, 10, 0.01)

#Calculate the functions sin t, cos t, sinh t, and cosh t

sin_t = np.sin(t)

cos_t = np.cos(t)

sinh_t = np.sinh(t)

cosh_t = np.cosh(t)

#Create a subplot with four plots

plt.subplot(2, 2, 1)

plt.plot(t, sin_t)

plt.xlabel('t')

plt.ylabel('sin(t)')

plt.subplot(2, 2, 2)

plt.plot(t, cos_t)

plt.xlabel('t')

plt.ylabel('cos(t)')

plt.subplot(2, 2, 3)

plt.plot(t, sinh_t)

plt.xlabel('t')

plt.ylabel('sinh(t)')

plt.subplot(2, 2, 4)

plt.plot(t, cosh_t)

plt.xlabel('t')

plt.ylabel('cosh(t)')

#Show the plot

plt.show()

**OUTPUT**
 
2.   Compute the first and second derivatives of these functions using built in tools such as grad  

**PROGRAM**

import numpy as np

import matplotlib.pyplot as plt

#Define the vector t

t = np.arange(0, 10, 0.01)

#Calculate the functions sin t, cos t, sinh t, and cosh t

sin_t = np.sin(t)

cos_t = np.cos(t)

sinh_t = np.sinh(t)

cosh_t = np.cosh(t)

#Calculate the first and second derivatives of the functions

d_sin_t = np.gradient(sin_t, t)

d2_sin_t = np.gradient(d_sin_t, t)

d_cos_t = np.gradient(cos_t, t)

d2_cos_t = np.gradient(d_cos_t, t)

d_sinh_t = np.gradient(sinh_t, t)

d2_sinh_t = np.gradient(d_sinh_t, t)

d_cosh_t = np.gradient(cosh_t, t)

d2_cosh_t = np.gradient(d_cosh_t, t)

#Create a subplot with 12 plots

plt.figure(figsize=(20, 30))

#Plot the functions

plt.subplot(3, 4, 1)

plt.plot(t, sin_t)

plt.xlabel('t')

plt.ylabel('sin(t)')

plt.subplot(3, 4, 2)

plt.plot(t, cos_t)

plt.xlabel('t')

plt.ylabel('cos(t)')

plt.subplot(3, 4, 3)

plt.plot(t, sinh_t)

plt.xlabel('t')

plt.ylabel('sinh(t)')

plt.subplot(3, 4, 4)

plt.plot(t, cosh_t)

plt.xlabel('t')

plt.ylabel('cosh(t)')

#Plot the first derivatives

plt.subplot(3, 4, 5)

plt.plot(t, d_sin_t)

plt.xlabel('t')

plt.ylabel('d/dt sin(t)')

plt.subplot(3, 4, 6)

plt.plot(t, d_cos_t)

plt.xlabel('t')

plt.ylabel('d/dt cos(t)')

plt.subplot(3, 4, 7)

plt.plot(t, d_sinh_t)

plt.xlabel('t')

plt.ylabel('d/dt sinh(t)')

plt.subplot(3, 4, 8)

plt.plot(t, d_cosh_t)

plt.xlabel('t')

plt.ylabel('d/dt cosh(t)')

#Plot the second derivatives

plt.subplot(3, 4, 9)

plt.plot(t, d2_sin_t)

plt.xlabel('t')

plt.ylabel('d2/dt2 sin(t)')

plt.subplot(3, 4, 10)

plt.plot(t, d2_cos_t)

plt.xlabel('t')

plt.ylabel('d2/dt2 cos(t)')

plt.subplot(3, 4, 11)

plt.plot(t, d2_sinh_t)

plt.xlabel('t')

plt.ylabel('d2/dt2 sinh(t)')

plt.subplot(3, 4, 12)

plt.plot(t, d2_cosh_t)

plt.xlabel('t')

plt.ylabel('d2/dt2 cosh(t)')

#Show the plot

plt.show()

**OUTPUT**
 
3. Realize the function f(t) = 4t2 + 3 and plot it for the vector t = [5; 5] with increment 0:01

import numpy as np

import matplotlib.pyplot as plt

#Define the vector t

t = np.arange(5, 10, 0.01)

#Calculate the function f(t)

f_t = 4 * t**2 + 3

#Plot the function f(t)

plt.plot(t, f_t)

plt.xlabel('t')

plt.ylabel('f(t)')

plt.title('Plot of f(t) = 4t^2 + 3')

plt.show()

**OUTPUT**

4. 
 
import numpy as np

from scipy import integrate

#Define the function f(t)

def f(t):

return 4 * t**2 + 3

#Define the integration limits

lower_limit = -2

upper_limit = 2

#Compute the integral of f(t) in the interval [-2, 2]

integral, error = integrate.quad(f, lower_limit, upper_limit)

#Print the integral

print("Integral of f(t) in the interval [-2, 2]:", integral)

**OUTPUT**

The integral of f(t) in the interval [-2, 2] is: 33.333333333333336

5. Repeat the above steps with trapezoidal and Simpson method and compare the results.

**PROGRAM**

import numpy as np

import scipy.integrate as integrate

#Define the function f(t)

def f(t):

return 4 * t**2 + 3

#Define the trapezoidal method

def trapezoidal_method(f, a, b, n):

x = np.linspace(a, b, n+1)
    
y = f(x)
    
h = (b - a) / n
    
integral = (h/2) * (y[0] + 2*np.sum(y[1:n]) + y[n])
    
return integral

#Define Simpson's method

def simpsons_method(f, a, b, n):

if n % 2:
    
raise ValueError("n must be an even number.")
    
x = np.linspace(a, b, n+1)
    
y = f(x)
    
h = (b - a) / n
    
integral = (h/3) * (y[0] + 4*np.sum(y[1:n:2]) + 2*np.sum(y[2:n-1:2]) + y[n])
    
return integral

#Set the interval and number of subintervals

a, b = -2, 2

n = 100  # Number of subintervals

#Calculate the integrals

trap_result = trapezoidal_method(f, a, b, n)

simp_result = simpsons_method(f, a, b, n)

#Compare the results

print("Integration using Trapezoidal method:", trap_result)

print("Integration using Simpson's method:", simp_result)

#For comparison, let's also use scipy's quad function for numerical integration

exact_integral, _ = integrate.quad(f, a, b)

print("Exact integral using scipy's quad:", exact_integral)

**OUTPUT**

Integration using Trapezoidal method: 33.3376

Integration using Simpson's method: 33.33333333333334

Exact integral using scipy's quad: 33.333333333333336

6.  

**PROGRAM**

import numpy as np

from scipy import integrate

#Define the function to integrate

def f(x):

return np.exp(-x**2/2)

#Define the interval of integration

a = 0

b = np.inf

#Trapezoidal method

def trapezoidal_method(f, a, b, n):

x = np.linspace(a, b, n+1)

y = f(x)

h = (b - a) / n

integral = (h/2) * (y[0] + 2*np.sum(y[1:n]) + y[n])

return integral

#Simpson's method

def simpsons_method(f, a, b, n):

if n % 2:

raise ValueError("n must be an even number.")

x = np.linspace(a, b, n+1)

y = f(x)

h = (b - a) / n

integral = (h/3) * (y[0] + 4*np.sum(y[1:n:2]) + 2*np.sum(y[2:n-1:2]) + y[n])

return integral

#Set the number of subintervals

n = 100

#Calculate the integrals

trap_result = trapezoidal_method(f, a, b, n)

simp_result = simpsons_method(f, a, b, n)

#Compare the results

print("Integration using Trapezoidal method:", trap_result)

print("Integration using Simpson's method:", simp_result)

#For comparison, let's also use scipy's quad function for numerical integration
exact_integral, _ = integrate.quad(f, a, b)
print("Exact integral using scipy's quad:", exact_integral)
# Compute 1/sqrt(2 pi) of integral of exp(-x^2/2) using above three methods
print("1/sqrt(2 pi) of integral of exp(-x^2/2) using Trapezoidal method:", trap_result / np.sqrt(2 * np.pi))
print("1/sqrt(2 pi) of integral of exp(-x^2/2) using Simpson's method:", simp_result / np.sqrt(2 * np.pi))
print("1/sqrt(2 pi) of integral of exp(-x^2/2) using scipy's quad:", exact_integral / np.sqrt(2 * np.pi))


OUTPUT
Integration using Trapezoidal method: nan
Integration using Simpson's method: nan
Exact integral using scipy's quad: 1.2533141373154997
1/sqrt(2 pi) of integral of exp(-x^2/2) using Trapezoidal method: nan
1/sqrt(2 pi) of integral of exp(-x^2/2) using Simpson's method: nan
1/sqrt(2 pi) of integral of exp(-x^2/2) using scipy's quad: 0.49999999999999983

INFERENCE:
Visualized the basic functions such as sin t, cos t, sinht and cosht and performed numerical differentiation and integration using different methods
