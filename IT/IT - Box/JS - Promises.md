# Callback
A callback is a function passed as an argument to another function.
```js
function myDisplayer(some) {  
	document.getElementById("demo").innerHTML = some;  
}  
  
function myCalculator(num1, num2, myCallback) {  
	let sum = num1 + num2;  
	myCallback(sum);  
}  
  
myCalculator(5, 5, myDisplayer);
```

# Asynchronous
```js
etTimeout(function() { myFunction("I love You !!!"); }, 3000);  
  
function myFunction(value) {  
	document.getElementById("demo").innerHTML = value;  
}
```

```js
setInterval(myFunction, 1000);  
  
function myFunction() {  
	let d = new Date();  
	document.getElementById("demo").innerHTML=  
	d.getHours() + ":" +  
	d.getMinutes() + ":" +  
	d.getSeconds();  
}
```

# Promises
```js
myFunction().then(  
	function(value) { /* code if successful */ },  
	function(error) { /* code if some error */ }  
);
```

```js
function myDisplayer(some) {  
	document.getElementById("demo").innerHTML = some;  
}  
  
let myPromise = new Promise(function(myResolve, myReject) {  
	let x = 0;  
	
	if (x == 0) {  
		myResolve("OK");  
	} else {  
		myReject("Error");  
	}  
});  
  
myPromise.then(  
	function(value) {myDisplayer(value);},  
	function(error) {myDisplayer(error);}  
);
```

# Async
```js
async function myFunction() {  
	return "Hello";  
}  
myFunction().then(  
	function(value) {myDisplayer(value);},  
	function(error) {myDisplayer(error);}  
);
```

```js
async function myDisplay() {  
	let myPromise = new Promise(function(resolve, reject) {  
		resolve("I love You !!");  
  });  
	document.getElementById("demo").innerHTML = await myPromise;  
}  

myDisplay();
```