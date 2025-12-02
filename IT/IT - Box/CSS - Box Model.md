**Content -> Padding -> Border -> Outline -> Margin**
# Borders

```css
body { 
border: border-width border-style border-color ;
border-radius: px px px px; 
}
```

- `border-style`
	- `dotted` 
	- `dashed` 
	- `solid` 
	- `double`
	- `groove` 
	- `ridge` 
	- `inset`
	- `outset` 
	- `none`
	- `hidden`

## Border  Images
```css
body {
	border-image: source slice width outset repeat | initial | inherit;
	border-image-source: none| url() | initial | inherit;
	border-image-slice: number | % | fill| initial | inherit;
	border-image-width: number | % | auto | initial | inherit;
	border-image-outset: length | number | initial | inherit;
	border-image-repeat: stretch | repeat | round | space | initial | inherit;
}
```

# Margins
```css
body { margin: top right bottom left / auto / inherit }
```

# Padding
```css
body { 
padding: top right bottom left; 
box-sizing: content-box / border-box;
}
```

# Outline
```css 
body {
	outline: outline-width outline-style outline-color|initial|inherit; 
	outline-offset: -5px;
}
```

# Box Sizing
```css
body {
	box-sizing: content-box | border-box | initial | inherit;
}
```