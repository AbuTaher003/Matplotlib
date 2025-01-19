# Step Plot in Matplotlib

This note explains the code and functionality of step plots in Matplotlib. By following this, you will easily grasp the concept and apply it to your projects.

### Code Example:
```python
import matplotlib.pyplot as plt

# Data for the step plot
x = [1, 2, 3, 4, 5, 6]
y = [2, 2, 1, 3, 5, 4]

# Creating the step plot
plt.step(x, y, color='b', marker="o", ms=10, mfc="r", label="Python")

# Adding labels and grid
plt.legend()
plt.xlabel("X - axis")
plt.ylabel("Y - axis")
plt.grid()  # Creates a grid on the plot
plt.title("Step Plot", fontsize=15)

# Display the plot
plt.show()
```

### Key Features Explained:

1. **plt.step():**
   - This function is used to create a step plot where data points are connected by horizontal and vertical lines.

2. **marker="o":**
   - Specifies the type of marker used for data points. Here, "o" creates circular markers.

3. **ms=10:**
   - Sets the marker size. Larger values make bigger markers.

4. **mfc="r":**
   - Stands for Marker Face Color. It determines the fill color of the markers. Here, it is set to red ("r").

5. **plt.grid():**
   - Adds a grid to the plot, making it easier to visualize the alignment of data points.

6. **plt.title():**
   - Sets the title of the plot. The `fontsize` parameter allows you to adjust the font size.

### Visualization:
The step plot connects the data points using horizontal and vertical lines, making it ideal for visualizing changes in value at specific intervals.

### How to Use:
- Customize the `x` and `y` values to represent your data.
- Experiment with different `marker`, `ms`, and `mfc` values to change the appearance of the plot.
- Use `plt.grid()` and labels for better readability.


