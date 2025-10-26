# Flags

|         |                                              |
| ------- | -------------------------------------------- |
| /       | Opening delimiter for the regular expression |
| pattern | Regular expression (a search criteria)       |
| /       | Closing delimiter for the regular expression |
| flags   | One or more single modifier flags            |

| Flag | Description                                                     |
| ---- | --------------------------------------------------------------- |
| /d   | Performs substring matches (new 2022)                           |
| /g   | Performs a global match (find all)                              |
| /i   | Performs case-insensitive matching                              |
| /m   | Performs multiline matching                                     |
| /s   | Allows . (dot) to match line terminators (new 2018)             |
| /u   | Enables Unicode support (new 2015)                              |
| /v   | An upgrade to the /u flag for better Unicode support (new 2025) |
| /y   | Performs a "sticky" search (new 2015)                           |

## Properties

| Property    | Description                          |
| ----------- | ------------------------------------ |
| global      | Returns `true` if the /g flag is set |
| hasIndices  | Returns `true` if the /d flag is set |
| ignoreCase  | Returns `true` if the /i flag is set |
| multiline   | Returns `true` if the /m flag is set |
| dotAll      | Returns `true` if the /s flag is set |
| sticky      | Returns `true` if the /y flag is set |
| unicode     | Returns `true` if the /u flag is set |
| unicodeSets | Returns `true` if the /v flag is set |

# Classes

| Class  | Description                                         |
| ------ | --------------------------------------------------- |
| [a]    | Matches the character between the brackets          |
| [^a]   | Matches all characters NOT between the brackets     |
| [abc]  | Matches all characters between the brackets         |
| [^abc] | Matches all characters NOT between the brackets     |
| [a-z]  | Matches all characters in the range from a to z     |
| [^a-z] | Matches all characters NOT in the range from a to z |
| [0-9]  | Matches all characters in the range from 0 to 9     |
| [^0-9] | Matches all characters NOT in the range from 0 to 9 |

# Metacharacters

| Meta   | Description                                       |
| ------ | ------------------------------------------------- |
| \d     | Matches Digits                                    |
| \D     | Matches None Digits                               |
| \w     | Matches alphanumeric Word characters              |
| \W     | Matches None alphanumeric Word characters         |
| \s     | Matches Spaces                                    |
| \S     | Matches None Spaces                               |
| \ddd   | Matches characters by the Octal numer ddd         |
| \xhh   | Matches characters by the HexadecimaL number hh   |
| \uhhhh | Matches Unicode characters by the hex number hhhh |

# Quantifiers

| Code   | Description                           |
| ------ | ------------------------------------- |
| x+     | Matches at least one x                |
| x*     | Matches zero or more occurrences of x |
| x?     | Matches zero or one occurrences of x  |
| x{n}   | Matches n occurences of x             |
| x{n,m} | Matches from n to m occurences of x   |
| x{n,}  | Matches n or more occurences of x     |

# Assertions

| Syntax   | Name            | Description                                |
| -------- | --------------- | ------------------------------------------ |
| ^        | String boundary | Matches the beginning of a string          |
| $        | String boundary | Matches the end of a string                |
| \b       | Word boundary   | Matches the beginning or end of a word     |
| \B       | Word boundary   | Matches NOT the beginning or end of a word |
| (?=...)  | Lookahead       | Matches the subsequent string              |
| (?!...)  | Lookahead       | Matches NOT the subsequent string          |
| (?<=...) | Lookbehind      | Matches the previous string                |
| (?<!...) | Lookbehind      | Matches NOT the previous string            |

| Char           | Description               |
| -------------- | ------------------------- |
| (x)            | Matches x and saves it    |
| (?`<n>`x)        | Matches x and labels it n |
| (?flag:x)      | Enables flag(s) for x     |
| (?flag-flag:x) | Disables flag(s) for x    |

# Methods
| Name        | Description                                                                                 |
| ----------- | ------------------------------------------------------------------------------------------- |
| compile()   | Compiles a regular expression (Deprecated)                                                  |
| constructor | Returns the function that created the RegExp prototype                                      |
| dotAll      | Returns `true` if the **s** flag is set in the expression                                   |
| escape()    | Returns a string where characters that belongs to the regular expression syntax are escaped |
| exec()      | Returns a result array for a matches in a string                                            |
| flags       | Returns the modifiers set in the expression                                                 |
| global      | Returns `true` if the **g** flag is set in the expression                                   |
| hasIndices  | Returns `true` if the **d** flag is set (new in 2022)                                       |
| ignoreCase  | Returns `true` if the **i** flag is set                                                     |
| lastIndex   | Specifies the index at which to start the next match                                        |
| multiline   | Returns `true` if the **m** modifier is set                                                 |
| source      | Returns the text of the RegExp pattern                                                      |
| sticky      | Returns `true` if the **y** flag is set                                                     |
| test()      | Tests for a match in a string. Returns `true` or `false`                                    |
| toString()  | Returns the string value of the regular expression                                          |
| unicode     | Returns `true` if the **u** flag is set                                                     |
| unicodeSets | Returns `true` if the **v** flag is set                                                     |