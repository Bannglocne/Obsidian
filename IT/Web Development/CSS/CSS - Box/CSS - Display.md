# Display
```css
* { 
	display: inline | block | contents | flex | grid | inline-block | inline-flex | inline-grid	| inline-table	| list-item	| run-in | table | table-caption | table-column-group | table-header-group | table-footer-group | table-row-group | table-cell	| table-column | table-row	| none	| initial	| inherit;
}
```

# Position
```css
* { 
	position: static | absolute | fixed | relative | sticky | initial | inherit;
}
```

# Z-Index
```css
* {
	z-index: -1;  
}
```

# Overflow
Controls what happens to content that is too big to fit into an area
```css
* {
	overflow: visible | hidden | clip | scroll | auto | initial| inherit;
	overflow-x: ;
	overflow-y: ;
	  
}
```

# Float
Specifies how an element should float within its container.
```css
body {
	float: none | left | right | initial | inherit;
}
```

# Flexbox
```css
body {
	flex-direction: row | row-reverse | column | column-reverse | initial | inherit;
	flex-wrap: nowrap | wrap | wrap-reverse | initial | inherit;
	
	flex: flex-grow flex-shrink flex-basis | auto | initial | inherit;
	flex-basis: number | auto | initial | inherit;
	flex-shrink: number | initial | inherit;
	flex-grow: number | initial | inherit;
	
}
```

```html
<div class="container">  
  <div style="order: 3">1</div>  
  <div style="order: 2">2</div>  
  <div style="order: 4">3</div>  
  <div style="order: 1">4</div>  
</div>
```

# Clear & Clearfix
```css
body {
	clear: none | left | right | both | initial | inherit;
}
```

To avoid element "overflow" outside of its container
```css
.clearfix::after {  
	content: "";  
	clear: both;  
	display: table;
  }
```

# Algin
```css
body {
	justify-content: flex-start | flex-end | center | space-between | space-around | space-evenly | initial | inherit;
}
```

```css
body {
	align-items: normal | stretch | positional alignment | flex-start | flex-end | baseline | initial | inherit;
	align-content: stretch | center | flex-start | flex-end | space-between | space-around | space-evenly | initial | inherit;
	align-self: auto | stretch | center | flex-start | flex-end | baseline | initial | inherit;
```

# Shapes
```css
img {
	clip-path: clip-source | basic-shape | margin-box | border-box | padding-box | content-box | fill-box | stroke-box | view-box | none | initial | inherit;
	shape-outside: none | margin-box | border-box | padding-box | content-box | basic-shape | url(image) | initial | inherit


	object-fit: fill | contain | cover | scale-down | none | initial | inherit;
	object-position: position | initial | inherit;
}
```

# Masking
```html
<style>
	.mask1 {  
		-webkit-mask-image: url(w3logo.png);  
		mask-image: url(w3logo.png);  
		mask-size: 70%;  
		mask-repeat: no-repeat;
	}
	</style>

<div class="mask1">
	<img src="img1.jpg">
</div>
```

# User Interface
```css
div {
	resize: none | both | horizontal | vertical | initial | inherit;
}
```

# Media Query
Different view for different screen size
```css
@media not|only mediatype and (media feature) and (media feature) {
  CSS-Code;
}
```

```html
<link rel="stylesheet" media="print" href="print.css">  
<link rel="stylesheet" media="screen" href="screen.css">  
<link rel="stylesheet" media="screen and (min-width: 480px)" href="example1.css">  
<link rel="stylesheet" media="screen and (min-width: 701px) and (max-width: 900px)" href="example2.css">  
```

# Grid

```css
body {
	grid-area: grid-row-start / grid-column-start / grid-row-end / grid-column-end | itemname;
	grid-column: grid-column-start / grid-column-end;
	grid-column-start: auto |span n | column-line;
	grid-column-end: auto |span n | column-line;
	grid-row: grid-row-start / grid-row-end;
	grid-row-start: auto | row-line;
	grid-row-end: auto| row-line |span n;
	
	grid-template: none| grid-template-rows / grid-template-columns | grid-template-areas | initial | inherit;
	grid-template-columns: none | auto | max-content | min-content | minmax() | length | percentage | fit-content() | repeat() | subgrid | initial | inherit;
	grid-template-rows: none | auto | max-content | min-content | minmax() | length | percentage | fit-content() | repeat() | subgrid | initial | inherit;
}
```

```css
.item1 { grid-area: header; }  
.item2 { grid-area: menu; }  
.item3 { grid-area: main; }  
.item4 { grid-area: right; }  
.item5 { grid-area: footer; }  
  
.grid-container {  
	display: grid;  
	grid-template-areas:  
	'header header header header header header'  
	'menu main main main right right'  
	'menu footer footer footer footer footer';
    }
```

## Gap
```css
body {
	gap: row-gap column-gap | initial | inherit;
}
```

# @support
If browser support property with exact value
```css
@supports (property: value) {
  /* CSS rules */
}
```