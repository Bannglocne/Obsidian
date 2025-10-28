```python
a = [1]
a.append([0,1])
>>> a
[1,[0,1]]
>>> a[1][0]
0
```

# Matrix description in Python
```python
a = []
m = int(input("Enter the number of rows of the matrix: "))
n = int(input("Enter the number of columns of the matrix: "))
for i in range(m):
    print("Prepare to enter the ", i + 1, "th row:")
    b = []
    for j in range(n):
        x = int(input("Enter the " + str(j + 1) + "th element : "))
        b.append(x)
    a.append(b)
    
# Print Matrix
for i in range(m):
    for j in range(n):
        print(a[i][j], end=" ")
    print()
```

# Structured Data
```python
A = [["A", [1,2,3],[4,5,6]],["B",[2,3,4],[4,5,6]]]
for name,score1,score2 in A:
    print(name)
    print("    Midterm exam test: ", end = " ")
    for score in score1:
        print(score, end="  ")
    print()
    print("    Final exam test: ", end = " ")
    for score in score2:
        print(score, end="  ")
    print()
```

# Slicing
```python
newlist = A[<start>:<stop>:<increment>]
```

```python
>>> a = [0,1,2,3,4,5]
>>> a[0:2] = "a","b"
>>> a
["a","b",2,3,4,5]


>>> a[-6: -1] # == a[0:5] == a[0:-1]
["a","b",2,3,4,5]

>>>a[-1:0] # == a[5:0] == a[-1:-6]
[]
```

```python
>>>a = [1,2,3,4,5]
>>>a[0:4:2]
[1,3,5]

>>>a[ : : -1]
[5,4,3,2,1]

>>>a[0:5:-1]
[]

>>>a[ : : 2] = [1,1,1] #Assign directly to [1,1,1]
[1,2,1,4,1]
```

# List Parameter Binding
`x = [1,5,"HB"]`
![[NameSpace_1.png]]
`y = x`
![[NameSpace_2.png]]
`x[0] = 10`
![[NameSpace_3.png]]
`y[1] = [1,1]`
![[NameSpace_4.png]]
`x = 'One'`
![[NameSpace_5.png]]

# List Comprehension
```python
>>>x = [1,2,3,4,5,6,7,8,9,10]
>>>y = [i * i for i in x]
>>>y
[1,4,9,16,25,36,49,64,81,100]
```

# Quickly create Sequential data
```python
<generator> = (<biểu thức> for <tham biến> in <interator>)
```

==Note==: The object of the above sequential data type can only generate data once.
```python
>>> a = (2*i + 1 for i in range (10))
>>> type(a)
<class 'generator'>

>>> for k in a:
   print(k, end = " ")
1 3 5 7 9 11 13 15 17 19
```