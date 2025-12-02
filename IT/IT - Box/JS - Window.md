# Screen
- `screen.width`
- `screen.height`
- `screen.availWidth`
- `screen.availHeight`
- `screen.colorDepth`
- `screen.pixelDepth`

# Location
- `window.location.href` returns the href (URL) of the current page
- `window.location.hostname` returns the domain name of the web host
- `window.location.pathname` returns the path and filename of the current page
- `window.location.protocol` returns the web protocol used (http: or https:)
- `window.location.assign()` loads a new document

# History
- `history.back()` - same as clicking back in the browser
- `history.forward()` - same as clicking forward in the browser

# Navigator
- `navigator.cookieEnabled`
- `navigator.language`
- `navigator.onLine`
- `navigator.appName`
- `navigator.appCodeName`
- `navigator.product`
- `navigator.appVersion`
- `navigator.userAgent`
- `navigator.platform`
- `navigator.javaEnabled()`

# Popup
```js
window.alert("sometext");
window.confirm("sometext");
window.prompt("sometext","defaultText");
```

# Timing
```js
window.setTimeout(function, milliseconds);
window.clearTimeout(timeoutVariable)
clearTimeout(myVar);

window.setInterval(function, milliseconds);
window.clearInterval(timerVariable)
clearInterval(myVar);
```

# Cookies
```js
document.cookie = "username=John Doe"; // Create a Cookie
let x = document.cookie; // Read a Cookie
document.cookie = "username=John Smith"; // Change a Cookie
document.cookie = "username="; // Delete a Cookie
```

**Function to Set-Get-Check a Cookie**
```js
function setCookie(cname, cvalue, exdays) {  
	const d = new Date();  
	d.setTime(d.getTime() + (exdays * 24 * 60 * 60 * 1000));  
	let expires = "expires="+d.toUTCString();  
	document.cookie = cname + "=" + cvalue + ";" + expires + ";path=/";  
}  
  
function getCookie(cname) {  
	let name = cname + "=";  
	let ca = document.cookie.split(';');  
	for(let i = 0; i < ca.length; i++) {  
		let c = ca[i];  
		while (c.charAt(0) == ' ') {  
			  c = c.substring(1);  
		}  
		if (c.indexOf(name) == 0) {  
			  return c.substring(name.length, c.length);  
		}  
	}  
	return "";  
}  
  
function checkCookie() {  
	let user = getCookie("username");  
	if (user != "") {  
		alert("Welcome again " + user);  
	} else {  
	user = prompt("Please enter your name:", "");  
	if (user != "" && user != null) {  
		  setCookie("username", user, 365);  
    }  
  }  
}
```