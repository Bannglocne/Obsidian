```python
>>> str (5)
>>> '5'

>>> str(divmod(19,5))
'(3,4)'
```

**Escape Character**

| Code | Result          | 
| ---- | --------------- | 
| \'   | Single Quote    |        
| \\   | Backslash       |        
| \n   | New Line        |        
| \r   | Carriage Return |        
| \t   | Tab             |        
| \b   | Backspace       |        
| \f   | Form Feed       |        
| \ooo | Octal value     |        
| \xhh | Hex value       |        

# ASCII & Unicode
```python
>>>ord("A")
65
>>>chr("Ẩ")
7848
```

# Adjusting & Aligning Character

| Function     | Example                         |
| ------------ | ------------------------------- |
| upper()      | NGUYEN XUAN LOC                 |
| lower()      | nguyen xuan loc                 |
| capitalize() | Nguyen xuan loc                 |
| title()      | Nguyen Xuan Loc                 |
| swapcase()   | nGUYEN xUAN lOC                 |
| strip()      | Remove start and end whitespace | 
| lstrip()     | Remove start whitespace         |
| rstrip()     | Remove end whitespace           |

# Methods

| Methods                    | Description                                                                     |
| -------------------------- | ------------------------------------------------------------------------------- |
| `len(txt)`                 | Length                                                                          |
| `txt[1,2]`                 | Slicing (Use negative indexes to start the slice from the end)                  |
| `"a" is not in txt`        | Check if not                                                                    |
| `for i in "txt"`           | Looping through                                                                 |
| `txt.count("a",start,end)` | Count the number of occurrences of a character                                  |
| `txt.find()`               | Find the index of first string <br>Return `-1` if not found                     |
| `txt.index()`              | Find the index of first string <br>Return [[Python - Bug\| Error]] if not found |
| `txt.replate("a","A",n)`   | Replace "a" by "A"  n times <br>`-1`: No limited                                |
| `s.split()`                | Split the original string into multiple substrings                              |
| `s.join()`                 | Join two or more strings                                                        |


**Count**
```python
>>>s = "00001111"
>>>s[0:5].count("1")
1
```
**Split and Join**
```python
>>> s = "Bạn    Lộc đẹp trai           vch  "
>>> s.split()
['Bạn', 'Lộc', 'đẹp', 'trai', 'vch']
>>> a = s.split()
>>> " ".join(a)
'Bạn Lộc đẹp trai vch'

>>> s.split(" ")
['Bạn', '', '', '', 'Lộc', 'đẹp', 'trai', '', '', '', '', '', '', '', '', '', '', 'vch', '', '']
>>> s.split(maxsplit = 4)
['Bạn', 'Lộc', 'đẹp', 'trai', 'vch  ']
>>> s.split(" ", 4)
['Bạn', '', '', '', 'Lộc đẹp trai           vch  ']
```
**Concatenation**
```python
a = "Hello"; b = "World"  
c = a + b  
```

# Format 
```python
>>> age = 18  
>>> txt = f"My name is Loc, I am {age}"

>>>s = "Hello {} and {}"
>>>s.format("A", "B")
Hello A and B

>>>s = "{1} is my name"
>>>a = Loc
>>>print(s.format(a))
Loc is my Name
```

## Field Command
![[Python_Field.png]]

```python
>>> s = "a = {:4}, b = {:4}, c =  {:4}" # Width
>>> s.format(1,2,3)
'a =    1, b =    2, c =     3' 
```

```python
>>>s = "{0:<10} {0:=10} {0:^10} {0:>10}" # <: Right; >: Left; =: 2 side; ^: Center
>>>print(s.format(123))
123               123    123            123 
```

```python
>>> s = "{0:-<10} {0:*^10} {0:->10}" # Fill whitespace
>>> s.format(123)
"123------- ***123**** -------123"
```

```python
>>>import math as x
>>>s = 'Số pi: {:.3}, số e: {:.3}' # Approximate number
>>>print(s.format(x.pi, x.e))
Số pi: 3.14, số e: 2.72
```

```python
>>>s = " {:#10.5}" # Add 0 to have x length
>>>s.format(0.4)
'    0.40000'
```

```python
>>> s = "{0:b} {0:c} {0:d} {0:e} {0:f} {0:g}" # b:binary; c: ASCII or Unicode; d: interger; f: decimal; e: e+; g: most general form
>>> s.format(65)
'1000001 A 65 6.500000e+01 65.000000 65'
```

```python
>>>s = "{0:,.5e} {0:,.5f}" # , every 3 number
>>>s.format(1112233114313.23311)
'1.11223e+12 1,112,233,114,313.23315'
```