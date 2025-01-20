# Stem Plot in Matplotlib

This note explains the code and functionality of stem plots in Matplotlib. Follow this to easily understand the topic and implement it in your projects.

### Code Example:
```python
import matplotlib.pyplot as plt

# Data for the stem plot
x = [1, 2, 3, 4, 5, 6]
y = [2, 2, 4, 3, 6, 5]

# Creating the stem plot
plt.stem(x, y, linefmt=":", markerfmt="ro", bottom=0, basefmt='b')

# Adding labels
plt.xlabel("Time", fontsize=15)
plt.ylabel("Speed", fontsize=15)

# Display the plot
plt.show()
```

### Key Features Explained:

1. **plt.stem():**
   - This function is used to create a stem plot where data points are shown with markers, and vertical lines connect them to a baseline.

2. **linefmt=":":**
   - Specifies the design of the vertical lines connecting the markers to the baseline. Here, `":"` means dotted lines.

3. **markerfmt="ro":**
   - Defines the design of the markers. Here, `"ro"` sets the marker shape to a circle (`o`) and its color to red (`r`).

4. **bottom=0:**
   - Sets the starting point (baseline) for the vertical lines. Here, it is set to `0`.

5. **basefmt='b':**
   - Specifies the color and style of the baseline. Here, `"b"` sets the baseline color to blue.

### Customization Options:
- Modify `linefmt`, `markerfmt`, `bottom`, and `basefmt` to create different styles for the plot.
- Change `x` and `y` values to reflect your data.

### Visualization:
Stem plots are ideal for representing discrete data, where the relationship between data points and the baseline is visually significant.

This explanation and code should help you understand and create stem plots with ease. Feel free to explore additional customization options in Matplotlib!

