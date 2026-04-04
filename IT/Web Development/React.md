#front-end #web #js #css 
# ES6 
- **[[JS - Classes| Class]]**
- **Arrow Function**: Write shorter [[JS - Functions| function]] syntax
```jsx
// Before
hello = function() {
  return "Hello World!";
}

// After
hello = () => {
  return "Hello World!";
}

hello = () => "Hello World!";
```
- **[[JS - Maps|Map]]**
- **Destructing:** Makes code cleaner and more readable by reducing repetitive object and array access
```jsx
const person = {
	name: "A",
	car: {
		brand: 'Maybach',
		model: 'S680',
  }
};

// Destructuring
let {name, car: { brand, model }} = person;
```
- **Spread Operator:** Quickly copy all or part of an existing array or object into another array or object.