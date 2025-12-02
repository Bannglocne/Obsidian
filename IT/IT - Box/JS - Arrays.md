**Arrays** use **numbered indexes** while **[[JS - Objects|Object]]** use **named indexes**.
```js
const num = ["1", "2"];

num[2]= "3";
num.push("4");  // Adds a new element (4) to num
name[name.length] = "5";  // Adds "5" to num
```

## Nested Arrays and Objects
```js
const myObj = {  
  name: "Loc",  
  age: 18,  
  cars: [  
    {name:"Mercedes", models:["C200", "C300"]},  
    {name:"Maybach", models:["S500", "S680"]}  
  ]  
}
```

# Methods
```js
const myChar = ["A", "B", "C", "D"];

myChar.length; // 4
myChar.length = 2; // Set length to 2

myChar.toString(); // A,B,C,D
myChar.join(" * "); // A * B * C * D

myChar.pop() // A,B,C
let x1 = myChar.pop(); // C
myChar.push("E"); // A,B,E

myChar.shift(); // B,E
let x2 = myChar.shift(); // B
myChar.unshift("A"); // A,E
```

```js
const char_1 = ["A", "B","C","D","E","F"];  
const char_2 = ["G"];
const char_3 = ["H"];
  
const myChar = char_1.concat(char_2, char_3); // A,B,C,D,E,F,G,H
const herChar = char_1.concat("F"); // A,B,C,D,E,F,H

char_1.copyWithin(2,0,2); // A,B,A,B,G,H
```

```js
const myArr = [[1,2],[3,4],[5,6]];  
const newArr = myArr.flat(); // 1,2,3,4,5,6 (Reducing the dimensionality of an array)

const newerArr = newArr.flatMap(x => [x, x * 10]); // 1,10,2,20,3,30,4,40,5,50,6,60
```

```js
const myChar = ["A", "B", "C", "D"];

const spliced = myChar.toSpliced(0, 1); // B,C,D -> Keep the original array unchanged
let removed = myChar.splice(2, 2, "E", "F"); // C, D -> Use to remove elements without leaving holes
myChar // A,B,E,F

const sliced = myChar.slice(1, 3); // B,E -> Create a new array when keep the original array unchanged
myChar // A,B,E,F
```

# Search
```js
array.lastIndexOf(item, start)
array.includes(search-item)

array.findIndex(function)
array.find(function)

array.findLast(condition)
findLastIndex(condition)
```

```js 
const numbers = [4, 25, 29];  
let first = numbers.find(myFunction);  // Returns the value of the first array element that passes a test function
  
function myFunction(value, index, array) {  
  return value > 18;  
}
```

```js
const temp = [30, 40, 42];  
let high = temp.findLast(x => x > 40);
```

# Sort
```js
array.sort() // Sorts an array alphabetically -> Safer: toSorted()
array.reverse() // Reverses the elements in an array -> Safer: toReversed()

array.sort(function(a, b){return a - b}); // Numeric sort
arrray.sort(function(){return 0.5 - Math.random()}); // Random order
```

```js
const points = [40, 100, 1, 5, 25, 10];

function myArrayMin(arr) {  
  return Math.min.apply(null, arr);  
} // Find the lowest number in an array
myArrayMin(points)

function myArrayMax(arr) {  
  return Math.max.apply(null, arr);  
} // Find the highest number in an array
myArrayMax(points)
```

# Iterations
```js
const numbers = [45, 4, 9, 16, 25];  
```

```js
let txt = "";  
numbers.forEach(myFunction);  // calls a function once for each array element 
  
function myFunction(value, index, array) {  
  txt += value + "<br>";  
}
```

```js
const numbers2 = numbers1.map(myFunction);  // creates a new array by performing a function on each array element
  
function myFunction(value, index, array) {  
  return value * 2;  
}
```

```js
const newArr = myArr.flatMap((x) => x * 2); // first maps all elements of an array and then creates a new array by flattening the array
```

```js
const over18 = numbers.filter(myFunction);  // creates a new array with array elements that pass a test     
  
function myFunction(value, index, array) {  
  return value > 18;  
}
```

```js
let sum = numbers.reduce(myFunction);  // runs a function on each array element to produce a single value
  
function myFunction(total, value, index, array) {  
  return total + value;  
}
```

```js
let sum = numbers.reduceRight(myFunction);  // runs a function on each array element to produce a single value  
  
function myFunction(total, value, index, array) {  
  return total + value;  
}
```

```js
let allOver18 = numbers.every(myFunction);   // checks if all array values pass a test
  
function myFunction(value, index, array) {  
  return value > 18;  
}
```

```js
let someOver18 = numbers.some(myFunction);  // checks if some array values pass a test    
  
function myFunction(value, index, array) {  
  return value > 18;  
}
```

```js
const myArr = Array.from(num, (x) => x * 2);  // returns an Array object from: Any iterable object; Any object with a length property
```

```js
const keys = num.keys();  // returns an Array Iterator object with the keys of an array
  
for (let x of keys) {  
  text += x + "<br>";  
}
```

```js
const f = num.entries();  // iterate over the key/value pairs
  
for (let x of f) {  
  document.getElementById("demo").innerHTML += x;  
}
```

```js
const months = ["Januar", "Februar", "Mar", "April"];  
const myMonths = months.with(2, "March"); // update elements in an array without altering the original array
```

```js
const arr1 = [1, 2, 3];  
const arr2 = [4, 5, 6];  
  
const arr3 = [...arr1, ...arr2];  // expands an array into individual elements
```