# For Loop
```python
>>> for i in range([<start>],<end>,[<increment>]:
      <code>
```

# If Condition
```python
if <condition>:
	<code>
else if <condition2>:
	<code>
else:
	<code
```

# While Loop
```python
while <condition>:
	<code>
else:
   <code>
```

# Break & Continue
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

# short-circuit operator
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


