> **J**ava**S**cript **O**bject **N**otation.
> A **plain text format** for storing and transporting data.
> **Send**, **Receive** and **Store data**.>

| Python                        | JSON                     |
| ----------------------------- | ------------------------ |
| [[Python - Dictionary\|dict]] | [[JS - Objects\|object]] |
| [[Python - List\|list]]       | [[JS - Arrays\|array]]   |
| [[Python - Tuple\|tuple]]     | [[JS - Arrays\|array]]   |
| [[Python - String\|string]]   | [[JS - String\|string]]  |
| [[Python - Numeric\|int]]     | [[JS - Number\|number]]  |
| [[Python - Numeric\|float]]   | [[JS - Number\|number]]  |
| [[Python - Boolean\|True]]    | true                     |
| [[Python - Boolean\|False]]   | false                    |
| None                          | null                     | 


```json
{  
	"employees":[  // Array
		{"firstName":"John", "lastName":"Doe"},  // Object
		{"firstName":"Anna", "lastName":"Smith"},  
		{"firstName":"Peter", "lastName":"Jones"}  
]  
}
```

# Convert
```js
const myObj = JSON.parse(text);
const myJSON = JSON.stringify(obj); // JSON.stringify(arr / num / bool);
```

```python
y = json.dumps(x, indent=4, separators=(". ", " = "), sort_keys=True)
```