
# Syntax Error và Logic Error
```python
>>> iff 4 < 5
SyntaxError: invalid syntax
```

- **Logic Error:**
	- Input errors -
	- Divide by zero errors 
	- Index errors exceeding the range limit 
	- Runtime errors too long 
	- Function call errors with incorrect type parameters

# Exception
```python
try:
   <command to catch errors>
except <Exception_1>:
   <error handling commands 1>
except <Exception_2>:
   <error handling commands 2>
except (<Exception_3>,<Exception_4>,....):
   <error handling commands 3 and 4 errors>
.
.
.
except Exception:
   <other error handling commands>
else:
   <commands executed when there are no errors>
finally:
   <commands always executed> #Regardless of whether there is an error or not
```

## Detailed error correction
**Error details**
```python
while True:
   try:
      x = int(input("Enter a number:"))
      break
   except ValueError as Err:
      print("You entered wrong: ", Err)
      print("Try again.")
print("You have entered the number: ", x)
```

**Skip Error**
```python
while True:
   try:
      x = int(input("Enter a number:"))
      break
   except ValueError:
      pass
print("You have entered the number: ", x)
```

## Some Exception in Python

| Error Name          | Error Details                                     |
| ------------------- | ------------------------------------------------- |
| AttributeError      | Accessing object properties                       |
| ZeroDivisionError   | Division by 0                                     |
| OverflowError       | Decimal overflow                                  |
| EOFError            | Trying to read information at the end of the file |
| ModuleNotFoundError | Module not found                                  |
| IndexError          | Array index                                       |
| KeyError            | Dictionary key                                    |
| NameError           | Accessing name in Namespace                       |
| RecursionError      | Recursion exceeds allowed limit                   |
| TypeError           | Type                                              |
| ValueError          | Value of an object                                |
| FileNoFoundError    | File no found                                     |
| FileExistError      | Overwriting existing file                         |
| IndentationError    | Command line error indenting incorrectly          |
| SyntaxError         | Syntax error                                      | 
