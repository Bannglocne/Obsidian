```html
<img src="_url_" alt="_alternatetext_">
```

# Map 
Clickable areas on an image
```html
<img src="map.jpg" usemap="#map">  
  
<map name="map">  
  <area shape="rect" coords="34,44,270,350" href="computer.htm">  
  <area shape="circle" coords="337,300,44" href="coffee.htm">
  <area shape="poly" coords="140,121,181,116,204,160,204,222,191,270,140,329,85,355,58,352,37,322,40,259,103,161,128,147" href="croissant.htm">
</map>
```
![[croissant_map.png]]

# Background Images
```html
<style>  
body {  background-image: url('img.jpg');}  
</style>
```

> Auto repeat itself if background image is smaller than element. Using `background-repeat: no-repeat;` to avoid this.

- Cover: May lose part of the image
```html
<style>  
body {  background-image: url('img_girl.jpg');  
  background-attachment: fixed;  
  background-size: cover;}  
</style
```
- Stretch: 
```html
<style>  
body {  background-image: url('img_girl.jpg');  
  background-repeat: no-repeat;  
  background-attachment: fixed;  
  background-size: 100% 100%;}  
</style>
```

# Picture
Browser can choose the image that best fits the current view
```html
<picture>  
  <source media="(min-width: 650px)" srcset="img1.jpg">  
  <source media="(min-width: 465px)" srcset="img2.jpg">  
  <img src="img3.jpg">  
</picture>
```