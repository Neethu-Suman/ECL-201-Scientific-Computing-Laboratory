**EXP NO: 8**										

**Coin Toss and Level crossing problem**

**OBJECTIVE**

●	To understand and explore random process simulation

1. Simulate a coin toss that maps a head as 1 and tail as 0. Toss the coin N = 100, 500,1000, 5000 and 500000 times and compute the probability (p) of head in each case. Compute the absolute error |0.5 - p| in each case and plot against N and understand the law of large numbers.

**PROGRAM**

import numpy as np

import matplotlib.pyplot as plt

#Define the number of trials for each experiment

N_values = [100, 500, 1000, 5000, 500000]

#Initialize empty lists to store the probabilities and absolute errors

probabilities = []

absolute_errors = []

#Loop through each number of trials
for N in N_values:
  # Initialize counter for heads
  heads_count = 0
  # Simulate N coin tosses
  for i in range(N):
    # Generate a random number between 0 and 1
    random_number = np.random.rand()
    # If the random number is less than 0.5, count it as a head
    if random_number > 0.5:
      heads_count += 1
  # Calculate the probability of heads
  probability = heads_count / N
  # Calculate the absolute error
  absolute_error = abs(0.5 - probability)
  # Append the values to the lists
  probabilities.append(probability)
  absolute_errors.append(absolute_error)
# Plot the absolute errors against N
plt.plot(N_values, absolute_errors)
plt.xlabel('Number of Trials (N)')
plt.ylabel('Absolute Error (|0.5 - p|)')
plt.title('Law of Large Numbers')
plt.show()

OUTPUT
 
2. Create a uniform random vector with a maximum magnitude of 10, plot, and observe. Set a threshold (VT = 2) and count how many times the random function has crossed VT. Count how many times the function has gone above and below the threshold.
PROGRAM
import numpy as np
import matplotlib.pyplot as plt
# Generate a uniform random vector with maximum magnitude 10
v = 10 * (np.random.rand(10))
x = range(10)
# Plot the random vector
plt.scatter(x,v)
plt.axhline(y=2, color='r', linestyle='--', label='Threshold VT = 2')  # Adding a line at VT = 2
plt.xlabel('Index')
plt.ylabel('Value')
plt.title('Uniform Random Vector')
plt.show()
# Set a threshold (VT = 2)
VT = 2
# Count how many times the random function has crossed VT
crossings = np.sum(np.abs(v) > VT)
# Count how many times the function has gone above and below the threshold
above_threshold = np.sum(v > VT)
below_threshold = np.sum(v < VT)
# Print the results
print(f'Number of crossings: {crossings}')
print(f'Number of times above threshold: {above_threshold}')
print(f'Number of times below threshold: {below_threshold}')
 
Number of crossings: 6
Number of times above threshold: 6
Number of times below threshold: 2

INFERENCE
	Familiarized with basic random process functions and used it in simulating coin toss and level crossing problem
