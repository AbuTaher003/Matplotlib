# Fill Between Plot

This note explains the concept of a fill-between plot using `matplotlib`. The fill-between plot highlights specific areas between two curves or between a curve and a baseline. Below is the Python code and its explanation.

## Code:
```python
import matplotlib.pyplot as plt
import numpy as np

# Define data points as numpy arrays
x = np.array([1, 2, 3, 4, 5, 6])
y = np.array([1, 2, 3, 4, 5, 6])

# Plot the line\plt.plot(x, y, color='r')

# Highlight the area between x = 2 and x = 4
plt.fill_between(x, y, color='g', where=(x >= 2) & (x <= 4), alpha=0.5)

# Add labels and title
plt.xlabel("X - axis")
plt.ylabel("Y - axis")
plt.title("Fill between plot", color='r', fontsize=20)

# Display the plot
plt.show()
```

---

## Explanation:

### What does the code do?
This code creates a fill-between plot with a red line connecting the points in `x` and `y`. It shades the region between the line and the x-axis from `x = 2` to `x = 4` with a green color. The shading is semi-transparent due to `alpha=0.5`.

### Key Points:
1. **Why Use Numpy Arrays?**
   - To use the `where` condition (`x >= 2` & `x <= 4`), the data must be numpy arrays. Regular Python lists will not work directly.

2. **How to Highlight a Region?**
   - Use `plt.fill_between()` to fill the area. The parameters include:
     - `x` and `y`: Define the curve.
     - `color`: Choose the color of the fill.
     - `where`: Specify the condition for filling the area (e.g., between `x = 2` and `x = 4`).
     - `alpha`: Set transparency.

3. **Default Fill Behavior:**
   - If you pass only `x` and `y` to `fill_between()`, it shades the area between the curve and the x-axis.

4. **Custom Area Selection:**
   - For a specific region (e.g., `x = [2, 4]`, `y1 = 2`, `y2 = 4`), use the `where` condition to highlight the region.

### Plot Description:
- The x-axis and y-axis represent the data points.
- The red line shows the values of `y` against `x`.
- The green shading emphasizes the region between `x = 2` and `x = 4`.

---

This simple code demonstrates how to highlight specific regions in your plot using `matplotlib`. You can customize it further by adjusting the data, colors, and transparency.

