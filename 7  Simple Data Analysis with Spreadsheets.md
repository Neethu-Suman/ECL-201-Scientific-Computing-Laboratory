**EXP NO: 7**										

**Simple Data Analysis with Spreadsheets**

OBJECTIVE
●	To export signal values as .csv file, read and display it
LEARNING OUTCOMES
●	After the completion of this experiment students will be able to compute with exported data.

SOFTWARE USED: 
                 SPIDER

1. Display cosine signal and export it as a .csv file. Read this .csv or .xls file as an array and plot it. Compute the mean and standard deviation of the signal. Plot its histogram with an appropriate bin size.


PROGRAM


import numpy as np
import matplotlib.pyplot as plt
import pandas as pd

# Generate a cosine signal
t = np.linspace(0, 2*np.pi, 1000)
y = np.cos(t)

# Export the signal to a CSV file
df = pd.DataFrame({'time': t, 'signal': y})
df.to_csv('cosine_signal.csv')

# Read the CSV file as an array
data = pd.read_csv('cosine_signal.csv')
t = data['time'].to_numpy()
y = data['signal'].to_numpy()

# Plot the signal
plt.plot(t, y)
plt.xlabel('Time')
plt.ylabel('Signal')
plt.title('Cosine Signal')
plt.show()

# Compute the mean and standard deviation of the signal
mean = np.mean(y)
std = np.std(y)
print('Mean:', mean)
print('Standard deviation:', std)

# Plot the histogram of the signal
plt.hist(y, bins=20)
plt.xlabel('Signal')
plt.ylabel('Frequency')
plt.title('Histogram of Cosine Signal')
plt.show()


OUTPUT

 

Mean: 0.0009999999999999148
Standard deviation: 0.7074595394791139


 



INFERENCE
	Familiarized with basic Simple Data Analysis using CSV file
