```python
import matplotlib
import matplotlib.pyplot as plt
```

# Plotting
Drawing points (markers) in a diagram.  Drawing a line from point to point.
```python
import matplotlib.pyplot as plt  
import numpy as np  
  
x = np.array([1, 2, 6, 8])
y = np.array([3, 8, 1, 10])
  
plt.plot(x, y) # With Line
plt.plot(x, y, 'o') # Without Line

plt.show()
```

# Marker & Line
```python
plt.plot(ypoints, 'o:r', ms = 20, mec = 'r', mfc = 'r', lw = '20.5')
```
- `ms`: Marker size
- `mec`, `mfc`: Marker color
- `lw`: Line Width

| Marker | Description    |
| ------ | -------------- |
| 'o'    | Circle         |
| '*'    | Star           |
| '.'    | Point          |
| ','    | Pixel          |
| 'x'    | X              |
| 'X'    | X (filled)     |
| '+'    | Plus           |
| 'P'    | Plus (filled)  |
| 's'    | Square         |
| 'D'    | Diamond        |
| 'd'    | Diamond (thin) |
| 'p'    | Pentagon       |
| 'H'    | Hexagon        |
| 'h'    | Hexagon        |
| 'v'    | Triangle Down  |
| '^'    | Triangle Up    |
| '<'    | Triangle Left  |
| '>'    | Triangle Right |
| '1'    | Tri Down       |
| '2'    | Tri Up         |
| '3'    | Tri Left       |
| '4'    | Tri Right      |
| '\|'   | Vline          |
| '_'    | Hline          |

## Line Reference

| Line Syntax | Description        |     
| ----------- | ------------------ | 
| '-'         | Solid line         |     
| ':'         | Dotted line        |     
| '--'        | Dashed line        |     
| '-.'        | Dashed/dotted line |     

## Color Reference

| Color Syntax |         |     
| ------------ | ------- | 
| 'r'          | Red     |     
| 'g'          | Green   |    
| 'b'          | Blue    |    
| 'c'          | Cyan    |     
| 'm'          | Magenta |     
| 'y'          | Yellow  |     
| 'k'          | Black   |     
| 'w'          | White   |     

# Labels
```python
font1 = {'family':'serif','color':'blue','size':20}  
  
plt.title("Name_0", fontdict = font1, loc = 'left')  
plt.xlabel("Name_1")  
plt.ylabel("Name_2")
```

# Grid
```python
plt.grid(axis = 'x', color = 'green', linestyle = '--', linewidth = 0.5)
```

# Subplot
```python
#plot 1:  
x = np.array([0, 1, 2, 3])  
y = np.array([3, 8, 1, 10])  
  
plt.subplot(1, 2, 1)  # The figure has 1 row, 2 columns, and this plot is the _first_ plot.
plt.plot(x,y)  
  
#plot 2:  
x = np.array([0, 1, 2, 3])  
y = np.array([10, 20, 30, 40])  
  
plt.subplot(1, 2, 2)  # The figure has 1 row, 2 columns, and this plot is the _second_ plot.
plt.plot(x,y)  

plt.suptitle("MY SHOP")  # Super title
plt.show()
```

# Scatter
The `scatter()` function plots one dot for each observation. It needs two arrays of the same length, one for the values of the x-axis, and one for values on the y-axis
```python
x = np.array([5,7,8,7,2,17,2,9,4,11,12,9,6])  
y = np.array([99,86,87,88,111,86,103,87,94,78,77,85,86])  
colors = np.array(["red","green","blue","yellow","pink","black","orange","purple","beige","brown","gray","cyan","magenta"])
  
plt.scatter(x, y, c=colors, s=sizes, alpha=0.5, cmap='nipy_spectral')
plt.show()
```

Color map
```python
colors = np.array([0, 10, 20, 30, 40, 45, 50, 55, 60, 70, 80, 90, 100])  
plt.scatter(x, y, c=colors, cmap='available-color-map-name')  
plt.colorbar()
```

# Bars & Histograms & Pie Charts
```python
plt.bar(x,y, color = 'blue', width = '0.1') #barh() for Horizontal; height = '0.1'
```

```python
plt.hist(x)
```

```python
y = np.array([35, 25, 25, 15])  
mylabels = ["Apples", "Bananas", "Cherries", "Dates"]  
myexplode = [0.2, 0.1, 0.1, 0.1]  
mycolors = ["r", "y", "b", "g"]
  
plt.pie(y, labels = mylabels, startangle = 90, explode = myexplode, shadow = True, color = mycolor, )
plt.legend(title = "Four Fruits:")
plt.show()
```