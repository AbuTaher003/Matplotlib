# Bar Plot using Matplotlib

## Introduction

This guide demonstrates how to create a bar plot using Matplotlib. Bar plots are used to represent categorical data with rectangular bars where the length of each bar is proportional to the value it represents.

---

## Code Explanation

Here is the code to create a bar plot:

```python
import matplotlib.pyplot as plt

# Data for the bar plot
x = ["python", "C", "C++", "Java"]
y = [90, 70, 40, 80]
c = ['r', 'y', 'g', 'b']

# Creating the bar plot
plt.bar(x, y, color=c, width=0.4, edgecolor='r', linewidth=5, alpha=1, label="popularity")

# Adding labels, title, and legend
plt.xlabel("Language", fontsize=15)
plt.ylabel("No.", fontsize=15)
plt.title("Popularity of Language", fontsize=20)
plt.legend()

# Displaying the plot
plt.show()
```

### Key Points:
- **`plt.bar(x, y, ...)`**: Creates a bar plot where `x` represents the categories and `y` represents the values.
- **Colors and Styling**: The bars are styled with specific colors (`c`), edge color, and line width.
- **Labels and Title**: Axis labels and the plot title are added using `plt.xlabel()`, `plt.ylabel()`, and `plt.title()`.
- **Legend**: A legend is added with `plt.legend()` to describe the data.

---

## Output

Below is the generated bar plot:

![Bar Plot](popularity_of_languages.png)

---

## Notes
- Ensure Matplotlib is installed in your environment using:

  ```bash
  pip install matplotlib
  ```

- You can modify the data (`x` and `y`) to create bar plots for other datasets.

---

Happy plotting with Matplotlib!

