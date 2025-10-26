**Selector:** [[CSS - Selector]]

# Import
```html
<link rel="stylesheet" href="mystyle.css">
<style> </style>
<p style="atr:value"> </p>
```

# Comments
```css
/* CSS Comment */
```

# Cascading Order
1. Importance `!important`
2. Specificity:

| Selector                                        | Description                                         |
| ----------------------------------------------- | --------------------------------------------------- |
| Inline styles                                   | Highest priority, will override all other selectors |
| Id selectors                                    | Second highest priority                             |
| Classes, attribute selectors and pseudo-classes | Third highest priority                              |
| Elements and pseudo-elements                    | Low priority                                        |
| Universal selector and :where()                 | No priority                                         |
3. Source Order

# Width & Height
- Value:
	- `auto` - Default
	- `length` - px, cm, em, etc
	- `%` - % of the containing block
	- `initial` - Its default value
	- `inherit` - From its parent value

- `max-width`: length / % / none

# Math Functions
```css
calc()
max(); min(); clamp()
round(); mod(); progress(); rem()
sin(); cos(); tan(); asin(); acos(); atan();atan2()
pow(); sqrt(); hypot(); log(); exp()
abs(); sign()
```

# Variables
```css
:root {  
	--blue: #1e90ff;  
	--white: #ffffff;
}

body {background-color: var(--blue);}
```

# @property
```css
@property --propertyname {
	syntax: "<color>";  
	initial-value: red;  
	inherits: false;  
}
```

# Counter
```css
body {
	counter-reset: none | name_number | initial | inherit;
}

h1::before {
	counter-increment: name_number number;
	content: "Section" counter(name) ". ";
}
```