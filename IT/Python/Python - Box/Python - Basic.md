# Print
```python
print(<value>, sep="...",end ="...",file ="...",flush="...")
```

# Input
```python
>>>x = input("Enter a number: ")
Enter a number: 5

>>>type(x)
<class 'str'>
```

# Comment
```python
# Comment

'''
Comment 1
Comment 2
'''

```

# Variable
```python
a,b,c = "A", 1, 2

a,b,c = 1

fruits = ["apple", "banana", "cherry"]  
x, y, z = fruits
```

## Scope
```python
global x
nonlocal x
```

## Keyword
| Flase   | None     | True     | and    | as    | assert | break  |
| ------- | -------- | -------- | ------ | ----- | ------ | ------ |
| class   | continue | def      | del    | elif  | else   | except |
| finally | for      | from     | global | if    | import | in     |
| is      | lambda   | nonlocal | not    | or    | pass   | raise  |
| return  | try      | while    | with   | yield |        |        |

# Data Types
- [[Python - String|String]]
- [[Python - Numeric|Numeric]]
- [[Python - Conditional & Loop|Sequence]]
- [[Python - Dictionary|Dictionary]]
- [[Python - Boolean|Boolean]]
- [[Python - Set|Set]]
- Binary:  _bytes_; _bytearray_; _memoryview_
- None: _NoneType_

# Arithmetic Expressions & Operator
- `+`, `-`, `*`, `/`, `//`, `%`, `**`
- `==`, `!=`, `>` , `,` , `>=` , `<=`
- `+=`, `-=`
- `divmod(x, y) = x // y, x % y`
- `eval()`
```python
>>> eval("1+2, 3**4, 14.2")
(3, 9, 28)
```
- `e`: 13e10 = 13.(10^50)
- **Bitwise**: `&`, `|`, `^`, `~`, `<<`, `>>`
---
> [!NOTE] Precedence
> `()`
> `**`
> `+x`, `-x`, `~x`
> `*`, `/`, `//`, `%` - `+`, `-`
> `<<`, `>>`
> `&` - `^` - `|`
> `==`,  `!=`,  `>`,  `>=`,  `<`,  `<=`,  `is`,  `is not`,  `in`,  `not in`
> `not` - `and` - `or`


# Stuff
## Help
- `help(<tên lệnh cần trợ giúp>)`
- Hoặc:
```python
help()
.
.
help> <lệnh>
```
-> `Enter`: Thoát

## Swap value
```python
x,y = y,x
```

## Separate Command
- Dùng `;`
```python
print("Hà"); print("Nội")
```

## Multiple  Lines Command
- Dùng `\`
```python
a = "Trời đẹp \
quá"
>>> a
"Trời đẹp quá"
```

## Underscore
- `_`: Không cần gán giá trị, mặc định gán giá trị biểu thức tính gần đây nhất

## Combine Function
```python
>>> int(float("3.141567"))
3
```