
# Khái niệm Module
- Khái niệm: Module là một file, trong đó các lớp, hàm và biến được định nghĩa. Tất nhiên, một Module cũng có thể bao gồm code có thể chạy. (Thư viện hàm số)
```python
>>> dir(__builtins__)
['ArithmeticError', 'AssertionError', 'AttributeError', 'BaseException', 'BaseExceptionGroup', 'BlockingIOError', 'BrokenPipeError', 'BufferError', 'BytesWarning', 'ChildProcessError', 'ConnectionAbortedError', 'ConnectionError', 'ConnectionRefusedError', 'ConnectionResetError', 'DeprecationWarning', 'EOFError', 'Ellipsis', 'EncodingWarning', 'EnvironmentError', 'Exception', 'ExceptionGroup', 'False', 'FileExistsError', 'FileNotFoundError', 'FloatingPointError', 'FutureWarning', 'GeneratorExit', 'IOError', 'ImportError', 'ImportWarning', 'IndentationError', 'IndexError', 'InterruptedError', 'IsADirectoryError', 'KeyError', 'KeyboardInterrupt', 'LookupError', 'MemoryError', 'ModuleNotFoundError', 'NameError', 'None', 'NotADirectoryError', 'NotImplemented', 'NotImplementedError', 'OSError', 'OverflowError', 'PendingDeprecationWarning', 'PermissionError', 'ProcessLookupError', 'RecursionError', 'ReferenceError', 'ResourceWarning', 'RuntimeError', 'RuntimeWarning', 'StopAsyncIteration', 'StopIteration', 'SyntaxError', 'SyntaxWarning', 'SystemError', 'SystemExit', 'TabError', 'TimeoutError', 'True', 'TypeError', 'UnboundLocalError', 'UnicodeDecodeError', 'UnicodeEncodeError', 'UnicodeError', 'UnicodeTranslateError', 'UnicodeWarning', 'UserWarning', 'ValueError', 'Warning', 'WindowsError', 'ZeroDivisionError', '__build_class__', '__debug__', '__doc__', '__import__', '__loader__', '__name__', '__package__', '__spec__', 'abs', 'aiter', 'all', 'anext', 'any', 'ascii', 'bin', 'bool', 'breakpoint', 'bytearray', 'bytes', 'callable', 'chr', 'classmethod', 'compile', 'complex', 'copyright', 'credits', 'delattr', 'dict', 'dir', 'divmod', 'enumerate', 'eval', 'exec', 'exit', 'filter', 'float', 'format', 'frozenset', 'getattr', 'globals', 'hasattr', 'hash', 'help', 'hex', 'id', 'input', 'int', 'isinstance', 'issubclass', 'iter', 'len', 'license', 'list', 'locals', 'map', 'max', 'memoryview', 'min', 'next', 'object', 'oct', 'open', 'ord', 'pow', 'print', 'property', 'quit', 'range', 'repr', 'reversed', 'round', 'set', 'setattr', 'slice', 'sorted', 'staticmethod', 'str', 'sum', 
'super', 'tuple', 'type', 'vars', 'zip']
```

# Lệnh import
- Cú pháp: `import <tên module>`
- Muốn truy cập một phương thức của module đã import, ta dùng lệnh: `<module>.<tên phương thức>`
```python
>>>import math
>>>math.sqrt(2)
1.4142135623709521
```
- Sử dụng trực tiếp hàm số của module: `from <module> import <hàm số>`
	- Hoặc `from <module> import *` sẽ cho phép sử dụng trực tuếp tất cả các hàm của module
```python
>>>from math import sqrt
>>>sqrt(2)
1.4142135623709521
```
- Có thể sử dụng lệnh import để thực hiện với nhiều module: `import <module1>, <module2>,...,<moduleN>`
- Cũng có thể dùng lệnh import như sau:
```python
>>> import math as m
>>> m.sqrt(2)
1.4142135623709521 
```

# Module math

```python
>>>import math
>>>print(dir(math))
['__doc__', '__loader__', '__name__', '__package__', '__spec__', 'acos', 'acosh', 'asin', 'asinh', 'atan', 'atan2', 'atanh', 'cbrt', 'ceil', 'comb', 'copysign', 'cos', 'cosh', 'degrees', 'dist', 'e', 'erf', 'erfc', 'exp', 'exp2', 'expm1', 'fabs', 'factorial', 'floor', 'fmod', 'frexp', 'fsum', 'gamma', 'gcd', 'hypot', 'inf', 'isclose', 'isfinite', 'isinf', 'isnan', 'isqrt', 'lcm', 'ldexp', 'lgamma', 'log', 'log10', 'log1p', 'log2', 'modf', 'nan', 'nextafter', 'perm', 'pi', 'pow', 'prod', 'radians', 'remainder', 'sin', 'sinh', 'sqrt', 'tan', 'tanh', 'tau', 'trunc', 'ulp']
```

# Số phức và module cmath
- Số phức được quy định viết là: `<giá trị phần thực> + <giá trị phần ảo>j`
```python
>>> z = 3 + 2j
>>> z
(3+2j)
>>>type(z)
<class 'complex'>
```
- ==Chú ý==:
	- Nếu giá trị ảo của số phức là 1 thì phải viết là 1j
	- Không được viết j trước giá trị số
- Module cmath của Python bao gồm các hàm, hằng và phương thức hỗ trợ tính toán trên các số phức
```python
>>> import cmath
>>> dir(cmath)
['__doc__', '__loader__', '__name__', '__package__', '__spec__', 'acos', 'acosh', 'asin', 'asinh', 'atan', 'atanh', 'cos', 'cosh', 'e', 'exp', 'inf', 'infj', 'isclose', 'isfinite', 'isinf', 'isnan', 'log', 'log10', 'nan', 'nanj', 'phase', 'pi', 'polar', 'rect', 'sin', 'sinh', 'sqrt', 'tan', 'tanh', 'tau']
```

# Tự thiết lập module
- Mỗi module như vậy là một tệp chương trình `*.py`, trong đó tất cả các hàm số và biến nhớ được định nghĩa sẽ là tài nguyên của module này
- Ví dụ
```python
# Tạo tệp python module1.py
def f1(x):
   print("Đây là số cần in", x)
def f2(x,y):
   return x + y
```
-> Copy tệp vào các thư mục Lib các thư viện gốc của python
```python
>>>import module1
>>>from module1 import *
>>>f1(16)
Đây là số cần in 16
>>> f2(22,22)
44
```

# Sinh số ngẫu nhiên của python
- Module `random` có hàm số `random()` có khả năng sinh ngẫu nhiên một số thực nằm trong khoảng `[0,1)`
```python
>>> from random import random
>>> random()
0.211234321253
```
- ==Chú ý==: Hàm random() không có tham số
- Ví dụ:
```python
>>> for i in range (n):
   print(int(M + (N + 1 - M)*random()), end = " ") # Sinh n các số ngẫy nhiên trong khoảng [M,N]
```

```python
from random import random
N = int(input("Nhập số phần tử cần sinh của dãy: "))
M = int(input("Nhập giá trị MAX của dãy cần sinh: "))
A = []
for i in range(N):
	A. append(int(M*random()))
print(A)
```

```python
import random  
print(random.randrange(1, 10))
```

# Sinh giá trị ngẫu nhiên từ một dãy
- Hàm `choice()`: `choice(<dãy giá trị tuần tự>)`
- Tham số của hàm có thể là một đối tượng dãy tuần tự bất kì như tuple, list, string,... Hàm số sẽ trả lại một phần tử ngẫu nhiên của dãy tuần tự trong hàm số
- Ví dụ:
```python
>>> import random as r
>>> r.choice(range(100))
19
```

```python
>>>import random as r
>>>A = [1,2,3,4,5,1,32,5,6,12,1]
>>>r.choice(A)
32
```

```python
>>> import random as r
>>> s = "LocDepTraiVCH"
>>> r.choice(s)
L
```

```python
>>> import random as r
>>> for i in range(100):
   print(r.choice(range(1,1000)),end = " ")
```

# Các hàm sinh số ngẫu nhiên khác
- `randint(a.b)`: Sinh ngẫu nhiên một số nguyên nằm giữa 2 giá trị [a,b], tính cả nút
- `randrange(start,stop,[step]`: Sinh số ngẫu nhiên nằm trong vùn range tương ứng













