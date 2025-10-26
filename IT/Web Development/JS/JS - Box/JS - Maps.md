```js
const fruits = new Map([  
	["apples", 500],  
]);
fruits.set("bananas", 300);
fruits.get("apples"); // 500
```

# Methods
```js
fruits.size;
fruits.delete("apples");
fruits.clear();
fruits.has("apples");
```

```js
let text = "";  
fruits.forEach (function(value, key) {  
	text += key + ' = ' + value;  
})
```

```js
// List all entries  
let text = "";  
for (const x of fruits.entries()) {  
  text += x;  
}
```

```js
// List all keys  
let text = "";  
for (const x of fruits.keys()) {  
	text += x;  
}
```

```js
// List all values  
let text = "";  
for (const x of fruits.values()) {  
	text += x;  
}
```

```js
// Create an Array  
const fruits = [  
	{name:"apples", quantity:300},  
	{name:"bananas", quantity:500},  
	{name:"oranges", quantity:200},  
	{name:"kiwi", quantity:150}  
];  
  
// Callback function to Group Elements  
function myCallback({ quantity }) {  
	return quantity > 200 ? "ok" : "low";  
}  
  
// Group by Quantity  
const result = Map.groupBy(fruits, myCallback);
```

# WeakMap