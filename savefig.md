# Savefig in Matplotlib

This note explains how to save plots as image files using `plt.savefig()` in Matplotlib. Below are the Python code snippets and their explanations.

---

## Code Example:
```python
import matplotlib.pyplot as plt

# Data points
x = [1, 2, 3, 4, 5]
y = [2, 1, 3, 2, 4]

# Plotting the graph
plt.plot(x, y, color='r')

# Save the plot with default settings
plt.savefig("line")  # Saves the image in the current folder with the name "line"

# Save the plot with custom settings
plt.savefig("line1", dpi=2000, facecolor='g', transparent=False)

plt.show()
```

### Explanation:
1. **plt.savefig("line")**:
   - Saves the plot in the current working directory.
   - The file will be named "line" with the default image format (usually PNG).

2. **Custom Parameters in plt.savefig()**:
   - **dpi**: Dots per inch (image resolution). Higher `dpi` means better quality. Default is 72 or 100.
   - **facecolor**: Changes the frame color of the image.
   - **transparent=True**: Makes the background of the image transparent (removes the default white background).
   - **bbox_inches="tight"**: Adjusts the bounding box of the plot to tightly fit the content.
   - **Formats**: You can save images in different formats like PNG, JPG, PDF, etc. For example: `plt.savefig("line1.pdf")`.

---

## DPI Example:
```python
import matplotlib.pyplot as plt

# 1st Figure: Default dpi
plt.figure(figsize=(5, 5), dpi=72)  # Default dpi
plt.plot([1, 2, 3, 4], [10, 20, 25, 30])
plt.title("Default DPI (72)")
plt.savefig("default_dpi.png")

# 2nd Figure: High dpi
plt.figure(figsize=(5, 5), dpi=300)  # Higher dpi for better quality
plt.plot([1, 2, 3, 4], [10, 20, 25, 30])
plt.title("High DPI (300)")
plt.savefig("high_dpi.png")

plt.show()
```

### Explanation:
1. **Default DPI (72)**:
   - Produces a lower-quality image.
   - File is smaller in size.

2. **High DPI (300)**:
   - Produces a higher-quality image suitable for printing.
   - File size will be larger due to better resolution.

---

## Key Notes:
1. **Current Directory**:
   - The saved file is stored in the folder where the Python script is running. Check the folder to find the saved file.

2. **Customizing Image Format**:
   - Change the format by adding an extension (e.g., `.png`, `.jpg`, `.pdf`).

3. **Transparent Background**:
   - Use `transparent=True` to remove the white background of the plot.

4. **Bounding Box Adjustment**:
   - `bbox_inches="tight"` ensures there is no extra space around the plot.

---

This guide provides a clear understanding of saving plots with `matplotlib.pyplot.savefig`. 
