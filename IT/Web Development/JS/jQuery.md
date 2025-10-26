>jQuery is a lightweight JavaScript library. Making it much easier to use JavaScript on website.

```html
<head>
	<script src="jquery-3.7.1.min.js"></script> <!--Download file in the same directory as the page where you wish to use it -->
	<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.7.1/jquery.min.js"></script>
</head>
```

# Syntax
Basic syntax is: `$(selector).action()`

**The Document Ready Event**
```js
$(function(){  
	// jQuery methods go here...
});
```

## Selector
| Syntax                      | Description                                                                  |
| --------------------------- | ---------------------------------------------------------------------------- |
| `$("*") `                   | Selects all elements                                                         |
| ` $(this)    `              | Selects the current HTML element                                             |
| `$("p.intro")    `          | Selects all` <p>` elements with class="intro"                                |
| `$("p:first")      `        | Selects the first `<p>` element                                              |
| `$("ul li:first") `         | Selects the first` <li>` element of the first `<ul>  `                       |
| ` $("ul li:first-child")`   | Selects the first` <li>` element of every `<ul> `                            |
| ` $("[href]")  `            | Selects all elements with an href attribute                                  |
| `$("a[target='_blank']")`   | Selects all `<a>` elements with a target attribute value equal to "_blank"   |
| ` $("a[target!='_blank']")` | Selects all <a> elements with a target attribute value NOT equal to "_blank" |
| `$(":button") `             | Selects all `<button>` elements and `<input>` elements of type="button"      |
| `$("tr:even") `             | Selects all even `<tr>` elements                                             |

```js
myElement.text("Hello Sweden!"); // Set Text Content
myText = $("#02").text(); // Get Text Content
myElement.html("<p>Hello World</p>"); // Set HTML Content
content = myElement.html(); // Get HTML Content
```

```js
myElement.hide(); // Hiding HTML Elements
myElement.show(); // Showing HTML Elements
$("#demo").css("font-size","35px"); // Styling HTML Elements
```

```js
$("#id02").remove(); // Removing HTML Elements
myParent = $("#02").parent().prop("nodeName"); ; // Get Parent Element
```