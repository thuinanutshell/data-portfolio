a compilation of useful code for data visualization in python : ) 
## Numpy
- `df.shape[0]` returns an integer that represents the total number of rows
- `df.shape[1]` returns an integer that represents the total number of columns
- `np.arange({integer})` returns an array of evenly spaced values within a given interval
## Matplotlib
### One Direction (1D)
```python
# Vertically stacked subplots
fig, axs = plt.subplots(2)
fig.suptitle('title')
axs[0].plot(x, y) # The first row
axs[1].plot(x, -y) # The last row

# Or
fig, (ax1, ax2) = plt.subplots(2, sharex=True) # if two plots share the same x-axis
ax1.plot(x,y)
ax2.plot(x,-y)
```
```python
# Horizontally stacked subplots
fig, (ax1, ax2) = plt.subplots(1, 2) # 1 row and 2 columns
fig.suptitle('title')
ax1.plot(x, y)
ax2.plot(x, -y)
```
### Two Directions (2D)
```python
fig, axs = plt.subplots(2, 2) # 2 rows and 2 columns
axs[0, 0].plot(x, y) # first plot of row 0 (first row) and column 0 (first column)
axs[0, 1].plot(x, y) # second plot of row 0 (first row) and column 1 (second column)
axs[1, 0].plot(x, y) # third plot of row 1 (second row) and column 0 (first column)
axs[1, 1].plot(x, y) # fourth plot of row 1(second row) and column 1 (second column)

# Or (notice how they all share the same x)
fig, ((ax1, ax2), (ax3, ax4)) = plt.subplots(2, 2)
ax1.plot(x,y)
ax2.plot(x, y**2)
ax3.plot(x, -y)
ax4.plot(x, -y**2)
```
