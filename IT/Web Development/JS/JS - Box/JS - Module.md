# Export
```js
const name = "Jesse";  
const age = 40;  
  
export {name, age};
```

```js
const message = () => {  
	const name = "Jesse";  
	const age = 40;  
	return name + ' is ' + age + 'years old.';  
};  
  
export default message;
```
# Import
```js
import { name, age } from "./person.js";
import message from "./message.js";
```
