
> [!NOTE] AJAX
>- **A**synchronous **J**avaScript **A**nd **X**ML.
>- Read data from a web server - after the page has loaded
>- Update a web page without reloading the page
>- Send data to a web server - in the background

# XMLHttpRequest Object
> 1. Create an XMLHttpRequest object
>2. Define a callback function
>3. Open the XMLHttpRequest object
>4. Send a Request to a server

```js
variable = new XMLHttpRequest();

xhttp.onload = function() {  
	// What to do when the response is ready  
}

xhttp.open("GET", "ajax_info.txt", true);  // "Post", false
xhttp.send();
```

## Methods
| Method                                | Description                                                                                                                                                                                                                  |
| ------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| new XMLHttpRequest()                  | Creates a new XMLHttpRequest object                                                                                                                                                                                          |
| abort()                               | Cancels the current request                                                                                                                                                                                                  |
| getAllResponseHeaders()               | Returns header information                                                                                                                                                                                                   |
| getResponseHeader()                   | Returns specific header information                                                                                                                                                                                          |
| open(_method, url, async, user, psw_) | Specifies the request  <br>  <br>_method_: the request type GET or POST  <br>_url_: the file location  <br>_async_: true (asynchronous) or false (synchronous)  <br>_user_: optional user name  <br>_psw_: optional password |
| send()                                | Sends the request to the server  <br>Used for GET requests                                                                                                                                                                   |
| send(_string_)                        | Sends the request to the server.  <br>Used for POST requests                                                                                                                                                                 |
| setRequestHeader()                    | Adds a label/value pair to the header to be sent                                                                                                                                                                             |

## Properties
| Property           | Description                                                                                                                                                                                                         |
| ------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| onload             | Defines a function to be called when the request is received (loaded)                                                                                                                                               |
| onreadystatechange | Defines a function to be called when the readyState property changes                                                                                                                                                |
| readyState         | Holds the status of the XMLHttpRequest.  <br>0: request not initialized  <br>1: server connection established  <br>2: request received  <br>3: processing request  <br>4: request finished and response is ready    |
| responseText       | Returns the response data as a string                                                                                                                                                                               |
| responseXML        | Returns the response data as XML data                                                                                                                                                                               |
| status             | Returns the status-number of a request  <br>200: "OK"  <br>403: "Forbidden"  <br>404: "Not Found"  <br>For a complete list go to the [Http Messages Reference](https://www.w3schools.com/tags/ref_httpmessages.asp) |
| statusText         | Returns the status-text (e.g. "OK" or "Not Found")                                                                                                                                                                  |

**Multiple Callback Functions**
```js
loadDoc("_url-1_", myFunction1);  
loadDoc("_url-2_", myFunction2);  
  
function loadDoc(url, cFunction) {  
	const xhttp = new XMLHttpRequest();  
	xhttp.onload = function() {cFunction(this);}  
	xhttp.open("GET", url);  
	xhttp.send();  
}  
  
function myFunction1(xhttp) {  
	// action goes here  
}  
function myFunction2(xhttp) {  
	// action goes here  
}
```

# Request
