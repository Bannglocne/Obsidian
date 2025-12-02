```js
function name1(a, b) {
	return a * b;
}
let name2 = function(a, b) {return a * b}
let myFunction = (a, b) => a * b;

const myFunction = new Function("a", "b", "return a * b");
```

# call() & apply()
```js
const person = {  
	fullName: function(city, country) {  
		return this.firstName + " " + this.lastName + "," + city + "," + country;  
	}  
}   
const person1 = {  
	firstName:"John",  
	lastName: "Doe"  
}  
person.fullName.call(person1, "Oslo", "Norway"); // separately
person.fullName.apply(person1, ["Oslo", "Norway"]); // array
```

# bind()
Borrow a method from another object
```js
const person = {  
	firstName:"John",  
	lastName: "Doe",  
	fullName: function () {  
		return this.firstName + " " + this.lastName;  
	}  
}  
const member = {  
	firstName:"Hege",  
	lastName: "Nilsen",  
}  
let fullName = person.fullName.bind(member);
```

**Can be used to preserve this **
```js
const person = {  
	firstName:"John",  
	lastName: "Doe",  
	display: function () {  
		let x = document.getElementById("demo");  
		x.innerHTML = this.firstName + " " + this.lastName;  
	}  
}  
  
let display = person.display.bind(person);  
setTimeout(display, 3000);
```