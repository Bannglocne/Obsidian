Storing multiple items in a single variable.
Unchangeable
```python
thistuple = ("apple",)  # Tuple
thistuple = ("apple") # NOT a Tuple
```

=> Change Tuple Items
```python
y = list(x)  
# Change Values / Add Items / Remove Items
x = tuple(y)
```

# Unpack Tuples
```python
fruits = ("apple", "banana", "cherry", "strawberry", "raspberry")  
(a, *b, c) = fruits  
```