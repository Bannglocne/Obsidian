# Document
## Finding HTML Elements

| Method                                  | Description                   |
| --------------------------------------- | ----------------------------- |
| document.getElementById(_id_)           | Find an element by element id |
| document.getElementsByTagName(_name_)   | Find elements by tag name     |
| document.getElementsByClassName(_name_) | Find elements by class name   |

---

## Changing HTML Elements

| Property                                   | Description                                   |
| ------------------------------------------ | --------------------------------------------- |
| _element_.innerHTML =  _new html content_  | Change the inner HTML of an element           |
| _element_._attribute = new value_          | Change the attribute value of an HTML element |
| _element_.style._property = new style_     | Change the style of an HTML element           |
| Method                                     | Description                                   |
| _element_.setAttribute_(attribute, value)_ | Change the attribute value of an HTML element |

---

## Adding and Deleting Elements

| Method                            | Description                       |
| --------------------------------- | --------------------------------- |
| document.createElement(_element_) | Create an HTML element            |
| document.removeChild(_element_)   | Remove an HTML element            |
| document.appendChild(_element_)   | Add an HTML element               |
| document.replaceChild(_new, old_) | Replace an HTML element           |
| document.write(_text_)            | Write into the HTML output stream |

## Adding Events Handlers

| Method                                                     | Description                                   |
| ---------------------------------------------------------- | --------------------------------------------- |
| document.getElementById(_id_).onclick = function(){_code_} | Adding event handler code to an onclick event |
| onload                                                     |                                               |
| onunload                                                   |                                               |
| oninput                                                    |                                               |
| onmouseover                                                |                                               |
| onmouseout                                                 |                                               |
| onmouseup                                                  |                                               |

# Even Listener
```js
element.addEventListener(event, function, useCapture);
```