```html
<script src="script.js"></script>
```

**Comment**
```js
// Inline comment

/* 
Multiple lines comment
*/
```

# Variables
|         | Scope | Redeclare | Reassign | Hoisted | Binds this |
| ------- | ----- | --------- | -------- | ------- | ---------- |
| `var`   | No    | Yes       | Yes      | Yes     | Yes        |
| `let`   | Yes   | No        | Yes      | No      | No         |
| `const` | Yes   | No        | No       | No      | No         |

# Types
| Type      | Description                                   |
| --------- | --------------------------------------------- |
| String    | A text of characters enclosed in quotes       |
| Number    | A number representing a mathematical value    |
| Bigint    | A number representing a large integer         |
| Boolean   | A data type representing true or false        |
| Object    | A collection of key-value pairs of data       |
| Undefined | A primitive variable with no assigned value   |
| Null      | A primitive value representing object absence |
| Symbol    | A unique and primitive identifier             |

```js
typeof <variables>;
```

# Operators

- `+=` `-=` `*=` `/=` `%=` `**=`
- `++` `--`
- `==` `===` `!=` `!==` `>` `<` `>=` `<=`
- `&&` `||` `!`


# Conditions
```js
if (condition1) {  

} else if (condition2) {  

} else {  
  
}
```

```js
switch(expression) {  
	case x:  
		// code block  
		break;  
	case y:  
		// code block  
		break;  
	default:  
		// code block 
}
```

```js
condition ? expression1 : expression2
```

# Loops
```js
for (expr1; expr2; expr) {  
  // code block
}

for (key in object) {  
  // code block
}

for (variable of iterable) {  
  // code block
}
```

```js
while (condition) {  
  // code block 
}
```

```js
do {  
// code block to be executed  
}  
while (condition);
```

# Errors
```js
try {  
	Block of code to try  
}  
catch(err) {  
	Block of code to handle errores  
}  
finally {  
	Block of code to be executed regardless of the try / catch result  
}
```

| Error Name     | Description                     |
| -------------- | ------------------------------- |
| EvalError      | An error in the eval() function |
| RangeError     | A number "out of range"         |
| ReferenceError | An illegal reference            |
| SyntaxError    | A syntax error                  |
| TypeError      | A type error                    |
| URIError       | An error in encodeURI()         |

# Events
```js
<element event = "some JavaScript">
```

| Event       | Description                                        |
| ----------- | -------------------------------------------------- |
| onchange    | An HTML element has been changed                   |
| onclick     | The user clicks an HTML element                    |
| onmouseover | The user moves the mouse over an HTML element      |
| onmouseout  | The user moves the mouse away from an HTML element |
| onkeydown   | The user pushes a keyboard key                     |
| onload      | The browser has finished loading the page          |