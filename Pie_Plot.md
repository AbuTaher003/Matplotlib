
# Pie Chart Notes

## Introduction to Pie Chart
Pie charts are circular charts divided into sectors, each representing a proportion of the whole. The `matplotlib` library in Python provides the `plt.pie()` function to create pie charts with various customizable features.

---

## Basic Pie Chart Code Example
```python
import matplotlib.pyplot as plt

x = [10, 30, 20, 15]  # Data values for the chart
y = ["C", "Python", "C++", "Java"]  # Labels for each sector
c = ['r', 'b', 'y', 'm']  # Colors for each sector
ex = [0.3, 0.0, 0.0, 0.0]  # Highlight one sector by separating it from the chart

plt.pie(x, labels=y, colors=c, explode=ex, autopct="%0.1f%%", radius=0.7, shadow=True, 
        labeldistance=1.1, startangle=0, textprops={"fontsize": 10}, counterclock=False, 
        wedgeprops={"linewidth": 2}, rotatelabels=False)
plt.title("Pie Chart")
plt.legend(loc=1)  # Display legend at location 1 (upper-right corner)
plt.show()
```

### Explanation:
1. **`colors` and `labels`:** Unlike `bar`, `scatter`, or `histogram`, the `colors` and `labels` parameters in pie charts require an `s` at the end.
2. **`explode`:** Separates one or more sectors. Set the value to a non-zero number for the sector you want to highlight, and others to `0.0`.
3. **`autopct`:** Displays percentages in the chart. `"%0.1f%%"` shows percentages with one decimal place.
4. **`shadow`:** Adds a shadow effect to the chart.
5. **`radius`:** Adjusts the size of the pie chart.
6. **`labeldistance`:** Determines how far labels are from the center of the chart.
7. **`startangle`:** Rotates the chart to start at a specified angle.
8. **`textprops`:** Customizes text properties like font size and color.
9. **`counterclock`:** `True` keeps the default counterclockwise direction. `False` makes it clockwise.
10. **`wedgeprops`:** Adjusts the thickness or shadow width of edges.
11. **`rotatelabels`:** Rotates labels when `True`.

---

## Single Sector Pie Chart
```python
plt.pie([1])
plt.show()
```
This creates a simple chart with only one sector.

---

## Nested Pie Chart
### Code Example:
```python
import matplotlib.pyplot as plt

x = [10, 20, 40, 30]
x1 = [20, 10, 40, 30]
y = ["C", "C++", "Python", "Java"]
c = ['r', 'b', 'm', 'g']

plt.pie(x, labels=y)
plt.pie(x1, radius=0.5, colors=c)  # Inner pie chart with a smaller radius
plt.show()
```

---

## Ring-Type Pie Chart (Method 1)
### Code Example:
```python
import matplotlib.pyplot as plt

x = [10, 20, 40, 30]
y = ["C", "C++", "Python", "Java"]

plt.pie(x, labels=y)
plt.pie([1], radius=0.7, colors="w")  # White inner circle to create a ring effect
plt.show()
```

---

## Ring-Type Pie Chart (Method 2)
### Code Example:
```python
import matplotlib.pyplot as plt

x = [10, 30, 20, 40]
y = ["C", "C++", "Python", "Java"]

plt.pie(x, labels=y)
cr = plt.Circle(xy=(0, 0), facecolor="w", radius=0.7)  # Add a white circle
plt.gca().add_artist(cr)  # Add the circle to the current plot
plt.show()
```

---

