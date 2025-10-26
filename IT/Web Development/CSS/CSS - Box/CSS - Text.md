# Text
```css
body {
	color: red;
	text-align: left / right / center / justify; /*Set horizontal alignment*/
	text-align-last: auto / left / right / center / justify / start / end; /*Align the last line*/
	vertical-align: baseline / length / % / sub / super / top / text-top / middle / bottom / text-bottom; /*Vertical alignment of an element in a line */
	direction: rtl / ltr;
	unicode-bidi: bidi-override; /*Always together with direction*/
	
	text-decoration: text-decoration-line text-decoration-color text-decoration-style text-decoration-thickness | initial | inherit | none;
	
	text-decoration-line: none | underline | overline | line-through | initial | inherit;
	text-decoration-color: color | initial | inherit;
	text-decoration-style: solid | double | dotted | dashed | wavy | initial | inherit;
	text-decoration-thickness: auto |from-font | length / percentage | initial | inherit;
	
	text-transform: none | capitalize | uppercase | lowercase | initial | inherit;
	text-indent: length | initial | inherit;
	letter-spacing: normal | length | initial | inherit;
	line-height: normal | number | length | initial | inherit;
	word-spacing: normal | number | length | initial | inherit;
	white-space: normal | nowrap | pre | pre-line | pre-wrap | initial | inherit;
	
	text-shadow: h-shadow v-shadow blur-radius color | none | initial | # inherit;
}
```

# Fonts

```html
<link rel="stylesheet" href="https://fonts.googleapis.com/css?family=Audiowide">**  

<style>  
	body {  font-family: "Audiowide", sans-serif;}  
</style>  

```

```css
* {
	  font: font-style font-variant font-weight font-size/line-height font-family | caption | icon | menu | message-box | small-caption | status-bar | initial | inherit;
  
	font-family: family-name | generic-family | initial | inherit; 
	font-style: normal | italic | oblique | initial | inherit;
	font-weight: normal | bold | bolder | lighter | number | initial | inherit;
	font-variant: normal | small-caps | initial | inherit;
	font-size: medium | xx-small | x-small | small | large | x-large | xx-large | smaller | larger | length | initial | inherit;
}
```

> **Web Safe Fonts**
Arial (sans-serif)
Verdana (sans-serif)
Tahoma (sans-serif)
Trebuchet MS (sans-serif)
Times New Roman (serif)
Georgia (serif)
Garamond (serif)
Courier New (monospace)
Brush Script MT (cursive)

## Web Fonts
```css
@font-face {
	font-family: ;
	src: ;
	font-stretch: ;
	font-style: ;
	font-weight: ;
	unicode-range: ;
}
```

# Icons
```html
<script src="https://kit.fontawesome.com/a076d05399.js" crossorigin="anonymous"></script>
```

# Text Effects
```css
body {
	text-overflow: clip | ellipsis | string | initial | inherit;
	word-wrap: normal | break-word | initial | inherit;
	word-break: normal | break-all | keep-all | break-word | initial | inherit;
	writing-mode: horizontal-tb | vertical-rl | vertical-lr;
}
```

# Multiple Columns
```css
div {
	column-count: number | auto | initial | inherit;
	column-gap: length |normal | initial | inherit;
	
	column-rule: column-rule-width column-rule-style column-rule-color | initial | inherit;
	column-rule-style: none | hidden | dotted | dashed | solid | double | groove | ridge | inset | outset | initial | inherit;
	column-rule-width: medium | thin | thick | length | initial | inherit;
	column-rule-color: color | initial | inherit;
	
	column-span: none | all | initial | inherit;
	column-width: auto | length | initial | inherit;
}
```