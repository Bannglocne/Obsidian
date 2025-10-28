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

```python
myfamily = {  
	"child1" : {  
		"name" : "Emil",  
		"year" : 2004  
	},  
	"child2" : {  
		"name" : "Tobias",  
		"year" : 2007  
	},  
}
```

##  keys() & values() & items()
```python
>>> for k in s.keys():
>>> for k in s.values():
>>> for i,k in s.items():
```

##  update()
```python
>>> T = {'Maths': 10, 'Biology': 8}
>>> h.update(T)
>>> h_copy = h.copy()
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

## Remove
```python
>>> A = {"Name":"A", "Age":"18", "Car":"Maybach"}
>>> del A["name"]
>>> A.pop("Age") # A.popitem()
```
- Clear all: `<dict object>.clear()`
- Delete Dict: `del <dict object>`