# Java Script Web

# DOM Document object model

- The format of document where our js understands html code.
- When the html code is loaded on the web browser DOC will be created on the browser.
- All tags are represented as objects in the DOC. With their hierarchy.
- Doc understands each elements as nodes.
- There are basically 3 nodes

      -Element  Main tags like head body div etc

      -Attribute Attributes inside Main tag like class id style

      -Txt A property 

# JS

- Java Script adds programing to our page , and also functionality.
- There are three ways to JS in html
1. Embed 
2. External 
3. Inline like on click on hover etc

```jsx
<script>
   document.write("Hello world");
</script>
```

- The document is an object which represents the entire document.
- write is a function / method used to print the message in side the bracket on the browser.
- write Can also print html tags.
- External js can be included in the ff way in our html

```jsx
<script src="example.js"> 
</script>
```

- alert is used to show pop up on top of the browser.

# Comments

 - two types comments single line //
  - and multiple line comments /* */

---

# Variables

can be assigned in three ways

 - var basic declaration of a variable 

 -let Just like in algebra, variables are used in expressions:

-`const` constant values and cannot be changed.

Js is dynamically and loosely assigned for data types meaning we dont have to specify the data types for them.

# Objects

Ex

```jsx
const person = {
  firstName: "John",
  lastName: "Doe",
  age: 50,
  eyeColor: "blue"
};
```

# Arrays

used to store multiple values in a single variable . 

EX

```jsx
var names=["benji","able","mike"];
```

doesn’t need a loop to print them all. 

# Operators

- Arithmetic Operators
- Assignment Operators
- Comparison Operators
- Logical Operators
- Conditional Operators
- Type Operators

# Control flow Statement

if/else 

 switch 

# loops

for loop 

```jsx
- for (let i = 0; i < cars.length; i++) {

text += cars[i] + "<br>";

}
```

for in // is used for objects 

```jsx
for (let x in person) {
  text += person[x];
}
```

for in // is used for normal data types and arrays

# Functions

A JavaScript function is a block of code designed to perform a particular task.

A JavaScript function is executed when "something" invokes it (calls it).

```jsx
let x = myFunction(4, 3);   // Function is called, return value will end up in x

function myFunction(a, b) {
  return a * b;             // Function returns the product of a and b
}
```

# Event

A JavaScript can be executed when an event occurs, like when a user clicks on an HTML element.

To execute code when a user clicks on an element, add JavaScript code to an HTML event attribute:

```jsx
onclick=JavaScript
```

Examples of HTML events:

- When a user clicks the mouse
- When a web page has loaded
- When an image has been loaded
- When the mouse moves over an element
- When an input field is changed
- When an HTML form is submitted
- When a user strokes a key

# Jquery

- A fast small feature-reach java script frame work or library.
- It simplifies task by minimizing number of code of java script and working more.
- It simplifies AJAX calls and DOM manipulation.
- Features include

`**HTML/DOM manipulation**`

`**CSS manipulation**`

`**HTML event methods**`

`**Effective animation**`  

`**AJAX**`

`**Utilities**` 

- $ used for calling the lib.

# JSON

JSON stands for JavaScript Object Notation. The JSON syntax is derived from JavaScript object notation syntax, but the JSON format is text or string only. JSON is a light weight data format for storing and transporting. JSON is mostly used when data is sent from a server to a client. JSON is an easier-to-use alternative to XML.

JSON could help as in many scenarios for example we could have an web application now here when we send a request to the server we just need the data because we already have the styles and html.

There for we could send it in a plain text but then when we fetch it from the client side we need to write a lot of programing the best thing to do is to send it in an object format b/c we have a JavaScript object and this format is what is known as JSON.

So basically JSON is a format of data used when sent from server to a client.

Example

```jsx
{
"users":[
  {
    "firstName":"Asabeneh",
    "lastName":"Yetayeh",
    "age":250,
    "email":"asab@asb.com"
  },
  {
    "firstName":"Alex",
    "lastName":"James",
    "age":25,
    "email":"alex@alex.com"
  },
  {
  "firstName":"Lidiya",
  "lastName":"Tekle",
  "age":28,
  "email":"lidiya@lidiya.com"
  }
]
}
```

# Converting JSON to JavaScript Object

Mostly we fetch JSON data from HTTP response or from a file, but we can store the JSON as a string and we can change to Object for sake of demonstration. In JavaScript the keyword *JSON* has *parse()* and *stringify()* methods. When we want to change the JSON to an object we parse the JSON using *JSON.parse()*. When we want to change the object to JSON we use *JSON.stringify()*.

```jsx
JSON.parse(json[, reviver])
```

# Converting Object to JSON

When we want to change the object to JSON we use *JSON.stringify()*. The stringify method takes one required parameter and two optional parameters. The replacer is used as filter and the space is an indentations. If we do not want to filter out any of the keys from the object we can just pass undefined.

```jsx
JSON.stringify(obj, replacer, space)
```

# Local storage, Session and Cookies

This are the basic ways of storing data inside our browser.

- All three are stored in the browser so if they  stored in chrome we cant find them in mozilla or any other browser.
- Local storage and session storage are very similar in many ways. They are only different in few instances.
- Cookies are almost completely different from the two and are older.

![session.PNG](/session.PNG)

To store JSON in local storage or session storage first you create an object in your JavaScript code.

Then convert this object to JSON format using  and Store it in a variable.

```jsx
var Sterlizer = JSON.stringify(Personal);

var x = JSON.stringify(Personal);
```

Store this variable in a local or session storage like

```jsx
localStorage.setItem("myobj",Sterlizer);

sessionStorage.setItem("obj", x);
```

To see it in an Object format convert it again like this  

```jsx
var deSterlizer = JSON.parse(localStorage.getItem("myobj"));

var y = JSON.parse(sessionStorage.getItem("obj"));
```
