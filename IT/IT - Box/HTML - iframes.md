```html
<iframe src="demo.html" style="height:5px;width:5px;border:5px" title="Example"></iframe>
```

# Target for Link
When the **target** attribute of a link matches the **name** of an iframe, the link will open in the iframe.
```html
<iframe src="demo.html" name="iframe_a"></iframe>

<a href="https://www.w3schools.com" target="iframe_a">W3Schools.com</a>
```