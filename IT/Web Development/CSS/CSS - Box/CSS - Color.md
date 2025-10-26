- RGBA: `rgba(red, green, blue,  alpha)`
- HSLA: `hsla(hue, saturation, lightness, alpha)`

# Keyword
- `transparent`
- `currentcolor`
- `inherit`

# Gradients
```css
body {
	background-image: linear-gradient(direction, color-stop1, color-stop2, ...);
	background-image: linear-gradient(angle, color-stop1, color-stop2);
	background-image: repeating-linear-gradient(angle | to side-or-corner, color-stop1, color-stop2, ...);
}
```

```css
body {
	background-image: radial-gradient(shape size at position, start-color, ..., last-color);
	background-image: repeating-radial-gradient(shape size at position, start-color, ..., last-color);	
}
```

```css
body {
	background-image: conic-gradient([from angle] [at position,] color [degree], color [degree], ..._);
	background-image: repeating-conic-gradient([from angle] [at position,] color degree, color degree, ..._);
}
```

# Shadow
```css
body {
	text-shadow: h-shadow v-shadow blur-radius color | none | initial | inherit;
		box-shadow: none | h-offset v-offset blur spread color | inset | initial | inherit;
}
```

# Filter
```css
img {
	filter: none | blur() | brightness() | contrast() | drop-shadow() | grayscale() | hue-rotate() | invert() | opacity() | saturate() | sepia() | url();
}
```