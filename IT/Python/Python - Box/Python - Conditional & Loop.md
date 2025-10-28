# Range
```python
range([<start>],<end>,[<increment>]:
```

# For Loop
```python
>>> for i in x:
      <code>
```

# If Condition
```python
if <condition>:
	<code>
else if <condition2>:
	<code>
else:
	<code>
	
# Shorthand
if <condition>: <code>
<code> if <condition> else <code>
```
**pass**: Do nothing

# Match
```python
match expression:
	case x if <condition):
		code block
	case y | z: # Combine Value
		code block
	case _: # Default Value
	    code block
```

# While Loop
```python
while <condition>:
	<code>
else:
   <code>
```

- `break`: Immediately stop current loop
- `continue`: End current loop and return to next loop
```python
c = 0
while True:
	name = input("Enter Name: ")
	if not name:
		break
	if name[0].islower():
		print("Capitalize the first letter")
		continue
	else:
		print("Name:", name)
		c = c = 1
print("You entered", c, "names")
```

# Short-circuit Logical operator
Python can quickly and accurately calculate the result of an operation without having to calculate all the parameters of the operation.

## and Operator
```python
>>> 2 and input("Nhập số")
Nhập số 3
'3'

>>> 0 and input("Nhập số:")
0

>>> x = False and print(1)
>>> x
False

>>> x = True and print(1)
1

>>> x #NoneType
>>> print(x)
None
```

## or Operator
```python
>>> print("Hi") or print(3)
Hi
3

>>> [0] or print(1)
[0]


>>> x = [0] or [1,1]
>>> x
[0]

>>> x = [] or [1,2]
>>> x
[1, 2]

>>> x = False or input("Nhập số")
Nhập số
>>> bool(x)
False

>>> x = False or input("Nhập số")
Nhập số 3
>>> bool(x)
True
```

# Iterator
An iterator is an [[Python - Object|object]] that contains a countable number of values.
```python
class MyNumbers:  
	def __iter__(self):  
		self.a = 1  
		return self  
  
	def __next__(self):  
		if self.a <= 20:  
			x = self.a  
			self.a += 1  
			return x  
		else:  
			raise StopIteration  
			
myclass = MyNumbers()  
myiter = iter(myclass)  
  
for x in myiter:  
	print(x)
```