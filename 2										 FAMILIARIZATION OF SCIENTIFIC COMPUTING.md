**EXP NO: 2**

**FAMILIARIZATION OF SCIENTIFIC COMPUTING**

**OBJECTIVE**

●	To familiarize different functions for scientific computing with examples

**LEARNING OUTCOMES**

●	After the completion of this experiment students will be able to execute small scripts using different arithmetic functions

**SOFTWARE USED:** 

spyder

1. Type the following in the command window, write down the results and the functions of these built in modules

**Basic Arithmetic Operators**

a = 5 + 3        # Addition: 
        
        8

b = 5 - 3        # Subtraction: 

        2

c = 5 * 3        # Multiplication: 

        15

d = 5 / 3        # Division: 
        
        1.6666666666666667

e = 5 // 3       # Floor Division: 

        1

f = 5 % 3        # Modulus: 
        
        2

g = 5 ** 3       # Exponentiation: 

        125

**Built-in Arithmetic Functions**

h = abs(-5)          # Absolute Value: 

        5

i = pow(5, 3)        # Power: 

        125

j = max(5, 3, 9)     # Maximum: 
        
        9

k = min(5, 3, 9)     # Minimum: 

        3

l = sum([5, 3, 9])   # Sum: 

        17
m = round(5.678, 2)  # Round: 

        5.682.  

#Using the math module

import math

n = math.sqrt(16)        # Square Root: 
        
        4.0

o = math.ceil(5.3)       # Ceiling: 

        6

p = math.floor(5.7)      # Floor: 

        5

#Trigonometric Functions

q = math.sin(math.pi / 2)  # Sine: 

        1.0

r = math.cos(0)            # Cosine: 

        1.0

s = math.tan(math.pi / 4)  # Tangent: 

        1.0

#Logarithmic Functions

t = math.log(10)          # Natural log (base e): 

        2.302585092994046

u = math.log10(100)       # Logarithm base 10: 

        2.0

v = math.log2(8)          # Logarithm base 2: 

        3.0

#Constants

pi = math.pi  # Pi: 

        3.141592653589793

e = math.e    # Euler's Number: 

        2.718281828459045

2. Basic arithmetic functions such as abs, sine, real, imag, complex, sinc etc. using bulit in modules.

#Importing the math and cmath modules

import math

import cmath

import numpy as np

#Absolute Value

a = abs(-5)  # 5

print(f"Absolute Value (abs(-5)): {a}")

#Sine (math module)

b = math.sin(math.pi / 2)  # 1.0

print(f"Sine (math.sin(math.pi / 2)): {b}")

#Real and Imaginary Parts of a Complex Number

c = complex(3, 4)  # 3 + 4j

real_part = c.real  # 3.0

imag_part = c.imag  # 4.0

print(f"Complex Number: {c}")

print(f"Real Part (c.real): {real_part}")

print(f"Imaginary Part (c.imag): {imag_part}")

#Creating Complex Numbers

d = complex(5, -7)  # 5 - 7j

print(f"Complex (complex(5, -7)): {d}")

#Sinc Function (Normalized Sinc using the math module)

def sinc(x):

return math.sin(math.pi * x) / (math.pi * x) if x != 0 else 1

e = sinc(1)  # 0.6366197723675814

f = sinc(0)  # 1

print(f"Sinc (sinc(1)): {e}")

print(f"Sinc (sinc(0)): {f}")

#cmath functions for complex numbers

g = cmath.sin(c)  # Sine of a complex number

h = cmath.cos(c)  # Cosine of a complex number

i = cmath.exp(c)  # Exponential of a complex number

print(f"Sine of Complex (cmath.sin(complex(3, 4))): {g}")

print(f"Cosine of Complex (cmath.cos(complex(3, 4))): {h}")

print(f"Exponential of Complex (cmath.exp(complex(3, 4))): {i}")

**OUTPUT** 

        Sine (math.sin(math.pi / 2)): 1.0

        Complex Number: (3+4j)

        Real Part (c.real): 3.0

        Imaginary Part (c.imag): 4.0

        Complex (complex(5, -7)): (5-7j)

        Sinc (sinc(1)): 0.6366197723675814

        Sinc (sinc(0)): 1

        Sine of Complex (cmath.sin(complex(3, 4))): (3.853738037919377+27.016813258003932j)

        Cosine of Complex (cmath.cos(complex(3, 4))): (-27.034945603074224-3.851153334811777j)

        Exponential of Complex (cmath.exp(complex(3, 4))): (-13.128783081462158-15.200784463067954j)


3. Create a complex number 5+4i, extract the real and imaginary parts and compute the magnitude of the vector using built in functions

**PROGRAM**

import cmath

#Create a complex number

z = complex(5, 4)

#Extract the real part

real_part = z.real

#Extract the imaginary part

imag_part = z.imag

#Compute the magnitude of the vector
magnitude = abs(z)
# Print the results
print(f"Complex Number: {z}")
print(f"Real Part: {real_part}")
print(f"Imaginary Part: {imag_part}")
print(f"Magnitude: {magnitude}") 

OUTPUT
Complex Number: (5+4j)
Real Part: 5.0
Imaginary Part: 4.0
Magnitude: 6.4031242374328485 
4. Vectorized computing
import numpy as np
# Generate some random data
data = np.random.rand(1000)      # 1000 random numbers
# Example of vectorized operations
# Element-wise operations
result1 = np.sqrt(data)  # Square root of each element
result2 = np.sin(data)   # Sine of each element
result3 = data ** 2      # Square of each element
# Reduction operations
sum_data = np.sum(data)          # Sum of all elements
mean_data = np.mean(data)        # Mean of all elements
max_data = np.max(data)          # Maximum value
argmax_data = np.argmax(data)    # Index of maximum value
# Print some results for illustration
print(f"Square root of data: {result1}")
print(f"Sine of data: {result2}")
print(f"Square of data: {result3}")

print(f"Sum of data: {sum_data}")
print(f"Mean of data: {mean_data}")
print(f"Max value in data: {max_data}")
print(f"Index of max value in data: {argmax_data}")
OUTPUT
Square root of data: [0.67964719 0.70820527 0.90902855 0.62451891 0.7091313  0.63921897
 0.72282841 0.87129517 0.98354684 0.94521795]
Sine of data: [0.62464747 0.34455672 0.83189612 0.46414262 0.34606488 0.6037581
 0.48653912 0.77040554 0.9887034  0.93816563]
Square of data: [0.46225183 0.50142176 0.82627745 0.38973066 0.50216641 0.40890197
 0.52198372 0.75942523 0.96731707 0.89358567]
Sum of data: 6.570759632600227
Mean of data: 0.6570759632600227
Max value in data: 0.9835468354977567
Index of max value in data: 8

7. Execute a script  to obtain the dot product and the cross product of two vectors a and b, where a = (1 5 6) and b = (2 3 8).
PROGRAM
import numpy as np
# Define vectors a and b
a = np.array([1, 5, 6])
b = np.array([2, 3, 8])
# Compute dot product
dot_product = np.dot(a, b)
# Compute cross product
cross_product = np.cross(a, b)
# Print results
print(f"Dot Product: {dot_product}")
print(f"Cross Product: {cross_product}")
OUTPUT
Dot Product: 53
Cross Product: [ 27 -10  -7]
8.. The voltage across a capacitor is   
Plot voltage v (t), versus time, t, for t = 0 to 50 seconds with increment of 5 s. Do not use loops.
PROGRAM
import numpy as np
import matplotlib.pyplot as plt
# Constants and initial conditions
V0 = 10.0  # Initial voltage (V)
R = 1.0    # Resistance (Ohms)
C = 1.0    # Capacitance (Farads)
t = np.arange(0, 51, 5)  # Time array from 0 to 50 seconds with increment of 5 s
# Calculate voltage v(t)
voltage = V0 * np.exp(-t / (R * C))
# Plotting
plt.figure(figsize=(8, 6))
plt.plot(t, voltage, marker='o', linestyle='-', color='b', label='Voltage $v(t)$')
plt.title('Voltage Across Capacitor vs Time')
plt.xlabel('Time (s)')
plt.ylabel('Voltage (V)')
plt.grid(True)
plt.legend()
plt.show()
OUTPUT
 
INFERENCE:
Familiarized with basic arithmetic functions for scientific computing and used vectorized computing for fast scientific applications.
