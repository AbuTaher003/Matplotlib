# Scatter Plot Notes

## Basic Scatter Plot
```python
import matplotlib.pyplot as plt

# Data points
day = [1, 2, 3, 4, 5, 6, 7]
no = [2, 3, 1, 5, 4, 7, 6]
c = ['r', 'g', 'r', 'y', 'g', 'b', 'y']
size = [40, 60, 20, 30, 40, 70, 30]

# Scatter plot
plt.scatter(day, no, color=c, s=size, marker="*", edgecolor='g', linewidth=0.5)

# Labels and title
plt.xlabel("Day", fontsize=15)
plt.ylabel("No.", fontsize=15)
plt.title("Scatter Plot", color='b', fontsize=25)

plt.show()
```

### Explanation:
- **day** and **no** are the x and y-axis values.
- **color (c)** specifies the color of the points.
- **size (s)** adjusts the size of the scatter points.
- **marker** specifies the style of the marker (e.g., "*").
- **edgecolor** and **linewidth** add styling to the edges of the points.

---

## Adding a Color Bar
```python
import matplotlib.pyplot as plt

# Data points
day = [1, 2, 3, 4, 5, 6, 7]
no = [2, 3, 1, 5, 4, 7, 6]
colours = [0.1, 0.2, 0.3, 0.4, 0.5, 0.6, 0.7]
size = [400, 600, 200, 300, 400, 700, 300]

# Scatter plot with color mapping
plt.scatter(day, no, c=colours, s=size, cmap="viridis", alpha=0.5)

# Adding color bar
plt.colorbar().set_label("ColorBar", fontsize=10)

# Labels and title
plt.xlabel("Day", fontsize=15)
plt.ylabel("No.", fontsize=15)
plt.title("Scatter Plot", color='b', fontsize=25)

plt.show()
```

### Explanation:
- **cmap="viridis"** maps numerical data to colors.
- **plt.colorbar()** adds a color bar, and **set_label()** names it.
- **alpha** adjusts transparency (0 = fully transparent, 1 = opaque).

---

## Adding a Second Scatter Plot
```python
import matplotlib.pyplot as plt

# Data points
day = [1, 2, 3, 4, 5, 6, 7]
no = [2, 3, 1, 5, 4, 7, 6]
no2 = [3, 4, 1, 5, 2, 7, 6]

colours = [0.1, 0.2, 0.3, 0.4, 0.5, 0.6, 0.7]
size = [400, 600, 200, 300, 400, 700, 300]

# First scatter plot
plt.scatter(day, no, c=colours, s=size, cmap="viridis", alpha=0.5)

# Second scatter plot
plt.scatter(day, no2, c='r', s=size)

# Adding color bar
t = plt.colorbar()
t.set_label("ColorBar", fontsize=10)

# Labels and title
plt.xlabel("Day", fontsize=15)
plt.ylabel("No.", fontsize=15)
plt.title("Scatter Plot", color='b', fontsize=25)

plt.show()
```

### Explanation:
- Added **no2** for a second scatter plot.
- Combined plots by calling **plt.scatter()** twice.
- Used different colors for distinction.

---

## Practice Example with Legends
```python
import matplotlib.pyplot as plt

# Data points
day = [1, 2, 3, 4, 5, 6]
no = [2, 6, 9, 3, 5, 1]
no2 = [4, 3, 5, 2, 8, 6]

colors = [0.1, 0.2, 0.3, 0.4, 0.5, 0.6]
size = [200, 400, 300, 500, 300, 280]

# First scatter plot
plt.scatter(day, no, c=colors, s=size, cmap='viridis', alpha=0.5, label="Scatter")
plt.legend(loc="upper left")

# Second scatter plot
plt.scatter(day, no2, c='r', s=size)

# Adding color bar
t = plt.colorbar()
t.set_label("ColorBar", fontsize=10)

# Labels and title
plt.xlabel("Day", fontsize=15)
plt.ylabel("No.", fontsize=15)
plt.title("Scatter plot", fontsize=20, color='r')

plt.show()
```

### Explanation:
- **label="Scatter"** adds a legend, and **plt.legend()** displays it.
- Used **loc="upper left"** to position the legend.

---

### Key Points to Remember:
1. **plt.scatter()** is used for scatter plots.
2. Use **cmap** for color mapping and **alpha** for transparency.
3. Add multiple plots by calling **plt.scatter()** multiple times.
4. Use **plt.colorbar()** to add a color bar.
5. Legends and labels make the plot more understandable.

---

