**EXP NO: 3**		

**REALIZATION OF ARRAYS AND MATRICES**

**OBJECTIVE**

●	To familiarize with the realization of arrays and matrixes and their visualization using plotting functions and GUI

**LEARNING OUTCOMES**

●	After the completion of this experiment students will be able to approximate an array/matrix with matrix decomposition.

**SOFTWARE USED:** 
          
SPYDER

1. Realize one dimensional array of real and complex numbers

**PROGRAM**

import numpy as np

#Create a one-dimensional array of real numbers

real_array = np.array([1, 2, 3, 4, 5])

#Create a one-dimensional array of complex numbers

complex_array = np.array([1 + 2j, 3 + 4j, 5 + 6j, 7 + 8j, 9 + 10j])

#Print the real array

print("Real array:", real_array)

#Print the complex array

print("Complex array:", complex_array)

**OUTPUT**

Real array: [1 2 3 4 5]

Complex array: [1. +2.j 3. +4.j 5. +6.j 7. +8.j 9.+10.j]

2.	Stem and continuous plots of real arrays using matplotlib/GUIs/charts.

**PROGRAM**

#Stem plot of the real array

plt.stem(real_array)

plt.title('Stem Plot of Real Array')

plt.show()

#Continuous plot of the real array

plt.plot(real_array)

plt.title('Continuous Plot of Real Array')

plt.show()

**OUTPUT**

<img src="https://github.com/Neethu-Suman/ECL-201-Scientific-Computing-Laboratory/blob/main/CODES/EXP3/1.png" width="600">

<img src="https://github.com/Neethu-Suman/ECL-201-Scientific-Computing-Laboratory/blob/main/CODES/EXP3/2.png" width = "600">
 
 
3. Find the roots of the following quadratic equation

x2 -2x +3 = 0

**PROGRAM**

import cmath

#Coefficients

a = 1

b = -2

c = 3

#Calculate the discriminant

discriminant = b**2 - 4*a*c

#Find the roots using the quadratic formula

root1 = (-b + cmath.sqrt(discriminant)) / (2*a)

root2 = (-b - cmath.sqrt(discriminant)) / (2*a)

#Print the roots

print(f"The roots of the equation are {root1} and {root2}")

**OUTPUT**

The roots of the equation are (1+1.4142135623730951j) and (1-1.4142135623730951j)

4.  Create two separate row vectors(arrays) a and b that contains elements from 1 to 10. Create an array of complex numbers z with a as the real part and b as the imaginary part. Find the sum and complex conjugate of the array z  

**PROGRAM**

import numpy as np

#Create row vectors a and b

a = np.arange(1, 11)

b = np.arange(1, 11)

#Create array of complex numbers z

z = a + 1j * b

#Find the sum of the array z

sum_z = np.sum(z)

#Find the complex conjugate of the array z

conjugate_z = np.conj(z)

#Print the results

print(f"Vector a: {a}")

print(f"Vector b: {b}")

print(f"Complex array z: {z}")

print(f"Sum of z: {sum_z}")

print(f"Complex conjugate of z: {conjugate_z}") 

**OUTPUT**

Vector a: [ 1  2  3  4  5  6  7  8  9 10]

Vector b: [ 1  2  3  4  5  6  7  8  9 10]

Complex array z: [ 1. +1.j  2. +2.j  3. +3.j  4. +4.j  5. +5.j  6. +6.j  7. +7.j  8. +8.j   9. +9.j 10.+10.j]

Sum of z: (55+55j)

Complex conjugate of z: [ 1. -1.j  2. -2.j  3. -3.j  4. -4.j  5. -5.j  6. -6.j  7. -7.j  8. -8.j 9. -9.j 10.-10.j] 

5. Realization of two dimensional arrays and matrices and their visualizations with imshow/matshow/charts

**PROGRAM**

import numpy as np

import matplotlib.pyplot as plt

#Create a two-dimensional array of real numbers

real_array = np.array([[1, 2, 3], [4, 5, 6], [7, 8, 9]])

#Print the real array

print("Real array:\n", real_array)

#imshow of the real array

plt.imshow(real_array, cmap="hot")

plt.title('Imshow of Real Array')

plt.show()

#matshow of the real array

plt.matshow(real_array, cmap="viridis")

plt.title('Matplotlib of Real Array')

plt.show()

**OUTPUT**

Real array:

 [[1 2 3]
 
 [4 5 6]
 
 [7 8 9]]

<img src="https://github.com/Neethu-Suman/ECL-201-Scientific-Computing-Laboratory/blob/main/CODES/EXP3/3.png" width ="600">

<img src="https://github.com/Neethu-Suman/ECL-201-Scientific-Computing-Laboratory/blob/main/CODES/EXP3/4.png" width ="600">

6. 	Inverse of a square matrix and the solution of the matrix equation [A][X] = [b] where A is an N x N matrix and X and b are N x 1 vectors.

**PROGRAM**

import numpy as np

#Define the matrix A

A = np.array([[2, 3], [1, 4]])

#Print the matrix A

print("Matrix A:")

print(A)

#Find the inverse of the matrix A

A_inv = np.linalg.inv(A)

#Print the inverse of the matrix A

print("Inverse of Matrix A:")

print(A_inv)

#Define the matrix b

b = np.array([[5], [2]])

#Print the matrix b

print("Matrix b:")

print(b)

#Solve the matrix equation [A][X] = [b] for [X]

X = np.linalg.solve(A, b)

#Print the solution [X]

print("Solution [X]:")

print(X)

**OUTPUT**

Matrix A:

[[2 3]

 [1 4]]

Inverse of Matrix A:

[[ 0.8 -0.6]

 [-0.2  0.4]]

Matrix b:

[[5]

 [2]]

Solution [X]:

[[ 2.8]

 [-0.2]]

7.. Computation of the rank and eigenvalues of  Matrix A

**PROGRAM**

#Define the matrix A

A = np.array([[2, 3], [1, 4]])

#Print the matrix A

print("Matrix A:")

print(A)

#Compute the rank of the matrix A

rank_A = np.linalg.matrix_rank(A)

#Print the rank of the matrix A

print("Rank of Matrix A:", rank_A)

#Compute the eigenvalues of the matrix A

eigenvalues_A = np.linalg.eigvals(A)

#Print the eigenvalues of the matrix A

print("Eigenvalues of Matrix A:", eigenvalues_A)

**OUTPUT**

Matrix A:

[[2 3]

 [1 4]]

Rank of Matrix A: 2

Eigenvalues of Matrix A: [1. 5.]

8. Approximate A for N = 1000 with the help of singular value decomposition of A as where Ui and Vi are the singular vectors and _i are the eigen values with _i < _j for i > j. One may use the built-in functions for singular value decomposition.

<img src ="https://github.com/Neethu-Suman/ECL-201-Scientific-Computing-Laboratory/blob/main/CODES/EXP3/5.png" width ="100">

**PROGRAM**

import numpy as np

#Define the matrix A

A = np.random.rand(1000, 1000)

#Compute the singular value decomposition of A

U, s, Vh = np.linalg.svd(A)

#Approximate A for N = 1000

A_approx = U[:, :1000] @ np.diag(s[:1000]) @ Vh[:1000, :]

#Print the matrix A

print("Matrix A:")

print(A)

#Print the approximated matrix A for N = 1000

print("Approximated Matrix A for N = 1000:")

print(A_approx)

**OUTPUT**

Matrix A:

[[0.48515969 0.69253842 0.9724357  ... 0.6538901  0.35243468 0.4435475 ]

 [0.73608134 0.17343474 0.95978315 ... 0.04422015 0.02941123 0.36663683]
 
 [0.12665399 0.85741149 0.68248467 ... 0.08905294 0.5524839  0.10351128]
 
 [0.58958556 0.69387035 0.48524938 ... 0.75832046 0.79927468 0.7331946 ]
 
 [0.21118366 0.03826133 0.26771646 ... 0.97975299 0.42143705 0.31806776]
 
 [0.44029941 0.32702244 0.66522572 ... 0.47750262 0.01940912 0.86640744]]

Approximated Matrix A for N = 1000:

[[0.48515969 0.69253842 0.9724357  ... 0.6538901  0.35243468 0.4435475 ]

 [0.73608134 0.17343474 0.95978315 ... 0.04422015 0.02941123 0.36663683]
 
 [0.12665399 0.85741149 0.68248467 ... 0.08905294 0.5524839  0.10351128]

 
 [0.58958556 0.69387035 0.48524938 ... 0.75832046 0.79927468 0.7331946 ]
 
 [0.21118366 0.03826133 0.26771646 ... 0.97975299 0.42143705 0.31806776]
 
 [0.44029941 0.32702244 0.66522572 ... 0.47750262 0.01940912 0.86640744]]

9.  

**PROGRAM**

import numpy as np

import matplotlib.pyplot as plt

#Define the matrix A

A = np.random.rand(1000, 1000)

#Compute the singular value decomposition of A

U, s, Vh = np.linalg.svd(A)

#Compute the absolute error (ABA) between A and A_approx for different values of r

r_values = [10, 50, 75, 100, 250, 500, 750]

aba_values = [ ]

for r in r_values:

  A_approx = U[:, :r] @ np.diag(s[:r]) @ Vh[:r, :]
  
  aba_values.append(np.linalg.norm(A - A_approx, ord='fro'))

#Plot the absolute error (ABA) against r

plt.plot(r_values, aba_values)

plt.xlabel('r')

plt.ylabel('Absolute Error (ABA)')

plt.title('Plot of Absolute Error (ABA) against r')

plt.show()

**OUTPUT**
 
**INFERENCE:**

Familiarized with the realization of arrays and matrixes and their visualization using plotting functions 


