# Selector
```css
* {  }
#id { }
.class { }
p.class { }
```

# Combinator
```css
div p { } /*Descendant*/
div > p { } /*Child*/
div + p { } /*Next Sibling*/
div ~ p { } /*Subsequent-sibling*/
div, p { } /* Selector list */
namespace|element { } /* Namespace*/
```
# Pseduo
```css
selector:pseudo-class-name {  
	CSS properties
}
```

```css
selector::pseudo-element-name {  
	CSS properties
}
```

# Attribute Selectors
Select elements with a specific attribute.
```css
[target] { }
[target="_blank"] { } /*Exact value*/
[title~="flower"] { } /*Contain a specific word*/
[class|="top"] { } /*Start with word (or have -)*/
[class^="top"] { } /*Start with word*/
[class$="test"] { } /*End with word*/
[class*="te"] { } /*Contain a specific text*/
``` 


