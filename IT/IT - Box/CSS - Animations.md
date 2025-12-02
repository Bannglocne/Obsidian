# Transforms
```css
body {
	transform: none | matrix(n,n,n,n,n,n) | matrix3d(n,n,n,n,n,n,n,n,n,n,n,n,n,n,n,n) | translate(x,y) | translate3d(x,y,z) | translateX(x) | translateY(y) | translateZ(z) | scale(x,y) | scale3d(x,y,z) | scaleX(x) | scaleY(y) | scaleZ(z) | rotate(angle) | rotate3d(x,y,z,angle) | rotateX(angle) | rotateY(angle) | rotateZ(angle) | skew(ax,ay) | skewX(a) | skewY(a) | perspective(n) | initial | inherit;
} 
```

# Transition
```css
body {
	transition: property duration timing-function delay | initial | inherit;
}
```

# Animations
```css
@keyframes name {  
	keyframes-selector {css-styles;}  
	keyframes-selector {css-styles;}  
  ...  
}

body {
	animation: name duration timing-function delay iteration-count direction fill-mode play-state;
	animation-name: keyframename| none | initial | inherit;
	animation-duration: time | initial | inherit;
	animation-delay: time | initial | inherit;
	animation-iteration-count: number | infinite | initial | inherit;
	animation-direction: normal | reverse | alternate | alternate-reverse | initial | inherit;
	animation-timing-function: linear | ease | ease-in | ease-out | ease-in-out | step-start | step-end | steps(int,start|end) | cubic-bezier(n,n,n,n) | initial | inherit;
	animation-fill-mode: none | forwards | backwards | both | initial | inherit;
} 
```