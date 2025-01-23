# Box Plot and Whisker Plot

This note explains how to create box plots and whisker plots using `matplotlib`. A box plot is used to visualize the distribution and variability of data. Below are the Python code snippets and their explanations.

---

## Code for a Single Box Plot:
```python
import matplotlib.pyplot as plt

# Data points
x = [10, 20, 30, 40, 50, 60, 70, 120]

# Create a box plot
plt.boxplot(
    x,
    labels=["Python"],
    notch=False,  # If True, the box will have a notch
    widths=0.2,  # Width of the box
    patch_artist=False,  # If True, fills the box with color
    showmeans=True,  # Displays a mean indicator
    whis=1.2,  # Whisker length factor (default is 1.5)
    sym="go",  # Customize outlier marker
    boxprops={"color": 'b'},  # Customize box color
    capprops={"color": 'b'},  # Customize cap color
    whiskerprops={"color": 'b'},  # Customize whisker color
    flierprops={"markeredgecolor": 'r'}  # Customize outlier edge color
)

plt.show()
```

### Details:
1. **notch**: When `True`, adds a notch to the box.
2. **widths**: Controls the box's width.
3. **patch_artist**: Fills the box interior when `True`.
4. **showmeans**: Displays the mean with a marker.
5. **sym**: Customizes outlier markers (e.g., "go" for green circles).
6. **boxprops, capprops, whiskerprops, flierprops**: Customize box, cap, whisker, and outlier styles using dictionaries.
7. **whis**: Adjusts whisker length (e.g., 1.2 for 1.2 times the IQR).

---

## Code for Multiple Box Plots:
```python
import matplotlib.pyplot as plt

# Data points for multiple plots
x = [10, 20, 30, 40, 50, 60, 70]
x1 = [10, 20, 30, 40, 50, 60, 90]

# Combine data into a list
y = [x, x1]

# Create multiple box plots
plt.boxplot(
    y,
    labels=["Python", "C++"],  # Labels for each box
    patch_artist=False,  # If True, fills the box with color
    showmeans=True  # Displays a mean indicator
)

# Add title and legend
plt.title("Box Plot and Whisker Plot", color='r', fontsize=15)
plt.legend(["BoxPlot"], loc="upper left")

plt.show()
```

### Details:
- You can plot multiple box plots by passing a list of data arrays.
- Each label in the `labels` parameter corresponds to a box plot.
- Customize properties as needed, similar to the single box plot.

---

## Notes:
1. **Matplotlib Warning:**
   - In newer versions of `matplotlib`, the `labels` parameter has been renamed to `tick_labels`. Update your code accordingly if you encounter a warning.

2. **Customization:**
   - Use `patch_artist=True` to fill boxes with colors.
   - Adjust whisker length using `whis` to represent specific data ranges.

---


