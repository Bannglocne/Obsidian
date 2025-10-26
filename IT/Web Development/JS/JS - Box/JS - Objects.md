```js
const person = {  
	first: "A",  
	last: "B",
	full : function() {  
		return this.first + " " + this.last;
	}  
	pets: {
		dog: brown;
	}
};

person.age = 18; 
delete person.age;
```

**Object Constructor [[JS - Functions|Functions]]**
```js
function Person(first, last) {  
	this.first = first;  
	this.last = last;  
}

const Father = new Person("A1", "A2");  
const Mother = new Person("B1", "B2")
```

# Display
```js
// Create an Array  
const myArray = Object.values(person);  
  
// Stringify the Array  
let text = myArray.toString();

let text = "";  
for (let [name, value] of Object.entries(person)) {  
  text += name + ": " + value + "<br>";  
}
```

# Destructing
```js
let {first, last, country = "Vietnam"} = person;
```

```js
const fruits = ["Bananas", "Oranges", "Apples", "Mangos"];

let [fruit1, fruit2] = fruits;
let [fruit1,,,fruit2] = fruits; // Skipping array value
let {[0]:fruit1 ,[1]:fruit2} = fruits; // Position value
```

# Prototypes
```js
function Person(first, last,) {  
	this.firstName = first;  
	this.lastName = last;  
}  
Person.prototype.nationality = "VietNam"; // Add properties to object constructor
```

# Iterations
```js
// Copies properties from a source object to a target object  
Object.assign(target, source)  
  
// Creates an object from an existing object  
Object.create(object)  
  
// Returns an array of the key/value pairs of an object  
Object.entries(object)  
  
// Creates an object from a list of keys/values  
Object.fromEntries()  
  
// Returns an array of the keys of an object  
Object.keys(object)  
  
// Returns an array of the property values of an object  
Object.values(object)  
  
// Groups object elements according to a function  
Object.groupBy(object, callback)
```

# Management
```js
// Adding or changing an object property  
Object.defineProperty(object, property, descriptor)  
  
// Adding or changing object properties  
Object.defineProperties(object, descriptors)  
  
// Accessing a Property  
Object.getOwnPropertyDescriptor(object, property)  
  
// Accessing Properties  
Object.getOwnPropertyDescriptors(object)  
  
// Returns all properties as an array  
Object.getOwnPropertyNames(object)  
  
// Accessing the prototype  
Object.getPrototypeOf(object)
```

# Get / Set
```js
// Create an object:  
const person = {  
	firstName: "John",  
	lastName: "Doe",  
	language: "en",  
	get lang() {  
		return this.language;  
  }  
};  
  
// Display data from the object using a getter:  
document.getElementById("demo").innerHTML = person.lang;
```

```js
const person = {  
	firstName: "John",  
	lastName: "Doe",  
	language: "",  
	set lang(lang) {  
		this.language = lang;  
  }  
};  
  
// Set an object property using a setter:  
person.lang = "en";  
  
// Display data from the object:  
document.getElementById("demo").innerHTML = person.language;
```

# Protection
```js
// Prevents re-assignment  
const car = {type:"Fiat", model:"500", color:"white"};  
  
// Prevents adding object properties  
Object.preventExtensions(object)  
  
// Returns true if properties can be added to an object  
Object.isExtensible(object)  
  
// Prevents adding and deleting object properties  
Object.seal(object)  
  
// Returns true if object is sealed  
Object.isSealed(object)  
  
// Prevents any changes to an object  
Object.freeze(object)  
  
// Returns true if object is frozen  
Object.isFrozen(object)
```