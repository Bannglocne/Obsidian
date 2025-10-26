Can be numbers, logicals, strings, or tuples, but cannot be lists, dic, or sets.
```python
>>> A = {1,2,3,"One"}
>>> type(A)
<class 'set'>
```

Elements cannot overlap
```python
>>> D = {1,2,1,2}
>>> D
{1,2}
```

## `set()`
```python
>>> s = 'abcdef'
>>> S = set(s)
>>> S
{'c', 'a', 'f', 'd', 'e', 'b'}

>>> d = {1:"Bình", 2:"Dương"}
>>> set(d)
{1, 2}

>>> A = [1,2,3,4,5,6,7,8,9,10]
>>> B = [1,4,8,32,21]
>>> S = {x for x in A if x not in B}
>>> S
{2, 3, 5, 6, 7, 9, 10}
```



## add()

```python
>>>A = set()
>>>A.add("a")
>>>A
{"a"}
```

## remove()
```python
>>>A = {1,2,(1,3)}
>>>A.remove(2)
>>>A
{1,(1,3)}
```

==Note==: **set** follows the naming method [[Python - List of list#Giải thích liên kết tham chiếu list| Namespace]] like list or dic.
	- `C = A`:  A and C point to a single object in the set. Therefore, after adding an element to A, C is still A
	- `B = A.copy()`: A and B point to different objects. Therefore, when A changes, B remains the same

## clear()
```python
>>>A = {1,234,12,43,(1,23),"Chào"}
>>>A.clear()
>>>A
set()
```

# Operations on sets

## Relationship
```python
>>>A = {(1,2),2,3,"One"}
>>>2 in A
True
>>>B = {(1,2), "One"}
>>>B.issubset(A)
True
>>>A.issuperset(B)
True
```

## union() or (|)
```python
>>> A = {1,23,4,5}
>>> B = {1,4,22,5}
>>> A | B
{1, 4, 5, 22, 23}
```

## intersection() or (&)
```python
>>> A = {1,23,4,5}
>>> B = {1,4,22,5}
>>> A & B
{1, 4, 5}
```

## difference() or (-)
```python
>>> A = {1,23,4,5}
>>> B = {1,4,22,5}
>>> A - B
{23}
>>> B - A
{22}
```

## symetric_differemce() or (^)
```python
>>> A = {1,23,4,5}
>>> B = {1,4,22,5}
>>> A^B
{22, 23}
```