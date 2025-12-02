```js
new Date()  
new Date(date string)  

new Date(year,month,day,hours,minutes,seconds,ms)  // Can remove the values ​​behind
  
new Date(milliseconds) // Since 01 January 1970
```

# Methods
```js
const d = new Date();  

d.toDateString();
d.toUTCString();
d.toISOString();
```

# Formats
 ```js
let msec = Date.parse("March 21, 2012");  // Convert it to milliseconds
 ```

# Get

| Method            | Description                          | UTC                  |
| ----------------- | ------------------------------------ | -------------------- |
| getFullYear()     | (yyyy)                               | getUTCFullYear()     |
| getMonth()        | (0-11)                               | getUTCMonth()        |
| getDate()         | (1-31)                               | getUTCDate()         |
| getDay()          | (0-6)                                | getUTCDay()          |
| getHours()        | (0-23)                               | getUTCHours()        |
| getMinutes()      | (0-59)                               | getUTCMinutes()      |
| getSeconds()      | (0-59)                               | getUTCSeconds()      |
| getMilliseconds() | (0-999)                              | getUTCMilliseconds() |
| getTime()         | (milliseconds since January 1, 1970) |                      |

```js
let ms = Date.now(); // Returns the number of milliseconds since January 1, 1970.

const d = new Date();
let diff = d.getTimezoneOffset(); // Returns the difference (in minutes) between local time an UTC time:
```

# Set

| Method            | Description                          |
| ----------------- | ------------------------------------ |
| setDate()         | (1-31)                               |
| setFullYear()     | (yyyy)                               |
| setHours()        | (0-23)                               |
| setMilliseconds() | (0-999)                              |
| setMinutes()      | (0-59)                               |
| setMonth()        | (0-11)                               |
| setSeconds()      | (0-59)                               |
| setTime()         | (milliseconds since January 1, 1970) |