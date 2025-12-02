>Consider a module to be the same as a code library.
>A file containing a set of functions you want to include in your application.

```python
import module_name as name
from module_name import method_1, method_2
from module_name import *
```

# Datetime
```python
>>> import datetime
>>> print(dir(datetime))
['MAXYEAR', 'MINYEAR', 'UTC', '__all__', '__builtins__', '__cached__', '__doc__', '__file__', '__loader__', '__name__', '__package__', '__spec__', 'date', 'datetime', 'datetime_CAPI', 'time', 'timedelta', 'timezone', 'tzinfo']
```

```python
import datetime
x = datetime.datetime.now()
print(x.strftime(" "))
```

| Directive | Description                                                 |
| --------- | ----------------------------------------------------------- |
| %a        | Weekday, short version                                      |
| %A        | Weekday, full version                                       |
| %w        | Weekday as a number 0-6, 0 is Sunday                        |
| %d        | Day of month 01-31                                          |
| %b        | Month name, short version                                   |
| %B        | Month name, full version                                    |
| %m        | Month as a number 01-12                                     |
| %y        | Year, short version, without century                        |
| %Y        | Year, full version                                          |
| %H        | Hour 00-23                                                  |
| %I        | Hour 00-12                                                  |
| %p        | AM/PM                                                       |
| %M        | Minute 00-59                                                |
| %S        | Second 00-59                                                |
| %f        | Microsecond 000000-999999                                   |
| %z        | UTC offset                                                  |
| %Z        | Timezone                                                    |
| %j        | Day number of year 001-366                                  |
| %U        | Week number of year, Sunday as the first day of week, 00-53 |
| %W        | Week number of year, Monday as the first day of week, 00-53 |
| %c        | Local version of date and time                              |
| %C        | Century                                                     |
| %x        | Local version of date                                       |
| %X        | Local version of time                                       |
| `%%`      | A % character                                               |
| %G        | ISO 8601 year                                               |
| %u        | ISO 8601 weekday (1-7)                                      |
| %V        | ISO 8601 weeknumber (01-53)                                 |

# Module math
```python
>>>import math
>>>print(dir(math))
['__doc__', '__loader__', '__name__', '__package__', '__spec__', 'acos', 'acosh', 'asin', 'asinh', 'atan', 'atan2', 'atanh', 'cbrt', 'ceil', 'comb', 'copysign', 'cos', 'cosh', 'degrees', 'dist', 'e', 'erf', 'erfc', 'exp', 'exp2', 'expm1', 'fabs', 'factorial', 'floor', 'fmod', 'frexp', 'fsum', 'gamma', 'gcd', 'hypot', 'inf', 'isclose', 'isfinite', 'isinf', 'isnan', 'isqrt', 'lcm', 'ldexp', 'lgamma', 'log', 'log10', 'log1p', 'log2', 'modf', 'nan', 'nextafter', 'perm', 'pi', 'pow', 'prod', 'radians', 'remainder', 'sin', 'sinh', 'sqrt', 'tan', 'tanh', 'tau', 'trunc', 'ulp']
```

```python
>>> import cmath
>>> dir(cmath)
['__doc__', '__loader__', '__name__', '__package__', '__spec__', 'acos', 'acosh', 'asin', 'asinh', 'atan', 'atanh', 'cos', 'cosh', 'e', 'exp', 'inf', 'infj', 'isclose', 'isfinite', 'isinf', 'isnan', 'log', 'log10', 'nan', 'nanj', 'phase', 'pi', 'polar', 'rect', 'sin', 'sinh', 'sqrt', 'tan', 'tanh', 'tau']
```

# Random
```python
>>> from random import random
>>> random()
0.211234321253
```

- `choice()`: `choice(<iterable>)`:  Generate random values ​​from a sequence
```python
>>>import random as r
>>>A = [1,2,3,4,5,1,32,5,6,12,1]
>>>r.choice(A)
32
```

- `randint(a.b)`: Randomly generate an integer between 2 values ​​[a,b]
- `randrange(start,stop,[step]`: Randomly generate in a range 

# RegEx
For more information: [[JS - RegExp]]
```python
>>> import re
>>> print(dir(re))
['A', 'ASCII', 'DEBUG', 'DOTALL', 'I', 'IGNORECASE', 'L', 'LOCALE', 'M', 'MULTILINE', 'Match', 'NOFLAG', 'Pattern', 'PatternError', 'RegexFlag', 'S', 'Scanner', 'U', 'UNICODE', 'VERBOSE', 'X', '_MAXCACHE', '_MAXCACHE2', '_ZeroSentinel', '__all__', '__builtins__', '__cached__', '__doc__', '__file__', '__loader__', '__name__', '__package__', '__path__', '__spec__', '__version__', '_cache', '_cache2', '_casefix', '_compile', '_compile_template', '_compiler', '_constants', '_parser', '_pickle', '_special_chars_map', '_sre', '_zero_sentinel', 'compile', 'copyreg', 'enum', 'error', 'escape', 'findall', 'finditer', 'fullmatch', 'functools', 'match', 'purge', 'search', 'split', 'sub', 'subn']
```
## Functions

| Function | Description                                                       |
| -------- | ----------------------------------------------------------------- |
| findall  | Returns a list containing all matches                             |
| search   | Returns a Match object if there is a match anywhere in the string |
| split    | Returns a list where the string has been split at each match      |
| sub      | Replaces one or many matches with a string                        |

## Metacharacter
| Character | Description                                                                | 
| --------- | -------------------------------------------------------------------------- |
| []        | A set of characters                                                        |
| \|        | Signals a special sequence (can also be used to escape special characters) |
| .         | Any character (except newline character)                                   |
| ^         | Starts with                                                                |
| $         | Ends with                                                                  |
| *         | Zero or more occurrences                                                   |
| +         | One or more occurrences                                                    |
| ?         | Zero or one occurrences                                                    |
| {}        | Exactly the specified number of occurrences                                |
| \|        | Either or                                                                  |
| ()        | Capture and group                                                          |

## Flags
You can add flags to the pattern when using regular expressions.

| Flag          | Shorthand | Description                                                                                                        | 
| ------------- | --------- | ------------------------------------------------------------------------------------------------------------------ | 
| re.ASCII      | re.A      | Returns only ASCII matches                                                                                         |        
| re.DEBUG      |           | Returns debug information                                                                                          |        
| re.DOTALL     | re.S      | Makes the . character match all characters (including newline character)                                           |        
| re.IGNORECASE | re.I      | Case-insensitive matching                                                                                          |        
| re.MULTILINE  | re.M      | Returns only matches at the beginning of each line                                                                 |        
| re.NOFLAG     |           | Specifies that no flag is set for this pattern                                                                     |        
| re.UNICODE    | re.U      | Returns Unicode matches. This is default from Python 3. For Python 2: use this flag to return only Unicode matches |        
| re.VERBOSE    | re.X      | Allows whitespaces and comments inside patterns. Makes the pattern more readable                                   |      

## Special Sequences
A special sequence is a `\` followed by one of the characters in the list below, and has a special meaning:

| Character | Description                                                                                                                                                                                                      |
| --------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| \A        | Returns a match if the specified characters are at the beginning of the string                                                                                                                                   |
| \b        | Returns a match where the specified characters are at the beginning or at the end of a word  <br>(the "r" in the beginning is making sure that the string is being treated as a "raw string")                    |
| \B        | Returns a match where the specified characters are present, but NOT at the beginning (or at the end) of a word  <br>(the "r" in the beginning is making sure that the string is being treated as a "raw string") |
| \d        | Returns a match where the string contains digits (numbers from 0-9)                                                                                                                                              |
| \D        | Returns a match where the string DOES NOT contain digits                                                                                                                                                         |
| \s        | Returns a match where the string contains a white space character                                                                                                                                                |
| \S        | Returns a match where the string DOES NOT contain a white space character                                                                                                                                        |
| \w        | Returns a match where the string contains any word characters (characters from a to Z, digits from 0-9, and the underscore _ character)                                                                          |
| \W        | Returns a match where the string DOES NOT contain any word characters                                                                                                                                            |
| \Z        | Returns a match if the specified characters are at the end of the string                                                                                                                                         |


## Sets
A set is a set of characters inside a pair of square brackets `[]` with a special meaning:

| Set        | Description                                                                                                                             |     
| ---------- | --------------------------------------------------------------------------------------------------------------------------------------- |  
| [arn]      | Returns a match where one of the specified characters (`a`, `r`, or `n`) is present                                                     |     
| [a-n]      | Returns a match for any lower case character, alphabetically between `a` and `n`                                                        |     
| `[^arn] `  | Returns a match for any character EXCEPT `a`, `r`, and `n`                                                                              |     
| [0123]     | Returns a match where any of the specified digits (`0`, `1`, `2`, or `3`) are present                                                   |     
| [0-9]      | Returns a match for any digit between `0` and `9`                                                                                       |     
| [0-5][0-9] | Returns a match for any two-digit numbers from `00` and `59`                                                                            |     
| [a-zA-Z]   | Returns a match for any character alphabetically between `a` and `z`, lower case OR upper case                                          |     
| [+]        | In sets, `+`, `*`, `.`, `\|`, `()`, `$`,`{}` has no special meaning, so `[+]` means: return a match for any `+` character in the string |     