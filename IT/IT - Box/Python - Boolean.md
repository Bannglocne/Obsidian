```python
>>> x = 1 > 2
>>> bool(x)
False
```

```python
>>> A = []
>>> bool(A)
False
>>> A.append(5)
>>> bool A
True
>>> bool (12 and [1,2,3])
True
>>> bool (33 and "")
False
```

# Comparison
```python
>>> a,b,c = 1,2,3
>>> 3 >= c > 2 > b >= 1 >= a
False
```

```python
def nhuan(n):
	if n % 400 == 0 (n % 4 == 0 and n % 100 != 0):
		return True
	else:
		return False
```


	# in Operator
```python
>>> A = [1,2,3,4]
>>> b = 0 in A
>>> b
False

>>> 0 in range(10)
True
```