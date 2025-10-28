```python
import os
os.chdir("D:\\")
file = open("HALO.txt","r")
s = file.read()
print(s)
file.close()
```

# Read
- `open(<file name>,"r")` : The reader will move to the beginning of the file
- `open(<file name>,"w")` : Open, delete all information already in the file. If the file does not exist, the command will create an empty text file.
```python
>>>file = open("HALO.txt", "r")
>>>content = file.read()
>>>print(content)
Hi, nice to meet you
>>>content = file.read()
>>>content
' '
>>>file.close()
```

- `read()` always reads data from the reading position onwards,  the second time the reader is at the end of the file so there is no data to read.
- `tell()` indicate the current position of the reader from the beginning of the file.
```python
>>>f = open("HALO.txt", "r")
>>>f.tell()
0
>>>all = f.read()
>>>f.tell()
68
>>>f.close()
```


## readline()
```txt
`=)))`
`:)))`
```

```python
>>> f = open("HALO.txt", "r")
>>> l = f.readline()
>>> l
'=)))\n'

>>> l = f.readline()
>>> l
':)))\n'
```

## readlines()
```python
>>> import os
>>> os.chdir("D:\\")
>>> f = open("HALO.txt")
>>> a = f.readlines()
>>> a
['Hi\n', 'Nice to meet you\n']
>>> for l in a:
...  print(l, end = " ")

Hi
Nice to meet you
```

# Write
```python
>>>import os
>>>os.chdir("G:\\")
>>>f = open("Hi.txt", "w")

>>>m1 = "Hi \n"
>>>m2 = "Nice to meet you \n"
>>>f.write(m1)
>>>f.write(m2)

>>>f.close()
Hi
Nice to meet you
```

##  writelines()
```python
import os
os.chdir("D:\\")
f = open("Hi.txt", "w")
m1 = "Hi"
m2 = "Nice to meet you"
A = [m1,m2]
f.writelines(A)
f.close()
```

# Delete
```python
import os
os.remove("text.txt")
```