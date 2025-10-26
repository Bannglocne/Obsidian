> **J**ava**S**cript **O**bject **N**otation.
> A **plain text format** for storing and transporting data.
> **Send**, **Receive** and **Store data**.>

### Data Types:
- [[JS - String| String]]
- [[JS - Number | Number]]
- [[JS - Objects| Object]]
- [[JS - Arrays| Array]]
- _boolean_
- _null_
(Can not be: [[JS - Dates|Date]], [[JS - Functions| Functions]], _undefined_)

```json
{  
	"employees":[  // Array
		{"firstName":"John", "lastName":"Doe"},  // Object
		{"firstName":"Anna", "lastName":"Smith"},  
		{"firstName":"Peter", "lastName":"Jones"}  
]  
}
```

```js
const myObj = JSON.parse(text);
const myJSON = JSON.stringify(obj); // JSON.stringify(arr / num / bool);
```