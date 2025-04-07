# Matplotlib Plotting Examples

This repository contains examples and code snippets demonstrating the usage of Matplotlib for data visualization in Python. The examples cover a variety of common plot types, such as line plots, bar charts, scatter plots, and pie charts.

## Table of Contents
1. [Installation](#installation)
2. [Usage](#usage)
3. [Examples](#examples)
   - Line Plot
   - Pie Chart
   - Bar Chart
   - Subplots
   - Polar Plot
   - Exponential and Trigonometric Functions Plot
4. [Conclusion](#conclusion)

---

## Installation

You will need to install `Matplotlib` and `NumPy` to run the examples. You can install them via pip:

```bash
pip install matplotlib numpy
```

## Usage

Clone this repository to your local machine:

```bash
git clone https://github.com/Evertte/matplotlib-examples.git
```

Run any of the Python scripts in this repository to visualize the different plotting techniques.

## Examples

### Line Plot

This example demonstrates how to plot a simple line graph.

```python
import numpy as np
import matplotlib.pyplot as plt

N_A_X = np.arange(2, 20, 3)
N_A_Y = np.arange(1, 12, 2)

plt.xlabel("N_A_X")
plt.ylabel("N_A_Y")
plt.title("Plot N_A_X by N_A_Y")
plt.plot(N_A_X, N_A_Y, color="red")
plt.show()
```

### Pie Chart

This example demonstrates how to create a pie chart.

```python
sizes = [5, 15, 10, 20 , 40 , 10]
labels = ["Scifi", "Drama", "Thriller", "Comedy", "Action", "Romance"]
explode = (0, 0, 0, 0, 0.1, 0)

plt.pie(sizes, labels=labels, explode=explode, autopct='%1.1f%%', shadow=True, startangle=90)
plt.axis('equal')
plt.show()
```

### Bar Chart

This example demonstrates both vertical and horizontal bar charts.

```python
X = np.arange(1, 9)
Y = X ** 2

plt.bar(X, Y)
plt.show()

plt.barh(X, Y)
plt.show()
```

### Subplots

This example demonstrates how to create subplots for different visualizations.

```python
plt.subplot(2, 2, 1)
plt.plot(X1, Y1, "red")
plt.subplot(2, 2, 2)
plt.plot(Y1, Y1, "blue")
plt.subplot(2, 2, 3)
plt.plot(X1, X1, "green")
plt.subplot(2, 2, 4)
plt.plot(Y1, X1, "black")
plt.show()
```

### Polar Plot

This example demonstrates how to create a polar plot.

```python
plt.polar(X, Y)
plt.show()
```

### Exponential and Trigonometric Functions Plot

This example demonstrates how to plot exponential and trigonometric functions.

```python
X = np.arange(-1, 5, 0.1)
Y = np.exp(-X) * np.cos(5 * X)

plt.plot(X, Y)
plt.show()
```

### Bar Chart with Annotations

This example demonstrates how to add annotations to a bar chart.

```python
import calendar
import numpy as np
import matplotlib.pyplot as plt

month_num = [1,2,3,4,5,6,7,8,9,10,11,12]
units_sold = [12, 34, 54, 33, 65, 90, 24, 89, 78, 55, 14, 38]

fig, ax = plt.subplots()
plt.xticks(month_num, calendar.month_name[1:13], rotation=20)
plot = ax.bar(month_num, units_sold)
for rect in plot:
    height = rect.get_height()
    ax.text(rect.get_x() + rect.get_width()/2., 1.002*height, "%d" % int(height), ha="center", va="bottom")
plt.show()
```

## Conclusion

This repository provides basic examples for using Matplotlib to visualize data in Python. You can expand these examples by modifying the data or trying out different types of plots, such as histograms, scatter plots, and 3D plots. Happy plotting!
