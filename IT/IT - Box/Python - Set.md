 _unordered_, _unchangeable*_, and _unindexed_.
 **Duplicates Not Allowed**
 ```python
thisset = {"apple", "banana", "cherry", True, 1, 2}  
print(thisset) # {True, 2, 'banana', 'cherry', 'apple'}
 ```

# Methods
- `add()`: Add one item to a set
- `update()`:  Add items from another set into the current set
- `remove()` / `discard()`: `discard()` won't raise an error if the item to remove doesn't exist
- `pop()`: Remove a random item 
- `clear()`: Remove all items
- `del`: Delete the set

```python
mySet = set1 | set2 | set3
mySet = set1 & set2 & set3
mySet = set1 - set2
mySet = set1 ^ set2
```

# Frozenset
```python
x = frozenset({"apple", "banana", "cherry"})
```
| Method                 | Shortcut   | Description                                                      |
| ---------------------- | ---------- | ---------------------------------------------------------------- |
| copy()                 |            | Returns a shallow copy                                           |
| difference()           | `-`        |                                                                  |
| intersection()         | `&`        |                                                                  |
| isdisjoint()           |            | Returns whether two frozensets have an intersection              |
| issubset()             | `<=` / `<` | Returns True if this frozenset is a (proper) subset of another   |
| issuperset()           | `>=` / `>` | Returns True if this frozenset is a (proper) superset of another |
| symmetric_difference() | `^`        |                                                                  |
| union()                | \|       |                                                                  |