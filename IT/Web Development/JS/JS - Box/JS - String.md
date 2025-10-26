| Escape Characters | Result               | Description  |
| ----------------- | -------------------- | ------------ |
| `\'`              | '                    | Single quote |
| `\" `             | "                    | Double quote |
| `\\`              | `\`                  | Backslash    |
| \b                | Backspace            |              |
| \f                | Form Feed            |              |
| \n                | New Line             |              |
| \r                | Carriage Return      |              |
| \t                | Horizontal Tabulator |              |
| \v                | Vertical Tabulator   |              |

## Back-Tics Syntax
```js
let name = "Loc";
let age = 18;
let text = 
`Hello ${name}
Next year, you are ${age +1} year old.`;
```

```js
let header = "Cars";  
let tags = ["Maybach", "Rolls Royce", "Porsche"];  
  
let html = `<h2>${header}</h2> <ul>`;  
for (const x of tags) {  
  html += `<li>${x}</li>`;  
}  
  
html += `</ul>`;
document.getElementById("demo").innerHTML = html;
```

## Methods
```js
let text1 = "Hello"
let text2 = "World"

let length = text1.length // 5 

let char = text1.charAt(0); // H
let char = text1.charCodeAt(0); // 72
let code = text1.codePointAt(0); // 72
let letter = text1.at(0); // let letter = text[0] -> H

let text3 = text1.concat(" ", text2); // Hello World

let part1 = text1.slice(2,4); // ll
let part2 = text1.substring(2,4); // ll
let part3 = text1.substr(2,4); // ll

let text4 = text1.toUpperCase(); // HELLO
let text5 = text2.toLowerCase(); // world

let text6 = text1.trim(): // Remove whitespace bothside
let text7 = text1.trimStart();
let text8 = text1.trimEnd();

let padded1 = text1.padStart(8,"0"); // 000Hello
let padded2 = text1.padEnd(8, "0"); // Hello000

let result = text1.repeat(2); // HelloHello
let newText = text3.replace("World", "Hello"); // World Hello
let newText2 = text3.replaceAll("Hello", "World");

let array1 = text3.split(" ");  
```

## Search
```js
let text1 = "Please locate where 'locate' occurs!";
let index1 = text1.indexOf("locate"); // 7 
let index2 = text1.lastIndexOf("locate"); //21
let index3 = text1.lastIndexOf("Loc"); // -1
let index4 = text1.search("locate"); //7

let text2 = "The rain in SPAIN stays mainly in the plain";
let match1 = text2.match("ain"); // 1
let match2 = text2.match(/ain/); // 1
let match3 = text2.match(/ain/g); // 3
let match4 = text2.match(/ain/gi); // 4

let text3 = "I love cats. Cats are very easy to love. Cats are very popular."
let iterator = text3.matchAll(/Cats/gi); // cats,Cats,Cats

let text4 = "Hello world, welcome to the universe.";  
let check1 = text4.includes("world", 12); //false

let text5 = "Hello world, welcome to the universe.";  
let check2 = text5.startsWith("world", 6) //true
let check3 = text5.endsWith("world", 11); //true
``` 