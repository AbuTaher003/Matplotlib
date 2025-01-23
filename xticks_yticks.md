# Matplotlib Axis Customization Notes

This note discusses various methods for customizing the x-axis and y-axis in Matplotlib. The code and its explanations are provided together for easy understanding.

```python
import matplotlib.pyplot as plt

x = [1, 2, 3, 4]
y = [3, 2, 4, 3]

plt.plot(x, y)

# Use plt.xticks() to set index numbers on the x-axis based on the x values.
plt.xticks(x)

# Use plt.yticks(x) to set index numbers on the y-axis similar to x values.

# Use plt.xticks() to set custom labels on the x-axis. Example:
# plt.xticks(x, labels=["python", "c", "c++", "java"])

# Use plt.xlim() and plt.ylim() to expand the axis limits.
# plt.xlim(0, 10)
# plt.ylim(0, 10)

# Use plt.axis() to set axis limits for both x and y at the same time. Example:
# plt.axis([0, 10, 0, 7])

plt.show()
```

### Code Explanation:
1. **plt.xticks(x):**
   This sets index numbers on the x-axis based on the x values.

2. **plt.yticks(x):**
   This sets index numbers on the y-axis similar to the x values.

3. **Custom Labels:**
   `plt.xticks(x, labels=["python", "c", "c++", "java"])` sets custom labels on the x-axis.

4. **Axis Limits:**
   - `plt.xlim(0, 10)` sets the x-axis limit from 0 to 10.
   - `plt.ylim(0, 10)` sets the y-axis limit from 0 to 10.

5. **Combined Axis Limit:**
   `plt.axis([0, 10, 0, 7])` sets limits for both x and y axes at the same time.

### Output
Running this code will display a line graph plotted according to the x and y values. Additionally, the xticks and axis limits can be customized.

