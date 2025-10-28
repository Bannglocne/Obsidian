```python
>>>a = [1,2,3,4,5] 

>>> a[1:3] = [10,11,12]
>>> a
[1,10,11,12,4,5]
```

## List Methods
- `len(a)`: Count length
- `del a[i]`: Delete element
- `a.append(<object>)`: Add a new object at the end as an element [^1]
- `a.clear()`: Delete all
- `a.count(<value>)`: Count the number of occurrences of an element 
- `b = a.coppy()`: Returns another list with the same values ​​as the first list. Or `b = list(a)`
- `a.extend()`: Expand, add object to the end of the list as a natural expansion [^1]
- `k = a.index(<giá trị>)`: Returns the first index in the list of values
-  `a.insert(index, <object>)`: Insert object to list at index
- `x = a.pop()`: Remove and retrieve the last element of the list
- `a.remove(<value>)`: Deletes the first element with the mentioned value
- `a.reverse`: Reverse the order 
- `a.sort()`: Re-arrange the list in ascending order

**Customize Sort Function**
```python
def myfunc(n):  
	return abs(n - 50)  
  
thislist = [100, 50, 65, 82, 23]  
thislist.sort(key = myfunc)  
print(thislist)
```








# Looping
```python
for x in myList:

for i in range(len(myList)):

while i < len(myList):
	  print(thislist[i])
	  
[print(x) for x in myList]
```

# Comprehension
```python
newlist = [expression for item in iterable if condition == True]
```

# Join Lists
```python
list3 = list1 + list2

for x in list2:
	list1.append(x)
	
list1.extend(list2)
```
# Range function
```python
n = 20
list(range(0,n,2))
[0,2,4,,6,8,10,12,14,16,18]
```

---
[^1]: With `append()` the object can be of any type, but with `extend()` the object must be of a sequential type.
