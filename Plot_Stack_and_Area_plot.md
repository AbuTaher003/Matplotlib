## Stack and Area Plot
 
```python
import matplotlib.pyplot as plt

x = [1, 2, 3, 4, 5]
area1 = [2, 4, 3, 4, 5]
area2 = [1, 3, 2, 5, 4]
area3 = [2, 3, 5, 4, 1]

# Create a stack plot
plt.stackplot(
    x, area1, area2, area3,
    colors=['r', 'g', 'm'],  # Specify colors for the areas
    labels=["area1", "area2", "area3"],  # Labels for the areas
    baseline="zero"  # Baseline type: "zero", "sym", or "wiggle"
)

# Add legend, labels, and title
plt.legend()
plt.xlabel("X - axis")
plt.ylabel("Y - axis")
plt.title("Stack Plot and Area plot")

# Display the plot
plt.show()
```

### Notes : 
- The `colors` parameter accepts a list of colors corresponding to each area, e.g., `['r', 'g', 'm']`.
- The `labels` parameter requires a list of labels for the areas, e.g., `["area1", "area2", "area3"]`.
- `baseline="zero"` keeps the baseline at the zero level. Alternative options are:
  - `"sym"`: Creates a symmetric plot around a central axis.
  - `"wiggle"`: Adjusts the baseline to minimize wiggles or undulations.
