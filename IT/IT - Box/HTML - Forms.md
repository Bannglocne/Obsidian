```html
<form action="/action_page.php" target="_blank" method="post">
  <fieldset>
    <legend>Personalia:</legend>
    
    <label for="name">Name:</label><br>  
    <input type="text" id="name" name="name"><br><br>  
    
    <!-- Gender -->
    <input type="radio" id="gen1" name="gender" value="Male">  
    <label for="gen1">Male</label><br>  
    <input type="radio" id="gen2" name="gender" value="Female">  
    <label for="gen2">Female</label><br><br>  
    
    <!-- Select -->
    <label for="cars">Choose a car:</label><br>  
    <select id="cars" name="cars" size="2" multiple>  
      <option value="maybach">Maybach</option>  
      <option value="benz">Benz</option>  
    </select><br><br>
    
    <!-- Datalist -->
    <label for="cargen">Car Gen:</label>
    <input list="cargens" name="cargen" id="cargen">
    <datalist id="cargens">
      <option value="S450">
      <option value="S680">
    </datalist><br><br>
    
    <!-- Button -->
    <button type="button" onclick="alert('Nice try Diddy!')">Click Me!</button><br><br>
    
    <!-- Textarea -->
    <label for="message">Message:</label><br>
    <textarea name="message" id="message" rows="5" cols="30">I love this car.</textarea><br><br>
    
    <!-- Submit -->
    <input type="submit" value="Submit">
  </fieldset>
</form>
```

# Target
| Value       | Description                 |
| ----------- | --------------------------- |
| _blank      | A new window or tab         |
| _self       | The current window          |
| _parent     | The parent frame            |
| _top        | The full body of the window |
| _framename_ | A named iframe              |

# Method
- GET
- POST (Recommend)

# Forms Elements
- `<input>`
- `<label>`
- `<select>`
- `<textarea>`
- `<button>`
- `<fieldset>`
- `<legend>`
- `<datalist>`
- `<output>`
- `<option>`
- `<optgroup>`

# Inpute Type
- `<input type="button">`
- `<input type="checkbox">`
- `<input type="color">`
- `<input type="date">`
- `<input type="datetime-local">`
- `<input type="email">`
- `<input type="file">`
- `<input type="hidden">`
- `<input type="image">`
- `<input type="month">`
- `<input type="number">`
- `<input type="password">`
- `<input type="radio">`
- `<input type="range">`
- `<input type="reset">`
- `<input type="search">`
- `<input type="submit">`
- `<input type="tel">`
- `<input type="text">`
- `<input type="time">`
- `<input type="url">`
- `<input type="week">`

## Input Attributes
- `readonly`:
- `disable`:
- `size`: 
- `maxlength`: 
- `min` & `max`: 
- `multiple`: 
- `pattern`: 
- `placeholder`:
- `required`:
- `step`:
- `autofocus`:
- `height` & `width`:
- `autocomplete`:
- `list`:

# Output
```html
<form action="/action_page.php"  
  oninput="x.value=parseInt(a.value)+parseInt(b.value)">  
  0  
  <input type="range"  id="a" name="a" value="50">  
  100 +  
  <input type="number" id="b" name="b" value="50">  
  =  
  <output name="x" for="a b"></output>  
  <br><br>  
  <input type="submit">  
</form>
```

# Attributes
- `form`: Outside the form element, but still part of the form (Same `id`).
- `formaction`:  Overrides the action attribute.
- `formenctype`: Overrides the enctype attribute (Only with `method="post"`).
- `formmethod`: Overrides the method attribute.
- `formtarget`: Overrides the target attribute.
- `formnovalidate`: Overrides the novalidate attribute. Skip `required`