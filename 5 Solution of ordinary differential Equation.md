EXP NO: 5										
Solution of ordinary differential Equation
OBJECTIVE
	To solve ordinary differential Equation
LEARNING OUTCOMES
	After the completion of this experiment students will be able to solve  ordinary differential Equation
SOFTWARE USED: 
                 Spider

1. Solve the first order differential equation

(dx )/dt+2x=0
With initial condition x(0)=1
PROGRAM
import numpy as np
from scipy.integrate import odeint

def model(x, t):
  """
  This function defines the differential equation dx/dt + 2x = 0.
  """
  return -2 * x

# Initial condition
x0 = 1

# Time points
t = np.linspace(0, 10, 100)

# Solve the differential equation
x = odeint(model, x0, t)

# Plot the solution
plt.plot(t, x)
plt.xlabel('t')
plt.ylabel('x(t)')
plt.show()

OUTPUT
 

2. solve second order differential equation
d2x/dt2+2 dx/dt  +2x=ℯ -t

Program
def model(y, t):
  """
  This function defines the second order differential equation d2x/dt2 + 2 dx/dt + 2x = e-t.
  """
  x, v = y
  dxdt = v
  dvdt = -2 * v - 2 * x + np.exp(-t)
  return [dxdt, dvdt]

# Initial conditions
y0 = [0, 0]

# Time points
t = np.linspace(0, 10, 1000)

# Solve the differential equation
y = odeint(model, y0, t)

# Extract the solution for x(t)
x = y[:, 0]

# Plot the solution
plt.plot(t, x)
plt.xlabel('t')
plt.ylabel('x(t)')
plt.show()

OUTPUT
 
INFERENCE:
Solved the ordinary differential Equations and plotted it
