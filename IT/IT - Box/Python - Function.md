1. Void Function
```python
def <name>(<n>):
	<code>
```
2. Function with a return value
```python
def<name>(<n>):
   <code>
   return<value>
   <code>
```

# Actual & Optional parameters
```python
def x(x, y = 2):
    return x**y
>>> x(5)
25
>>> x(5, y = 3)
125
```

## Positional-Only and Keyword-Only
```python
def ten_ham(pos_only, /, standard, *, kwd_only):
    pass
```
- `pos_only`: Bắt buộc truyền theo vị trí (trước `/`).
- `standard`: Có thể truyền theo vị trí HOẶC từ khóa (ở giữa `/` và `*`).
- `kwd_only`: Bắt buộc truyền theo từ khóa (sau `*`).

# Lambda
```python
cal = lambda x,y: x*x + y*y
>>> cal(1,2)
5
```

# *args and **kwargs

By default, a function must be called with the correct number of arguments.
However, sometimes you may not know how many arguments that will be passed into your function.

## Arbitrary Arguments 
=> Function will receive a [[Python - Tuple|tuple]] of arguments
```python
def my_function(*args):  
	print("Type:", type(args))  
	print("First argument:", args[0])  
	print("Second argument:", args[1])  
	print("All arguments:", args)  
my_function("Emil", "Tobias", "Linus")
"""
Type: <class 'tuple'>  
First argument: Emil  
Second argument: Tobias  
All arguments: ('Emil', 'Tobias', 'Linus')
"""
```
```python
def my_function(greeting, *names):  
	for name in names:  
		print(greeting, name)  
my_function("Hello", "Emil", "Tobias", "Linus")
```

## Arbitrary Keyword Arguments
=> Function will receive a [[Python - Dictionary|dictionary]] of arguments
```python
def my_function(**myvar):  
	print("Type:", type(myvar))  
	print("Name:", myvar["name"])  
	print("Age:", myvar["age"])  
	print("All data:", myvar)  
  
my_function(name = "Tobias", age = 30, city = "Bergen")
```
```python
def my_function(username, **details):  
	print("Username:", username)  
	print("Additional details:")  
	for key, value in details.items():  
		print(" ", key + ":", value)  
my_function("emil123", age = 25, city = "Oslo", hobby = "coding")
```

# Decorators
A Decorator is a function that takes another function as input and returns a new function
```python
def func1(<n>):  
	...
@decorator_name_1(<n>) # Decorator With Arguments
@decorator_name_2 # Multiple Decorators 
def func2(<n>):  
	 ... 
```

## Preserving Function Metadata
```python
import functools  
  
def func_1(func):  
	@functools.wraps(func) # Without: Return `func_2`
	  def func_2():  
		....
	  return <value>  
  
@decorator_name  
def myfunction():  
	  ...
print(myfunction.__name__) # Return: `myfunction`
```

# Generator Function
Function can be use many times
```python
def OddNum(n):
	for i in range(n):
		yield 2*i + 1
```

## next() & send() & close()
```python
next(x) # Manually iterate through a generator
x.send("World") # Allows you to send a value to the generator
x.close() # Stops the generator
```