Template for [[JS - Objects| Object]]
```js
class Car {  
	constructor(brand) {  
		this.carname = brand;  
	}  
	present() {  
		return 'I have a ' + this.carname;  
	}  
	static hello() {  // Static
		return "Hello!!";  
	}
}  
  
class Model extends Car {  //  Inheritance
	constructor(brand, mod) {  
		super(brand);  
		this.model = mod;  
	}  
	show() {  
		return this.present() + ', it is a ' + this.model;  
	}  
}  
  
let myCar = new Model("Ford", "Mustang");  
document.getElementById("demo").innerHTML = myCar.show();
```

# Using Getter / Setter
```js
class Car {  
	constructor(brand) {  
		this.carname = brand;  
	}  
	get cnam() {  
		return this.carname;  
	}  
	set cnam(x) {  
		this.carname = x;  
	}  
}  
  
const myCar = new Car("Ford");  
  
document.getElementById("demo").innerHTML = myCar.cnam;
```