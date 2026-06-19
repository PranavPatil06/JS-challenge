# 📅 Day 17

# DOM Introduction in JavaScript

## 🎥 Video

**DOM Introduction in JavaScript | Chai aur JavaScript**

---

# 📚 Introduction

Until now, most JavaScript programs we wrote were running in the console. However, real websites are interactive because JavaScript can manipulate HTML and CSS directly.

This interaction is possible through something called the **DOM (Document Object Model)**.

The DOM acts as a bridge between JavaScript and HTML, allowing developers to:

* Change text dynamically
* Update styles
* Add or remove elements
* Respond to user actions
* Build interactive web applications

Understanding the DOM is one of the most important milestones in JavaScript because it marks the transition from core JavaScript concepts to frontend development.

---

# 🔹 What is DOM?

DOM stands for:

```text
Document Object Model
```

It is a programming interface created by the browser for HTML documents.

The browser converts an HTML page into a tree-like structure that JavaScript can access and manipulate.

---

# HTML Document Example

```html
<!DOCTYPE html>
<html>
<head>
    <title>DOM</title>
</head>
<body>

    <h1>Hello World</h1>
    <p>Learning DOM</p>

</body>
</html>
```

---

# DOM Representation

```text
Document
│
└── HTML
    │
    ├── HEAD
    │   └── TITLE
    │
    └── BODY
        │
        ├── H1
        └── P
```

This structure is called:

```text
DOM Tree
```

---

# Why DOM Exists?

Without DOM:

```text
JavaScript cannot interact with HTML
```

With DOM:

```text
JavaScript can read
JavaScript can modify
JavaScript can create elements
JavaScript can delete elements
```

---

# Browser Creates DOM Automatically

When a webpage loads:

### Step 1

Browser downloads HTML.

↓

### Step 2

Browser parses HTML.

↓

### Step 3

Browser creates DOM Tree.

↓

### Step 4

JavaScript gets access to DOM.

---

# 🔹 Document Object

The entire webpage is represented by:

```javascript
document
```

Example:

```javascript
console.log(document);
```

Output:

```text
Complete HTML document
```

---

# Inspecting the DOM

Open Browser Developer Tools:

```text
Right Click
↓
Inspect
```

or

```text
F12
```

The Elements tab displays the DOM Tree.

---

# Useful Document Properties

---

## document.title

Returns webpage title.

```javascript
console.log(document.title);
```

Output:

```text
DOM Learning
```

---

## document.URL

Returns current page URL.

```javascript
console.log(document.URL);
```

---

## document.domain

Returns website domain.

```javascript
console.log(document.domain);
```

---

## document.links

Returns all links.

```javascript
console.log(document.links);
```

---

## document.images

Returns all images.

```javascript
console.log(document.images);
```

---

# 🔹 Accessing Elements

The DOM allows JavaScript to access HTML elements.

Example:

```html
<h1 id="title">Hello</h1>
```

JavaScript:

```javascript
document.getElementById("title");
```

Returns:

```text
<h1>Hello</h1>
```

---

# DOM as Objects

Every HTML element becomes a JavaScript object.

Example:

```html
<h1 id="title">Hello</h1>
```

JavaScript sees:

```javascript
{
    id: "title",
    innerHTML: "Hello"
}
```

This allows JavaScript to manipulate it.

---

# 🔹 Modifying Content

HTML:

```html
<h1 id="title">Hello</h1>
```

JavaScript:

```javascript
document.getElementById("title").innerHTML = "Welcome";
```

Output:

```html
<h1>Welcome</h1>
```

---

# 🔹 Modifying Styles

```javascript
document.getElementById("title").style.color = "red";
```

Changes text color.

---

# 🔹 DOM and Events

The DOM works closely with events.

Examples:

* Click
* Hover
* Submit
* Keypress

Example:

```javascript
button.addEventListener("click", function(){

});
```

User interaction becomes possible because of the DOM.

---

# DOM Relationships

Every node can have:

```text
Parent
Child
Sibling
```

Example:

```html
<body>

    <h1>Hello</h1>

    <p>Paragraph</p>

</body>
```

---

Relationship:

```text
BODY
│
├── H1
└── P
```

Body = Parent

H1 and P = Children

H1 and P = Siblings

---

# Types of Nodes

DOM consists of nodes.

---

## Element Nodes

```html
<h1>
<p>
<div>
```

---

## Text Nodes

```html
Hello World
```

---

## Attribute Nodes

```html
id
class
href
```

---

# Window Object vs Document Object

Common Interview Question.

---

## Window

Represents browser.

```javascript
window
```

Contains:

```text
alert()
setTimeout()
location
history
```

---

## Document

Represents webpage.

```javascript
document
```

Contains:

```text
HTML Elements
DOM Methods
DOM Properties
```

---

# DOM Manipulation Powers

Using DOM, JavaScript can:

### Change Text

```javascript
element.innerText
```

### Change HTML

```javascript
element.innerHTML
```

### Change CSS

```javascript
element.style
```

### Add Elements

```javascript
createElement()
```

### Remove Elements

```javascript
remove()
```

---

# Real-World Applications

## Social Media

Update likes instantly.

---

## E-Commerce

Update cart count dynamically.

---

## Dashboards

Display real-time analytics.

---

## Chat Applications

Show incoming messages instantly.

---

## Forms

Validate user input.

---

# Common Interview Questions

### What is DOM?

The browser's representation of an HTML document as a tree structure.

---

### Why is DOM important?

Allows JavaScript to interact with HTML and CSS.

---

### What is document?

The root object representing the webpage.

---

### Difference Between Window and Document?

Window = Browser

Document = Webpage

---

### What is a DOM Tree?

Hierarchical representation of HTML elements.

---

# 🔑 Key Learnings

* Learned what DOM stands for.
* Understood DOM Tree structure.
* Learned how browsers create DOM.
* Explored the document object.
* Learned useful document properties.
* Understood DOM nodes.
* Explored parent-child relationships.
* Learned content manipulation.
* Learned style manipulation.
* Understood DOM's role in interactive websites.

---

# 📚 Summary

Today's session introduced the Document Object Model (DOM), which acts as the connection between JavaScript and HTML. I learned how browsers convert HTML into a tree structure that JavaScript can access and manipulate. Understanding the document object helped me see how JavaScript interacts with webpage elements behind the scenes.

The most exciting part was realizing that JavaScript can dynamically change content, styles, and even create or remove elements. This topic marks the beginning of frontend development because the DOM is the foundation for building interactive websites and web applications.

---

## ✅ Progress

**Day 17**
**Topic: DOM Introduction in JavaScript**
