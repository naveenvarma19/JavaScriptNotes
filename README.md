# JavaScript Learning Repository

Welcome to my JavaScript Learning Repository! This repository is designed to help me keep track of my learning progress and notes on various JavaScript topics from the Udemy course by Maximilian Schwarzmüller. 

---

# JavaScript Notes

## What is JavaScript?

JavaScript is a programming language used to make websites interactive and dynamic. It runs in your web browser, letting you add cool features like animations, interactive forms, and real-time updates to your web pages.

## Why Do We Need JavaScript?

JavaScript is super important for creating modern websites because:

- **Interactivity:** It helps you add interactive elements to a webpage, like buttons and pop-ups, so users can engage with your site.
- **Client-Side Processing:** It runs directly in the user's browser, which makes websites faster and more responsive without needing constant communication with the server.
- **Asynchronous Operations:** It lets you handle tasks like fetching data from servers without freezing up the webpage, making your site feel smoother.
- **DOM Manipulation:** It can change the content and layout of a page on the fly, which is key for making dynamic, single-page applications.

---

## Linking JavaScript with HTML

JavaScript can be connected to HTML in two ways: internal and external.

### Internal JavaScript

- Use the `<script></script>` tag to include JavaScript code directly within an HTML file.

Example:
```html
<script>
  // Your JavaScript code here
</script>
```

### External JavaScript

- To use an external JavaScript file, include it using the `<script src="filename.js"></script>` tag. The `filename.js` file can contain any JavaScript code and be linked to the HTML file.

Example:
```html
<script src="filename.js"></script>
```

- The `<script>` tag must always have both opening and closing tags when referencing an external JS file, even if no code is placed between them.

- You can link as many external JavaScript files as needed in your HTML file.
 ---

## JavaScript `<script>` Tag Placement and `defer` Attribute

## `<script>` Tag Placement

- **Recommended Practice**: Place the `<script>` tag in the `<body>` tag.
  - **Performance**: Helps improve page load times because the browser can render the HTML content before loading and executing the script.
  - **Element Access**: Ensures that your script can access and manipulate HTML elements that are already present on the page.

## `defer` Attribute

- **Usage**: Add the `defer` attribute to the `<script>` tag.
  - **Execution Timing**: Scripts with the `defer` attribute are executed after the page has finished parsing.
  - **Order of Execution**: Scripts are executed in the order they appear in the document, but only after the HTML is fully parsed.

```html
<!-- Example -->
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <h1>Hello World</h1>
    <!-- Place script here -->
    <script src="script.js" defer></script>
</body>
</html>
```

---

##  `<noscript>` Tag

The `<noscript>` HTML tag is used to define content that should be displayed to users who have JavaScript disabled in their browsers. 

### Syntax
```html
<noscript>
  <!-- Content to display if JavaScript is turned off -->
</noscript>
```

### Example
```html
<noscript>
  <p>It looks like JavaScript is disabled in your browser. Please enable JavaScript to enjoy the full functionality of this website.</p>
</noscript>
```
---

# JavaScript Variables


In JavaScript, variables are used to store values that can be used and manipulated throughout your code.

## Creating Variables

In JavaScript, you can create variables using the `var`, `let`, or `const` keywords. Historically, the `var` keyword was used, but it's generally recommended to use `let` or `const` for modern JavaScript code.

### Syntax

```javascript
var variableName = value;
```

- **`var`**: Declares a variable that can be re-assigned and has function scope.
- **`let`**: Declares a variable that can be re-assigned and has block scope.
- **`const`**: Declares a variable that cannot be re-assigned and has block scope.

### Example

```javascript
var message = "Hello, world!";
console.log(message); // Outputs: Hello, world!
```
---

## Data Types

Variables in JavaScript can hold different types of values:

- **Text (String)**: `"Hello"`
- **Number**: `42`
- **Boolean**: `true` or `false`
- **Null**: Represents an empty value or a value that is not set yet.
- **NaN**: Stands for "Not-a-Number", but its type is actually a number.
- **Array**: A list of values, e.g., `[1, 2, 3]`
- **Object**: A collection of key-value pairs, e.g., `{ name: "Alice", age: 30 }`
- **Function**: A block of code that can be executed, e.g., `function greet() { return "Hello"; }`

### Example

```javascript
var text = "JavaScript";
var number = 100;
var isActive = true;
var emptyValue = null;
var notANumber = NaN;
var array = [1, 2, 3, 4];
var object = { name: "John", age: 25 };
var greet = function() { return "Hello!"; };
```

## Variable Naming Rules

- Variable names must begin with a letter, underscore (`_`), or dollar sign (`$`).
- Variable names cannot begin with a number, though they can contain numbers after the first character.
- Variable names are case-sensitive.

### Example

```javascript
var validName1 = "valid";
var validName2 = "_valid";
var validName3 = "$valid";
var validName4 = "valid1";

var 1invalidName = "invalid"; // This will cause an error
```

## Checking Variable Types

You can check the type of a variable using `typeof`.

### Syntax

```javascript
console.log(typeof variableName);
```

### Example

```javascript
var number = 10;
console.log(typeof number); // Outputs: "number"

var text = "Hello";
console.log(typeof text); // Outputs: "string"
```

---
## Strict Mode

# JavaScript Strict Mode

## Purpose
Enforces cleaner, safer code by catching common mistakes.

## How to Enable
Add `"use strict";` at the beginning of your script or function.

```javascript
"use strict";
// Your code here
```
Certainly! Here’s a corrected version of your notes formatted in Markdown for a README:

---
## Dynamic Typing

JavaScript is a dynamically typed language. This means that variables in JavaScript can hold values of any type, and their types can change during runtime. Because of this, you don't need to specify a type when declaring a variable.

```javascript
let example = 42;   // Initially a number
example = "Hello";  // Now it's a string
```
---
## Hoisting

Hoisting in JavaScript is a behavior where variable and function declarations are moved to the top of their containing scope during the compilation phase. This means that you can use variables and functions before they are declared in the code. 

Here's a simplified way to think about it:

1. **First Pass**: JavaScript scans the code and identifies all the declarations (e.g., `var`, `function`).
2. **Second Pass**: JavaScript executes the code, using the declarations that were identified in the first pass.

For example:

```javascript
console.log(x);  // undefined, not an error
var x = 5;
console.log(x);  // 5
```

In this case, `var x` is hoisted to the top, but the assignment `x = 5` is not.
---

## JavaScript Functions
## Declaring Functions

To declare a function in JavaScript, use the following syntax:

```javascript
function funName() {
    console.log('Inside Function');
}
```

However, just declaring a function does not execute it. To see the output, you need to **call** the function:

```javascript
funName();  // This will print 'Inside Function' to the console
```

## Functions with Arguments and Return Statement

Functions can accept arguments and return values. The `return` statement will send the output back to the place where the function was called.

### Example: Adding Two Numbers

Here's how you can declare a function that takes parameters and returns a value:

```javascript
function addition(num1, num2) {
    return num1 + num2;
}
```

To use the function, call it with arguments and store the result in a variable:

```javascript
var sum = addition(10, 10);
console.log(sum);  // This will print '20' to the console
```
