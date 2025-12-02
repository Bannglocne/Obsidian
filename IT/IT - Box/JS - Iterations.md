| Function  | Description                                                                            |
| --------- | -------------------------------------------------------------------------------------- |
| drop()    | Returns an iterator that skips a specified number of elements before yielding the rest |
| every()   | Returns `true` if all elements satisfy a test function                                 |
| filter()  | Returns an iterator containing elements that satisfy a filter function                 |
| find()    | Returns the first element that satisfies a test function                               |
| flatMap() | Returns an iterator by mapping each element and then flattening the results            |
| forEach() | Executes a function once for each element in the iterator.                             |
| from()    | creates an iterator object from an iterable                                            |
| map()     | Returns an iterator with all elements transformed by a map function                    |
| reduce()  | Applies a reducer function against each element to reduce it to a single value         |
| some()    | Returns `true` if at least one element satisfy a test function                         |
| take()    | Returns an iterator that yields a specified number of elements                         |

# Generator
```js
function* myStream() {  
// return {value:1, done:false}  
yield 1;  
  
// return {value:2, done:false}  
yield 2;  
  
// return {value:3, done:true}  
return 3;  
}  
  
// Create a Generator  
let myGenerator = myStream();  
  
// Iterate over the Generator  
for (let value of myGenerator) { // code }
```