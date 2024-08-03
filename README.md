# JavaScript Learning Repository

Welcome to my JavaScript Learning Repository! This repository is designed to help me keep track of my learning progress and notes on various JavaScript topics from the Udemy course by Maximilian Schwarzmüller. 


# JavaScript Notes

## What is JavaScript?

JavaScript is a programming language used to make websites interactive and dynamic. It runs in your web browser, letting you add cool features like animations, interactive forms, and real-time updates to your web pages.

## Why Do We Need JavaScript?

JavaScript is super important for creating modern websites because:

- **Interactivity:** It helps you add interactive elements to a webpage, like buttons and pop-ups, so users can engage with your site.
- **Client-Side Processing:** It runs directly in the user's browser, which makes websites faster and more responsive without needing constant communication with the server.
- **Asynchronous Operations:** It lets you handle tasks like fetching data from servers without freezing up the webpage, making your site feel smoother.
- **DOM Manipulation:** It can change the content and layout of a page on the fly, which is key for making dynamic, single-page applications.

## Key Point

JavaScript typically runs in the browser, enabling dynamic interactions by manipulating the Document Object Model (DOM) and handling events in real-time. This execution environment is managed by the browser's JavaScript engine, which varies by browser (e.g., V8 in Chrome, SpiderMonkey in Firefox). JavaScript's ability to perform asynchronous operations with callbacks, promises, and async/await allows for non-blocking, interactive web experiences.


```markdown

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
```

# JavaScript `<script>` Tag Placement and `defer` Attribute

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

### Key Points
- The content inside `<noscript>` is shown only when JavaScript is disabled.
- It helps provide a better user experience for users who may have JavaScript turned off.

---
