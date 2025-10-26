Function inside itself
```python
>>> def rc1(n):
   print("Next:",n)
   rc1(n+1)
   print("Stop")
```

**Fibonaci**
```python
def fi(n):
   if n == 1:
      return 1
   elif n == 2:
      return 1
   else:
      return fi(n-1) + fi(n-2)
```

**Calculate factorial of  numbers**
```python
def fac(n):
   if n == 0:
      return 1
   else:
      return n*fac(n-1)
```

# Applications of Recursion
**Merge Sort**
```python
def merge(right, left):
    kq = []
    while left != [] and right != []:
        if len(left) > 0 and len(right) > 0:
            if left[0] < right[0]:
                kq.append(left[0])
                left = left[1:]
            else:
                kq.append(right[0])
                right = right[1:]
        if len(left) == 0:
            kq.extend(right)
            break
        if len(right) == 0:
            kq.extend(left)
            break
    return kq
  

def merge_sort(A):
    if len(A) <= 1:
        return A
    left = A[:len(A) // 2]
    right = A[len(A)//2:]
    sortedleft = merge_sort(left)
    sortedright = merge_sort(right)
    return merge(sortedleft,sortedright)
```

**Quick sort**
```python
def Partition(A,p,r):
    pivot = A[r]
    i = p - 1
    for j in range(p,r):
        if A[j] < pivot:
            i = i + 1
            A[i],A[j] = A[j],A[i]
    if A[i+1] > A[r]:
        A[i + 1],A[r] = A[r],A[i+1]
    return i + 1
  

def QuickSort(A,p,r):
    if p < r:
        q = Partition(A,p,r)
        QuickSort(A,p,q-1)
        QuickSort(A,q+1,r)
```

**Minimal Change Algorithm**
```python
def insertNum(n,A,k):
    newlist = []
    if k == 0:
        newlist = [n] + A
    elif k == len(A) + 1:
        newlist = A + [n]
    else:
        newlist = A[:k] + [n] + A[k:]
    return newlist
def insertALL (n,A):
    newlist = []
    for k in range(len[A] + 1):
        newlist.append(insertNum(n,A,k))
    return newlist
def permutation(n):
    if n == 1:
        return [[1]]
    elif n == 2:
        return [[1,2],[2,1]]
    else:
        new = []
        A = permutation(n-1)
        for pe in A:
            new = new + insertALL(n,pe)
        return new
```