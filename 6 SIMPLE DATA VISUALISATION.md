**EXP NO: 6**										

**SIMPLE DATA VISUALISATION**

**OBJECTIVE**

●	To visualize the data in different ways

1. Draw stem plots, line plots, box plots, bar plots and scatter plots with random data.

**PROGRAM**

import matplotlib.pyplot as plt

import numpy as np

Generate some random data

x = np.random.rand(5)

y = np.random.rand(5)

Create a figure with 5 subplots

fig, axs = plt.subplots(1, 4, figsize=(20, 5))

Plot the data as a stem plot on the first subplot

axs[0].stem(x)

axs[0].set_title('Stem Plot')

Plot the data as a line plot on the second subplot

axs[1].plot(x,y)

axs[1].set_title('Line Plot')

Plot the data as a box plot on the third subplot

axs[2].boxplot(x)

axs[2].set_title('Box Plot')

Plot the data as a bar plot on the fourth subplot

axs[3].scatter(x, y)

axs[3].set_title('Scatter Plot')

Show the figure

plt.show()

**OUTPUT**

<img src="https://github.com/Neethu-Suman/ECL-201-Scientific-Computing-Laboratory/blob/main/CODES/EXP%206/1.png" width="400">
 
x

Out[24]: array([0.1039641 , 0.83258058, 0.29389689, 0.84802476, 0.6458698 ])

y

Out[25]: array([0.26463336, 0.54671308, 0.42698847, 0.01637255, 0.9540992 ])

2. Plot the bar chart that displays the supply of different fruits (apple, blueberry, cherry, and orange) with corresponding colors (red, blue, and orange). Include bar labels and bar colors as 'red', 'blue', '_red', and 'orange', a title for the chart, and a legend for the fruit colors.

**Program** 

import matplotlib.pyplot as plt

fruits = ['apple', 'blueberry', 'cherry', 'orange']

counts = [40, 100, 30, 55]

bar_labels = ['red', 'blue', '_red', 'orange']

bar_colors = ['tab:red', 'tab:blue', 'tab:red', 'tab:orange']

#Plot each bar individually so that each one can have a separate label

for i in range(len(fruits)):

plt.bar(fruits[i], counts[i], label=bar_labels[i], color=bar_colors[i])

#Create the bars

bars = plt.bar(fruits, counts, color=bar_colors)

#Add labels on top of each bar

for bar, count in zip(bars, counts):

plt.text(bar.get_x() + bar.get_width() / 2,  bar.get_height() - 5,str(count), ha='center', va='top', color='white', fontweight='bold')

plt.ylabel('Fruit supply')

plt.title('Fruit supply by kind and color')

plt.legend(title='Fruit color')

plt.show()

**OUTPUT**

<img src="https://github.com/Neethu-Suman/ECL-201-Scientific-Computing-Laboratory/blob/main/CODES/EXP%206/2.png" width="400">
 

3.  Plot the histogram of random data. And add legends in plots.

**PROGRAM**

import numpy as np
import matplotlib.pyplot as plt

#Generate some random data

data = np.random.rand(100)

#Create the histogram and capture the bin heights and bin edges

counts, bins, patches = plt.hist(data, bins=20, edgecolor='black')

#Add text labels on top of each bar

for count, patch in zip(counts, patches):

#Get the center of the bar

bin_x = patch.get_x() + patch.get_width() / 2

#Add text above the bar

plt.text(bin_x, count, str(int(count)), ha='center', va='bottom', color='black', fontweight='bold')

#Add title and labels

plt.title('Histogram of Random Data')

plt.xlabel('Value')

plt.ylabel('Frequency')

plt.show()

**OUTPUT**


 

4. Implement and plot the functions with t = [-10; 10] with increment 0:01

A. f(t) = cos t

B. f(t) = cos t cos 5t + cos 5t

import numpy as np

import matplotlib.pyplot as plt

#Create a vector t = [-10; 10] with increment 0:01 as an array.

t = np.arange(-10, 10.01, 0.01)

#Define the function f(t) = cos t

def f1(t):

return np.cos(t)

#Define the function f(t) = cos t cos 5t + cos 5t

def f2(t):

return np.cos(t) * np.cos(5 * t) + np.cos(5 * t)

#Plot the functions

plt.plot(t, f1(t), label='f(t) = cos t')

plt.plot(t, f2(t), label='f(t) = cos t cos 5t + cos 5t')

#Add legend and labels

plt.legend()

plt.xlabel('t')

plt.ylabel('f(t)')

#Show the plot

plt.show()

**OUTPUT**
 
**INFERENCE**

Familiarized with basic visualization plots using matplotlib 

