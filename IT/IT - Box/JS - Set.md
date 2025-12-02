```js
const letters = new Set(["a"]);
letters.add("b");

const c = "c";
letters.add(c);
```

# Methods
```js
letters.size; // 3
answer = letters.has("d"); // false
```

```js
let text = "";  
letters.forEach (function(value) {  
	text += value;  
})
```

```js
// Get all Values  
const myIterator = letters.values();  
  
// List all Values  
let text = "";  
for (const entry of myIterator) {  
  text += entry;  
}
```

```js
// Create an Iterator  
const myIterator = letters.keys();  
  
// List all Elements  
let text = "";  
for (const x of myIterator) {  
  text += x;  
}
```

```js
// Get all Entries  
const myIterator = letters.entries();  
  
// List all Entries  
let text = "";  
for (const entry of myIterator) {  
  text += entry;  
}
```

# Logic
```js
const C = A.union(B); // Hợp
const C = A.intersection(B); // Giao
const C = A.difference(B); // Trừ
const C = A.symetricDifference(B); // Hiệu đối xứng
let answer = A.isSubsetOf(B); // Tập con
let answer = A.isSupersetOf(B); // Tập cha
let answer = A.isDisjointFrom(B); // Tập không giao
```

# WeakSet
