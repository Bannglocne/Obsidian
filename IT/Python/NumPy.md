#python #library #database 
```python
import numpy as np
print(np.__version__)
```

# Arrays
## Dimensions
```python
arr = np.array(1) # 0-D

arr = np.array([1, 2]) # 1-D
print(arr[1])

arr = np.array([[1, 2, 3, 4, 5], [6, 7, 8, 9, 10]]) # 2-D
print(arr[0, 1])
print(arr[0:2, 1:4])

arr = np.array([[[1, 2], [3, 4]], [[5, 6], [7, 8]]]) # 3-D
print(arr[0, 1, 2])

arr = np.array([1, 2], ndmin=5) # Higher Dimensional Arrays
```

```python
print(arr.array) # Checking dimensions
```

## Data Types
- `i` - integer
- `b` - boolean
- `u` - unsigned integer
- `f` - float
- `c` - complex float
- `m` - timedelta
- `M` - datetime
- `O` - object
- `S` - string
- `U` - unicode string
- `V` - fixed chunk of memory for other type ( void )

**Creating arrays with a defined data type and size**
```python
arr = np.array([1, 2, 3, 4], dtype='i4')
```

## Copying & View
```python
x = arr.view() #  Just a view of the original array
y = arr.copy() # New array, owns the data

# Check if an array owns it's data or not
print(x.base)
print(y.base)
```

## Shape
The number of elements in each dimension.
```python
arr = np.array([[1, 2, 3, 4], [5, 6, 7, 8]])    
print(arr.shape) # (2, 4) : The array has 2 dimensions, where the first dimension has 2 elements and the second has 4.
```
**Reshape**
```python
arr = np.array([1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12])
newarr = arr.reshape(2, 3, 2)

'''
1-D to 3D [[[ 1  2][ 3  4][ 5  6]] [[ 7  8][ 9 10][11 12]]]
Is a view
(2, 3, -1): Numpy will automatic calculate the last number
'''

newarr = arr.reshape(-1) # Flattening the arrays
```

## Iterating
```python
for x in arr:  
	for y in x:  
		for z in y:  
			...
# Or 
for x in np.nditer(arr):
```

**Different Data Types**
```python
for x in np.nditer(arr, flags=['buffered'], op_dtypes=['S']):  
```

**Different Step Size**
```python
for x in np.nditer(arr[:, ::2]):  
```

**Enumerated Iteration**
```python
for idx, x in np.ndenumerate(arr):
```

## Joining
```python
np.array([1, 2, 3])  
np.array([4, 5, 6])
np.stack((arr1, arr2), axis=1) # Axis:  [[1 4] [2 5] [3 6]]
np.hstack((arr1, arr2)) # Along rows: [1,2,3,4,5,6]
np.vstack((arr1, arr2)) # Along columns: [[1,2,3], [4,5,6]]
np.dstack((arr1, arr2)) # Along depth: [[1,4], [2,5], [3,6]]
```

## Slpitting
```python
arr = np.array([1, 2, 3, 4, 5, 6])  
  
newarr = np.array_split(arr, 4)
print(newarr) # [array([1, 2]), array([3, 4]), array([5]), array([6])]
print(newarr[0]) # [1,2]
print(newarr[1]) # [3,4]
print(newarr[2]) # [5,6]
```
Can use `hsplit()`, `vsplit()`, `dsplit()`

## Search
```python
arr = np.array([1, 2, 3, 4, 5, 4, 4])
x = np.where(arr == 4) # (array([3, 5, 6]),)
x = np.searchsorted(arr, 3, side="right") # 4 
```

```python
arr = np.array([1, 3, 5, 7])
x = np.searchsorted(arr, [2, 4, 6]) # Return indexes where 2,4,6 should be inserted in the original array to maintain the order: [1 2 3]
```

## Sort
```python
np.sort(arr)
```

## Filter 
Getting some elements out of an existing array and creating a new array out of them
```python
arr = np.array([41, 42, 43, 44])
x = [True, False, True, False]

newarr = arr[x] # [41, 43]
```

```python
arr = np.array([41, 42, 43, 44])
filter_arr = arr > 42

newarr = arr[filter_arr]
```

_Example:_
```python
import numpy as np
arr = np.array([1, 2, 3, 4, 5, 6, 7])

filter_arr = []

for element in arr:
	if element % 2 == 0:
		filter_arr.append(True)
	else:
		filter_arr.append(False)
newarr = arr[filter_arr]

print(filter_arr) # [False, True, False, True, False, True, False]
print(newarr) # [2 4 6]
```

# Random
## Create random
```python
random.randint(100) # Random Number
random.rand() # Random float between 0 and 1

random.randint(100, size=(5)) # 1-D array containing 5 random integers
random.randint(100, size=(3, 5)) # 2-D array with 3 rows, each row containing 5 random integers

random.rand(5) # 1-D array containing 5 random floats
random.rand(3, 5) # 2-D array with 3 rows, each row containing 5 random numbers

random.choice([3, 5, 7, 9]) # Return one of the values in an array
random.choice([3, 5, 7, 9]) # 2-D array that consists of the values in the array parameter (3, 5, 7, and 9)
```

## Distribution
### Data
A list of all possible values, and how often each value occurs. _Random Distribution_: A set of random numbers that follow a certain probability density function.
```python
x = random.choice([3, 5, 7, 9], p=[0.1, 0.3, 0.6, 0.0], size=(100)) # The probability for the value
```

### Random Permutations
Re-arranged array
```python
arr = np.array([1, 2, 3, 4, 5]) 

random.shuffle(arr) # View Array
random.permutation(arr) # Copy Array
```

### Normal 
`loc` - (Mean) where the peak of the bell exists.
`scale` - (Standard Deviation) how flat the graph distribution should be.
```python
random.normal(loc=1, scale=2, size=(2, 3))
```

### Binomial 
`n` - number of trials.
`p` - probability of occurrence of each trial (e.g. for toss of a coin 0.5 each).
```python
random.binomial(n=10, p=0.5, size=10)
```
### Poisson 
`lam` - rate or known number of occurrences e.g. 2 for above problem.

```python
random.poisson(lam=2, size=10)  
```

### Uniform 
`low` - lower bound - default 0 .0.
`high` - upper bound - default 1.0.
```python
random.uniform(size=(2, 3))
```

### Logistic 
`loc` - mean, where the peak is. Default 0.
`scale` - standard deviation, the flatness of distribution. Default 1.
```python
random.logistic(loc=1, scale=2, size=(2, 3))
```

### Multinomial 
`n` - number of times to run the experiment.
`pvals` - list of probabilties of outcomes (e.g. [1/6, 1/6, 1/6, 1/6, 1/6, 1/6] for dice roll).
```python
x = random.multinomial(n=6, pvals=[1/6, 1/6, 1/6, 1/6, 1/6, 1/6])
```

### Exponential 
`scale` - inverse of rate ( see lam in poisson distribution ) defaults to 1.0.
```python
random.exponential(scale=2, size=(2, 3))
```

### Chi Square
`df` - (degree of freedom).
```python
random.chisquare(df=2, size=(2, 3))
```

### Rayleigh 
```python
random.rayleigh(scale=2, size=(2, 3))
```

### Pareto 
```python
random.pareto(a=2, size=(2, 3))
```

### 
`a` - distribution parameter.
```python
random.zipf(a=2, size=(2, 3))
```

# ufunc
```python
import numpy as np  
  
def myadd(x, y):  
	return x+y  
  
myadd = np.frompyfunc(myadd, 2, 1)  
print(myadd([1, 2, 3, 4], [5, 6, 7, 8]))
```

## Simple Arithmetic
```python
np.add(arr1, arr2)
np.subtract(arr1, arr2)
np.multiply(arr1, arr2)
np.divide(arr1, arr2)
np.power(arr1, arr2)
np.mod(arr1, arr2) # remainder()
np.divmod(arr1, arr2)
np.absolute(arr)
```

**Summations**
```python
np.sum([arr1, arr2])
np.sum([arr1, arr2], axis=1)
np.cumsum(arr)
```

**Products**
```python
np.prod(arr)
np.prod([arr1, arr2])
np.prod([arr1, arr2], axis=1)
np.cumprod(arr)
```

**Differences**
```python
newarr = np.diff(arr)
newarr = np.diff(arr, n=2)
```

**LCM & GCD**
```python
np.lcm.reduce(arr)
np.gcd.reduce(arr)
```

## Rounding Decimals
```python
np.trunc([-3.1666, 3.6667]) # Remove the decimals, and return the float number closest to zero. Can use fix()

np.around(3.1666, 2) # Increments preceding digit or decimal by 1 if >=5 else do nothing

np.floor([-3.1666, 3.6667]) # Rounds off decimal to nearest lower integer.

np.ceil([-3.1666, 3.6667]) # Rounds off decimal to nearest upper integer.
```

## Logs
```python
np.log2(arr)
np.log10(arr)
np.log(arr)
```

## Trigonometric 
```python
np.sin(np.pi/2) # sin(), cos(), tan(), sinh(), cosh(), tanh()

np.deg2rad(arr)
np.rad2deg(arr)
np.arcsin(angle) # Finding angles. arcsin(), arccos(), arctan(), arcsinh(), arccosh() and arctanh()
np.hypot(base, perp) # Pythagoras
```

## Set Operations
A collection of unique elements.

Create a Set:
```python
arr = np.array([1, 1, 1, 2, 3, 4, 5, 5, 6, 7])  
x = np.unique(arr)
```

### Finding
```python
np.union1d(arr1, arr2) # Union: The unique values of two arrays
np.intersect1d(arr1, arr2, assume_unique=True) # Intersection: The values that are present in both arrays
np.setdiff1d(set1, set2, assume_unique=True) # Difference: The values in the first set that is NOT present in the seconds set
np.setxor1d(set1, set2, assume_unique=True) # Symmetric Difference: The values that are NOT present in BOTH sets
```