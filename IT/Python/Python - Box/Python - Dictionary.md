```python
>>> person = {"Name": "A", "Age":"18"}
>>> peson
{'Name': 'A', 'Age': '18'}
>>> person["Name"]
'A'
```

```python
>>> person = {}
>>> s["Name"] = 'A'
>>> s["Age"] = '18'
>>> s
{'Name': 'A', 'Age': '18'}
```

##  keys() & values()
```python
>>> for k in s.keys():
   print(k)
Name
Age
```

```python
>>> for k in s.values():
   print(k)
A
18
```

## items()
```python
>>> for i,k in s.items():
   print(i,k)
Name A
Age 18
```

##  update()
```python
>>>h
{'Maths':9.5, 'Physics': 10, 'Biology': 6.5}
>>> T = {'Maths': 10, 'Biology': 8}
>>> h.update(T)
>>> h
{'Maths': 10, 'Physics': 10, 'Biology': 8}
```

## get()
```python
h = {'Maths': 10, 'Physics': 10, 'English': 10}
subjects = ["Maths", 'Physics', 'Chemistry', 'Biology', 'English']
for i in subjects:
    print("{:1}: {}".format(mon,h.get(mon,"Still waiting")))
Maths: 10
Physics: 10
Chemistry: Still waiting
Biology: Still waiting
English: 10
```

## del()
```python
>>> A = {"Name":"A", "Age":"18"}
>>> del A["name"]
>>> A
{'Age': '18'}
```

- Clear all: `<dict object>.clear()`