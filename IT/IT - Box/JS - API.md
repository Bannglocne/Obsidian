# Validity
**checkValidity()**
```js
<input id="id1" type="number" min="100" max="300" required>  
<button onclick="myFunction()">OK</button>  
  
<p id="demo"></p>  
  
<script>  
function myFunction() {  
	const inpObj = document.getElementById("id1");  
	if (!inpObj.checkValidity()) { 
		document.getElementById("demo").innerHTML = inpObj.validationMessage;  
	}  
}  
</script>
```

- `setCustomValidity()`: Sets the validationMessage property of an input element.

## Constraint Validation DOM Properties

| Property          | Description                                                              |
| ----------------- | ------------------------------------------------------------------------ |
| validity          | Contains boolean properties related to the validity of an input element. |
| validationMessage | Contains the message a browser will display when the validity is false.  |
| willValidate      | Indicates if an input element will be validated.                         |

## Validity Properties

| Property        | Description                                                              |
| --------------- | ------------------------------------------------------------------------ |
| customError     | Set to true, if a custom validity message is set.                        |
| patternMismatch | Set to true, if an element's value does not match its pattern attribute. |
| rangeOverflow   | Set to true, if an element's value is greater than its max attribute.    |
| rangeUnderflow  | Set to true, if an element's value is less than its min attribute.       |
| stepMismatch    | Set to true, if an element's value is invalid per its step attribute.    |
| tooLong         | Set to true, if an element's value exceeds its maxLength attribute.      |
| typeMismatch    | Set to true, if an element's value is invalid per its type attribute.    |
| valueMissing    | Set to true, if an element (with a required attribute) has no value.     |
| valid           | Set to true, if an element's value is valid.                             |

# History
## History Object Properties

| Property | Description                                    |
| -------- | ---------------------------------------------- |
| length   | Returns the number of URLs in the history list |

## History Object Methods

| Method    | Description                                |
| --------- | ------------------------------------------ |
| back()    | Loads the previous URL in the history list |
| forward() | Loads the next URL in the history list     |
| go()      | Loads a specific URL from the history list |

# Storage
## Storage Object Properties and Methods

| Property/Method             | Description                                                              |
| --------------------------- | ------------------------------------------------------------------------ |
| key(_n_)                    | Returns the name of the _n_th key in the storage                         |
| length                      | Returns the number of data items stored in the Storage object            |
| getItem(_keyname_)          | Returns the value of the specified key name                              |
| setItem(_keyname_, _value_) | Adds a key to the storage, or updates a key value (if it already exists) |
| removeItem(_keyname_)       | Removes that key from the storage                                        |
| clear()                     | Empty all key out of the storage                                         |

## Related Pages for Web Storage API

| Property              | Description                                                                              |
| --------------------- | ---------------------------------------------------------------------------------------- |
| window.localStorage   | Allows to save key/value pairs in a web browser. Stores the data with no expiration date |
| window.sessionStorage | Allows to save key/value pairs in a web browser. Stores the data for one session         |

# Web Worker
```js
let w;  
  
function startWorker() {  
	if (typeof(w) == "undefined") {  
		w = new Worker("demo_workers.js");  
  }  
	w.onmessage = function(event) {  
		document.getElementById("result").innerHTML = event.data;  
  };  
}  
  
function stopWorker() {  
	w.terminate();  
	w = undefined;  
}
```

# Fetch

# Geolocation
```js
const x = document.getElementById("demo");

function getLocation() {
	if (navigator.geolocation) {
		navigator.geolocation.getCurrentPosition(showPosition, showError);
	} else { 
		x.innerHTML = "Geolocation is not supported by this browser.";
  }
}

function showPosition(position) {
	x.innerHTML = "Latitude: " + position.coords.latitude + "<br>Longitude: " + position.coords.longitude;
}

function showError(error) {
	switch(error.code) {
	case error.PERMISSION_DENIED:
		  x.innerHTML = "User denied the request for Geolocation."
		break;
	case error.POSITION_UNAVAILABLE:
		x.innerHTML = "Location information is unavailable."
		break;
	case error.TIMEOUT:
		x.innerHTML = "The request to get user location timed out."
		break;
	case error.UNKNOWN_ERROR:
		x.innerHTML = "An unknown error occurred."
		break;
  }
}
```

## The getCurrentPosition() Method - Return Data

| Property                | Returns                                                                 |
| ----------------------- | ----------------------------------------------------------------------- |
| coords.latitude         | The latitude as a decimal number (always returned)                      |
| coords.longitude        | The longitude as a decimal number (always returned)                     |
| coords.accuracy         | The accuracy of position (always returned)                              |
| coords.altitude         | The altitude in meters above the mean sea level (returned if available) |
| coords.altitudeAccuracy | The altitude accuracy of position (returned if available)               |
| coords.heading          | The heading as degrees clockwise from North (returned if available)     |
| coords.speed            | The speed in meters per second (returned if available)                  |
| timestamp               | The date/time of the response (returned if available)                   |