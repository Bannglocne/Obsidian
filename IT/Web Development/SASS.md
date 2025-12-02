```scss
$myColor: red;  
  
h1 {
	$myColor: green !global;
	color: $myColor //green
}
  
p { 
	color: $myColor; //green
}  
```

# Nesting
```scss
nav {  
	ul {    
		color: red;  
	}  
	li {    
		margin: 0;  
	}  
}
```

```scss
font: {  
	family: Helvetica, sans-serif;  
	weight: bold;
}
```

# @import
Import .scss file into another .scss file

`reset.scss`
```scss 
html,  body,  ul,  ol {  
	margin: 0;  
	padding: 0;
}
```

`standard.scss`
```scss
@import "reset";  
  
body {  
	font-family: Helvetica, sans-serif;  
	font-size: 18px;  
	color: red;
  }
```

# Sass Partials
Start  a file name with `_`, Sass will note transpile it.
`_colors.scss:`
```scss
$myPink: #EE82EE;  
$myBlue: #4169E1;  
$myGreen: #8FBC8F;
```

```scss
@import "colors";  
  
body {  
	font-family: Helvetica, sans-serif;  
	font-size: 18px;  
	color: $myBlue;
  }
```

# @mixin
Create CSS code that is to be reused throughout the website.
```scss
@mixin name {  
	property: value;  
	property: value;  
	...
}
```

Include a mixin.
```scss
selector {
	@include mixin-name;
}
```

We can pass variables to a mixin
```scss
@mixin name($var1: value1, $var3) {
	property: $var1 value2 $var3;
}  
  
.selector {
	@include bordered(value1, value3);
}
```

# @extend
Share a set of CSS properties from one selector to another
```scss
selector1  { 
	ppt1: value1;  
	ppt2: value2;  
}  
  
selector2  {
	@extend selector1;  
	ppt3: value3;
}  
```

# Function

## String
| Function                                | Description & Example                                                                                                                                                                     |
| --------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| quote(_string_)                         | Adds quotes to _string_, and returns the result.  <br>  <br>**Example:**  <br>quote(Hello world!)  <br>Result: "Hello world!"                                                             |
| str-index(_string_, _substring_)        | Returns the index of the first occurrence of the _substring_ within _string_.  <br>  <br>**Example:**  <br>str-index("Hello world!", "H")  <br>Result: 1                                  |
| str-insert(_string_, _insert_, _index_) | Returns _string_ with _insert_ inserted at the specified _index_ position.  <br>  <br>**Example:**  <br>str-insert("Hello world!", " wonderful", 6)  <br>Result: "Hello wonderful world!" |
| str-length(_string_)                    | Returns the length of _string_ (in characters).  <br>  <br>**Example:**  <br>str-length("Hello world!")  <br>Result: 12                                                                   |
| str-slice(_string_, _start_, _end_)     | Extracts characters from _string_; start at _start_ and end at _end_, and returns the slice.  <br>  <br>**Example:**  <br>str-slice("Hello world!", 2, 5)  <br>Result: "ello"             |
| to-lower-case(_string_)                 | Returns a copy of _string_ converted to lower case.  <br>  <br>**Example:**  <br>to-lower-case("Hello World!")  <br>Result: "hello world!"                                                |
| to-upper-case(_string_)                 | Returns a copy of _string_ converted to upper case.  <br>  <br>**Example:**  <br>to-upper-case("Hello World!")  <br>Result: "HELLO WORLD!"                                                |
| unique-id()                             | Returns a unique randomly generated unquoted string (guaranteed to be unique within the current sass session).  <br>  <br>**Example:**  <br>unique-id()  <br>Result: tyghefnsv            |
| unquote(_string_)                       | Removes quotes around _string_ (if any), and returns the result.  <br>  <br>**Example:**  <br>unquote("Hello world!")  <br>Result: Hello world!                                           |

## Numeric
| Function                   | Description & Example                                                                                                                                                                                              |
| -------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| abs(_number_)              | Returns the absolute value of _number_.  <br>  <br>**Example:**  <br>abs(15)  <br>Result: 15  <br>abs(-15)  <br>Result: 15                                                                                         |
| ceil(_number_)             | Rounds _number_ up to the nearest integer.  <br>  <br>**Example:**  <br>ceil(15.20)  <br>Result: 16                                                                                                                |
| comparable(_num1_, _num2_) | Returns whether _num1_ and _num2_ are comparable.  <br>  <br>**Example:**  <br>comparable(15px, 10px)  <br>Result: true  <br>comparable(20mm, 1cm)  <br>Result: true  <br>comparable(35px, 2em)  <br>Result: false |
| floor(_number_)            | Rounds _number_ down to the nearest integer.  <br>  <br>**Example:**  <br>floor(15.80)  <br>Result: 15                                                                                                             |
| max(_number..._)           | Returns the highest value of several numbers.  <br>  <br>**Example:**  <br>max(5, 7, 9, 0, -3, -7)  <br>Result: 9                                                                                                  |
| min(_number..._)           | Returns the lowest value of several numbers.  <br>  <br>**Example:**  <br>min(5, 7, 9, 0, -3, -7)  <br>Result: -7                                                                                                  |
| percentage(_number_)       | Converts _number_ to a percentage (multiplies the number with 100).  <br>  <br>**Example:**  <br>percentage(1.2)  <br>Result: 120                                                                                  |
| random()                   | Returns a random number between 0 and 1.  <br>  <br>**Example:**  <br>random()  <br>Result: 0.45673                                                                                                                |
| random(_number_)           | Returns a random integer between 1 and _number_.  <br>  <br>**Example:**  <br>random(6)  <br>Result: 4                                                                                                             |
| round(_number_)            | Rounds _number_ to the nearest integer.  <br>  <br>**Example:**  <br>round(15.20)  <br>Result: 15  <br>round(15.80)  <br>Result: 16                                                                                |

## List
| Function                                         | Description & Example                                                                                                                                                                                                                                                                                                                                                                                                 |
| ------------------------------------------------ | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| append(_list_, _value_, [_separator_])           | Adds a single _value_ to the end of the list. _separator_ can be auto, comma, or space. auto is default.  <br>  <br>**Example:  <br>**append((a b c), d)  <br>Result: a b c d  <br>append((a b c), (d), comma)  <br>Result: a, b, c, d                                                                                                                                                                                |
| index(_list_, _value_)                           | Returns the index position for the _value_ in list.  <br>  <br>**Example:**  <br>index(a b c, b)  <br>Result: 2  <br>index(a b c, f)  <br>Result: null                                                                                                                                                                                                                                                                |
| is-bracketed(_list_)                             | Checks whether the list has square brackets.  <br>  <br>**Example:**  <br>is-bracketed([a b c])  <br>Result: true  <br>is-bracketed(a b c)  <br>Result: false                                                                                                                                                                                                                                                         |
| join(_list1_, _list2_, [_separator, bracketed_]) | Appends _list2_ to the end of _list1_. _separator_ can be auto, comma, or space. auto is default (will use the separator in the first list). _bracketed_ can be auto, true, or false. auto is default.  <br>  <br>**Example:**  <br>join(a b c, d e f)  <br>Result: a b c d e f  <br>join((a b c), (d e f), comma)  <br>Result: a, b, c, d, e, f  <br>join(a b c, d e f, $bracketed: true)  <br>Result: [a b c d e f] |
| length(_list_)                                   | Returns the length of the list.  <br>  <br>**Example:**  <br>length(a b c)  <br>Result: 3                                                                                                                                                                                                                                                                                                                             |
| list-separator(_list_)                           | Returns the list separator used, as a string. Can be either space or comma.  <br>  <br>**Example:**  <br>list-separator(a b c)  <br>Result: "space"  <br>list-separator(a, b, c)  <br>Result: "comma"                                                                                                                                                                                                                 |
| nth(_list_, _n_)                                 | Returns the _n_th element in the list.  <br>  <br>**Example:**  <br>nth(a b c, 3)  <br>Result: c                                                                                                                                                                                                                                                                                                                      |
| set-nth(_list_, _n_, _value_)                    | Sets the _n_th list element to the _value_ specified.  <br>  <br>**Example:**  <br>set-nth(a b c, 2, x)  <br>Result: a x c                                                                                                                                                                                                                                                                                            |
| zip(_lists_)                                     | Combines lists into a single multidimensional list.  <br>  <br>**Example:**  <br>zip(1px 2px 3px, solid dashed dotted, red green blue)  <br>Result: 1px solid red, 2px dashed green, 3px dotted blue                                                                                                                                                                                                                  |

## Map
| Function                     | Description & Example                                                                                                                                                                                                                                                                                                       |
| ---------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| map-get(_map_, _key_)        | Returns the value for the specified _key_ in the map.  <br>  <br>**Example:**  <br>$font-sizes: ("small": 12px, "normal": 18px, "large": 24px)  <br>map-get($font-sizes, "small")  <br>Result: 12px                                                                                                                         |
| map-has-key(_map_, _key_)    | Checks whether _map_ has the specified _key_. Returns true or false.  <br>  <br>**Example:**  <br>$font-sizes: ("small": 12px, "normal": 18px, "large": 24px)  <br>map-has-key($font-sizes, "big")  <br>Result: false                                                                                                       |
| map-keys(_map_)              | Returns a list of all keys in _map_.  <br>  <br>**Example:**  <br>$font-sizes: ("small": 12px, "normal": 18px, "large": 24px)  <br>map-keys($font-sizes)  <br>Result: "small", "normal, "large"                                                                                                                             |
| map-merge(_map1_, _map2_)    | Appends _map2_ to the end of _map1_.  <br>  <br>**Example:**  <br>$font-sizes: ("small": 12px, "normal": 18px, "large": 24px)  <br>$font-sizes2: ("x-large": 30px, "xx-large": 36px)  <br>map-merge($font-sizes, $font-sizes2)  <br>Result: "small": 12px, "normal": 18px, "large": 24px, "x-large": 30px, "xx-large": 36px |
| map-remove(_map_, _keys..._) | Removes the specified keys from _map_.  <br>  <br>**Example:**  <br>$font-sizes: ("small": 12px, "normal": 18px, "large": 24px)  <br>map-remove($font-sizes, "small")  <br>Result: ("normal": 18px, "large": 24px)  <br>map-remove($font-sizes, "small", "large")  <br>Result: ("normal": 18px)                             |
| map-values(_map_)            | Returns a list of all values in _map_.  <br>  <br>**Example:**  <br>$font-sizes: ("small": 12px, "normal": 18px, "large": 24px)  <br>map-values($font-sizes)  <br>Result: 12px, 18px, 24px                                                                                                                                  |

## Selector
| Function                                                | Description & Example                                                                                                                                                                                                                                                                       |
| ------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| is-superselector(_super_, _sub_)                        | Checks whether the _super_ selector matches all the elements that _sub_ matches.  <br>  <br>**Example:**  <br>is-superselector("div", "div.myInput")  <br>Result: true  <br>is-superselector("div.myInput", "div")  <br>Result: false  <br>is-superselector("div", "div")  <br>Result: true |
| selector-append(_selectors_)                            | Appends the second (and third/fourth etc.) selector to the first selector.  <br>  <br>**Example:**  <br>selector-append("div", ".myInput")  <br>Result: div.myInput  <br>selector-append(".warning", "__a")  <br>Result: .warning__a                                                        |
| selector-extend(_selector_, _extendee_, _extender_)     |                                                                                                                                                                                                                                                                                             |
| selector-nest(_selectors_)                              | Returns a new selector containing a nested list of CSS selectors based on the list provided.  <br>  <br>**Example:**  <br>selector-nest("ul", "li")  <br>Result: ul li  <br>selector-nest(".warning", "alert", "div")  <br>Result: .warning div, alert div                                  |
| selector-parse(_selector_)                              | Returns a list of strings contained in _selector_ using the same format as the parent selector.  <br>  <br>**Example:  <br>**selector-parse("h1 .myInput .warning")  <br>Result: ('h1' '.myInput' '.warning')                                                                               |
| selector-replace(_selector_, _original_, _replacement_) | Returns a new selector with the selectors specified in _replacement_ in place of selectors specified in _original_.  <br>  <br>**Example:**  <br>selector-replace("p.warning", "p", "div")  <br>Result: div.warning                                                                         |
| selector-unify(_selector1_, _selector2_)                | Returns a new selector that matches only elements matched by both _selector1_ and _selector2_.  <br>  <br>**Example:**  <br>selector-unify("myInput", ".disabled")  <br>Result: myInput.disabled  <br>selector-unify("p", "h1")  <br>Result: null                                           |
| simple-selectors(_selectors_)                           | Returns a list of the individual selectors in _selectors_.  <br>  <br>**Example:**  <br>simple-selectors("div.myInput")  <br>Result: div, .myInput  <br>simple-selectors("div.myInput:before")  <br>Result: div, .myInput, :before                                                          |

## Introspection 
| Function                                 | Description & Example                                                                                                                                                                                        |
| ---------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| call(_function_, _arguments_...)         | Calls a function with arguments, and returns the result.                                                                                                                                                     |
| content-exists()                         | Checks whether the current mixin was passed a @content block.                                                                                                                                                |
| feature-exists(_feature_)                | Checks whether _feature_ is supported by the current Sass implementation.  <br>  <br>**Example:**  <br>feature-exists("at-error");  <br>Result: true                                                         |
| function-exists(_functionname_)          | Checks whether the specified function exists.  <br>  <br>**Example:**  <br>function-exists("nonsense")  <br>Result: false                                                                                    |
| get-function(_functionname_, css: false) | Returns the specified function. If css is true, it returns a plain CSS function instead.                                                                                                                     |
| global-variable-exists(_variablename_)   | Checks whether the specified global variable exists.  <br>  <br>**Example:**  <br>variable-exists(a)  <br>Result: true                                                                                       |
| inspect(_value_)                         | Returns a string representation of _value_.                                                                                                                                                                  |
| mixin-exists(_mixinname_)                | Checks whether the specified mixin exists.  <br>  <br>**Example:**  <br>mixin-exists("important-text")  <br>Result: true                                                                                     |
| type-of(_value_)                         | Returns the type of _value_. Can be number, string, color, list, map, bool, null, function, arglist.  <br>  <br>**Example:**  <br>type-of(15px)  <br>Result: number  <br>type-of(#ff0000)  <br>Result: color |
| unit(_number_)                           | Returns the unit associated with a number.  <br>  <br>**Example:**  <br>unit(15px)  <br>Result: px                                                                                                           |
| unitless(_number_)                       | Checks whether the specified number has a unit associated with it.  <br>  <br>**Example:**  <br>unitless(15px)  <br>Result: false  <br>unitless(15)  <br>Result: true                                        |
| variable-exists(_variablename_)          | Checks whether the specified variable exists in the current scope.  <br>  <br>**Example:**  <br>variable-exists(b)  <br>Result: true                                                                         |

## Color
| Function                                        | Description & Example                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| ----------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| rgb(_red_, _green_, _blue_)                     | Sets a color using the Red-Green-Blue (RGB) model. An RGB color value is specified with: rgb(red, green, blue). Each parameter defines the intensity of that color and can be an integer between 0 and 255, or a percentage value (from 0% to 100%).  <br>  <br>**Example:**  <br>rgb(0, 0, 255); // rendered as blue because the blue parameter is set to its highest value (255) and the others are set to 0                                                                                                                                                           |
| rgba(_red_, _green_, _blue_, _alpha_)           | Sets a color using the Red-Green-Blue-Alpha (RGBA) model. RGBA color values are an extension of RGB color values with an alpha channel - which specifies the opacity of the color. The alpha parameter is a number between 0.0 (fully transparent) and 1.0 (fully opaque).  <br>  <br>**Example:**  <br>rgba(0, 0, 255, 0.3); // rendered as blue with opacity                                                                                                                                                                                                           |
| hsl(_hue_, _saturation_, _lightness_)           | Sets a color using the Hue-Saturation-Lightness (HSL) model - and represents a cylindrical-coordinate representation of colors. Hue is a degree on the color wheel (from 0 to 360) - 0 or 360 is red, 120 is green, 240 is blue. Saturation is a percentage value; 0% means a shade of gray and 100% is the full color. Lightness is also a percentage; 0% is black, 100% is white.  <br>  <br>**Example:**  <br>hsl(120, 100%, 50%); // green  <br>hsl(120, 100%, 75%); // light green  <br>hsl(120, 100%, 25%); // dark green  <br>hsl(120, 60%, 70%); // pastel green |
| hsla(_hue_, _saturation_, _lightness_, _alpha_) | Sets a color using the Hue-Saturation-Lightness-Alpha (HSLA) model. HSLA color values are an extension of HSL color values with an alpha channel - which specifies the opacity of the color. The alpha parameter is a number between 0.0 (fully transparent) and 1.0 (fully opaque).  <br>  <br>**Example:**  <br>hsl(120, 100%, 50%, 0.3); // green with opacity  <br>hsl(120, 100%, 75%, 0.3); // light green with opacity                                                                                                                                             |
| grayscale(_color_)                              | Sets a gray color with the same lightness as _color_.  <br>  <br>**Example:**  <br>grayscale(#7fffd4);  <br>Result: `#c6c6c6`                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| complement(_color_)                             | Sets a color that is the complementary color of _color_.  <br>  <br>**Example:**  <br>complement(#7fffd4);  <br>Result: `#ff7faa`                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| invert(_color_, _weight_)                       | Sets a color that is the inverse or negative color of _color_. The _weight_ parameter is optional and must be a number between 0% and 100%. Default is 100%.  <br>  <br>**Example:**  <br>invert(white);  <br>Result: black                                                                                                                                                                                                                                                                                                                                              |

| Function            | Description & Example                                                                                                                                            |
| ------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| red(_color_)        | Returns the red value of _color_ as a number between 0 and 255.  <br>  <br>**Example:**  <br>red(#7fffd4);  <br>Result: 127  <br>red(red);  <br>Result: 255      |
| green(_color_)      | Returns the green value of _color_ as a number between 0 and 255.  <br>  <br>**Example:**  <br>green(#7fffd4);  <br>Result: 255  <br>green(blue);  <br>Result: 0 |
| blue(_color_)       | Returns the blue value of _color_ as a number between 0 and 255.  <br>  <br>**Example:**  <br>blue(#7fffd4);  <br>Result: 212  <br>blue(blue);  <br>Result: 255  |
| hue(_color_)        | Returns the hue of _color_ as a number between 0deg and 360deg.  <br>  <br>**Example:**  <br>hue(#7fffd4);  <br>Result: 160deg                                   |
| saturation(_color_) | Returns the HSL saturation of _color_ as a number between 0% and 100%.  <br>  <br>**Example:**  <br>saturation(#7fffd4);  <br>Result: 100%                       |
| lightness(_color_)  | Returns the HSL lightness of _color_ as a number between 0% and 100%.  <br>  <br>**Example:**  <br>lightness(#7fffd4);  <br>Result: 74.9%                        |
| alpha(_color_)      | Returns the alpha channel of _color_ as a number between 0 and 1.  <br>  <br>**Example:**  <br>alpha(#7fffd4);  <br>Result: 1                                    |
| opacity(_color_)    | Returns the alpha channel of _color_ as a number between 0 and 1.  <br>  <br>**Example:**  <br>opacity(rgba(127, 255, 212, 0.5));  <br>Result: 0.5               |

| Function                                                                                 | Description & Example                                                                                                                                                                                                                            |
| ---------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| mix(_color1_, _color2_, _weight_)                                                        | Creates a color that is a mix of _color1_ and _color2_. The _weight_ parameter must be between 0% and 100%. A larger weight means that more of color1 should be used. A smaller weight means that more of color2 should be used. Default is 50%. |
| adjust-hue(_color_, _degrees_)                                                           | Adjusts the _color_'s hue with a degree from -360deg to 360deg.  <br>  <br>**Example:**  <br>adjust-hue(#7fffd4, 80deg);  <br>Result: `#8080ff`                                                                                           |
| adjust-color(_color_, _red_, _green_, _blue_, _hue_, _saturation_, _lightness_, _alpha_) | Adjusts one or more parameters by the specified amount. This function adds or subtracts the specified amount to/from the existing color value.  <br>  <br>**Example:**  <br>adjust-color(#7fffd4, blue: 25);  <br>Result:                        |
| change-color(_color_, _red_, _green_, _blue_, _hue_, _saturation_, _lightness_, _alpha_) | Sets one or more parameters of a _color_ to new values.  <br>  <br>**Example:**  <br>change-color(#7fffd4, red: 255);  <br>Result: `#ffffd4`                                                                                                       |
| scale-color(_color_, _red_, _green_, _blue_,  _saturation_, _lightness_, _alpha_)        | Scales one or more parameters of _color_.                                                                                                                                                                                                        |
| rgba(_color_, _alpha_)                                                                   | Creates a new color of _color_ with the given _alpha_ channel.  <br>  <br>**Example:**  <br>rgba(#7fffd4, 30%);  <br>Result: rgba(127, 255, 212, 0.3)                                                                                            |
| lighten(_color_, _amount_)                                                               | Creates a lighter color of _color_ with an _amount_ between 0% and 100%. The amount parameter increases the HSL lightness by that percent.                                                                                                       |
| darken(_color_, _amount_)                                                                | Creates a darker color of _color_ with an _amount_ between 0% and 100%. The amount parameter decreases the HSL lightness by that percent.                                                                                                        |
| saturate(_color_, _amount_)                                                              | Creates a more saturated color of _color_ with an _amount_ between 0% and 100%. The amount parameter increases the HSL saturation by that percent.                                                                                               |
| desaturate(_color_, _amount_)                                                            | Creates a less saturated color of _color_ with an _amount_ between 0% and 100%. The amount parameter decreases the HSL saturation by that percent.                                                                                               |
| opacify(_color_, _amount_)                                                               | Creates a more opaque color of _color_ with an _amount_ between 0 and 1. The amount parameter increases the alpha channel by that amount.                                                                                                        |
| fade-in(_color_, _amount_)                                                               | Creates a more opaque color of _color_ with an _amount_ between 0 and 1. The amount parameter increases the alpha channel by that amount.                                                                                                        |
| transparentize(_color_, _amount_)                                                        | Creates a more transparent color of _color_ with an _amount_ between 0 and 1. The amount parameter decreases the alpha channel by that amount.                                                                                                   |
| fade-out(_color_, _amount_)                                                              | Creates a more transparent color of _color_ with an _amount_ between 0 and 1. The amount parameter decreases the alpha channel by that amount.                                                                                                   |