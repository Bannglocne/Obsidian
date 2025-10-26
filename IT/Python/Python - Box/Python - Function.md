# Void Function
```python
def <name>(<n>):
	<code>
```

# Function with a return value
```python
def<name>(<n>):
   <code>
   return<value>
   <code>
```

# Actual & Optional parameters
```python

def f(x,y):
    return x*y + x - y
>>> f(y=5,x=2)
7

def x(x, y = 2):
    return x**y
>>> x(5)
25
>>> x(5, y = 3)
125
```

# Lambda
```python
cal = lambda x,y: x*x + y*y
>>> cal(1,2)
5
```