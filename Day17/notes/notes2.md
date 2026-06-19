# 📅 Day 17 - File 2

# All DOM Selectors, NodeList and HTMLCollection in JavaScript

## 🎥 Video

**All DOM Selectors, NodeList and HTMLCollection | Chai aur JavaScript**

---

# 📚 Introduction

After understanding what the DOM is, the next step is learning how to access elements from an HTML page.

JavaScript provides several DOM selector methods that allow developers to locate and manipulate elements efficiently.

These selectors are used daily in:

* React Applications
* E-Commerce Websites
* Dashboards
* Portfolio Websites
* Form Validation
* Interactive UI Components

In this session, I learned:

* `getElementById()`
* `getElementsByClassName()`
* `getElementsByTagName()`
* `querySelector()`
* `querySelectorAll()`
* NodeList
* HTMLCollection
* Differences between NodeList and HTMLCollection

---

# 🔹 Why DOM Selectors Matter

Consider this HTML:

```html
<h1 id="title">Hello World</h1>
```

JavaScript cannot modify this element until it first finds it.

DOM selectors help JavaScript locate elements inside the webpage.

---

# 🔹 getElementById()

The most commonly used DOM selector.

Used to select an element using its unique id.

---

## Syntax

```javascript
document.getElementById("idName")
```

---

## Example

HTML

```html
<h1 id="title">Hello World</h1>
```

JavaScript

```javascript
const heading = document.getElementById("title");
```

Returns:

```html
<h1 id="title">Hello World</h1>
```

---

# Storing in Variables

```javascript
const title = document.getElementById("title");
```

Now we can manipulate it.

---

# Changing Content

```javascript
title.innerHTML = "Welcome";
```

Output:

```html
<h1>Welcome</h1>
```

---

# Changing Style

```javascript
title.style.color = "red";
```

---

```javascript
title.style.backgroundColor = "black";
```

---

```javascript
title.style.padding = "10px";
```

---

```javascript
title.style.borderRadius = "10px";
```

---

# Useful Properties

---

## innerHTML

Returns complete HTML.

```javascript
console.log(title.innerHTML);
```

---

## innerText

Returns visible text only.

```javascript
console.log(title.innerText);
```

---

## textContent

Returns all text content.

```javascript
console.log(title.textContent);
```

---

# Difference

HTML:

```html
<h1 id="title">
    Hello
    <span style="display:none">World</span>
</h1>
```

---

### innerText

```text
Hello
```

---

### textContent

```text
Hello World
```

---

# 🔹 getElementsByClassName()

Used to select elements using class names.

---

## Syntax

```javascript
document.getElementsByClassName("className")
```

---

HTML

```html
<li class="item">One</li>
<li class="item">Two</li>
<li class="item">Three</li>
```

---

JavaScript

```javascript
const items = document.getElementsByClassName("item");
```

Returns:

```javascript
HTMLCollection(3)
```

---

# Accessing Elements

```javascript
items[0]
items[1]
items[2]
```

---

# Changing Element

```javascript
items[0].style.color = "red";
```

---

# 🔹 getElementsByTagName()

Selects elements based on tag name.

---

## Syntax

```javascript
document.getElementsByTagName("tag")
```

---

Example

```javascript
document.getElementsByTagName("li");
```

Returns:

```javascript
HTMLCollection
```

---

HTML

```html
<li>One</li>
<li>Two</li>
<li>Three</li>
```

---

Result:

```javascript
HTMLCollection(3)
```

---

# 🔹 querySelector()

One of the most powerful selectors.

Returns the first matching element.

---

## Syntax

```javascript
document.querySelector("selector")
```

---

# Select by ID

```javascript
document.querySelector("#title");
```

---

# Select by Class

```javascript
document.querySelector(".item");
```

---

# Select by Tag

```javascript
document.querySelector("h1");
```

---

# Example

```javascript
const title = document.querySelector("#title");

title.style.color = "blue";
```

---

# Selecting Nested Elements

HTML

```html
<ul>
    <li>One</li>
    <li>Two</li>
</ul>
```

---

JavaScript

```javascript
document.querySelector("ul li");
```

Returns:

```html
<li>One</li>
```

First matching element only.

---

# 🔹 querySelectorAll()

Returns all matching elements.

---

## Syntax

```javascript
document.querySelectorAll("selector")
```

---

Example

```javascript
document.querySelectorAll("li");
```

Returns:

```javascript
NodeList(3)
```

---

# Accessing Elements

```javascript
const items = document.querySelectorAll("li");

items[0]
items[1]
items[2]
```

---

# Styling Elements

```javascript
items[0].style.color = "green";
```

---

# Using forEach

One major advantage.

```javascript
items.forEach((item) => {

    item.style.color = "red";

});
```

All elements become red.

---

# 🔹 NodeList

A NodeList is a collection of DOM nodes.

Returned by:

```javascript
querySelectorAll()
```

---

Example

```javascript
const items = document.querySelectorAll("li");
```

Returns:

```javascript
NodeList
```

---

# Characteristics

```text
Array-like
Indexed
Has length property
Supports forEach()
```

---

Example

```javascript
items.forEach((item) => {

    console.log(item);

});
```

Works perfectly.

---

# 🔹 HTMLCollection

Returned by:

```javascript
getElementsByClassName()
getElementsByTagName()
```

---

Example

```javascript
const items = document.getElementsByClassName("item");
```

Returns:

```javascript
HTMLCollection
```

---

# Characteristics

```text
Array-like
Indexed
Has length property
Does NOT support forEach()
```

---

# Problem

```javascript
items.forEach((item)=>{

});
```

Error:

```text
forEach is not a function
```

---

# Converting HTMLCollection to Array

Use:

```javascript
Array.from()
```

---

Example

```javascript
const converted = Array.from(items);
```

Now:

```javascript
converted.forEach((item)=>{

});
```

Works successfully.

---

# NodeList vs HTMLCollection

| Feature                 | NodeList         | HTMLCollection                   |
| ----------------------- | ---------------- | -------------------------------- |
| Returned By             | querySelectorAll | getElementsByClassName / TagName |
| Array Like              | ✅                | ✅                                |
| forEach()               | ✅                | ❌                                |
| Indexed                 | ✅                | ✅                                |
| length Property         | ✅                | ✅                                |
| Convert to Array Needed | Usually No       | Often Yes                        |

---

# Most Commonly Used Selectors

Modern JavaScript developers mostly use:

```javascript
querySelector()
querySelectorAll()
```

Because:

```text
Flexible
Powerful
Supports CSS Selectors
Cleaner Code
```

---

# Real-World Examples

## Form Validation

```javascript
const email =
document.querySelector("#email");
```

---

## Navigation Menu

```javascript
const links =
document.querySelectorAll(".nav-link");
```

---

## To-Do Application

```javascript
const tasks =
document.querySelectorAll(".task");
```

---

## E-Commerce Website

```javascript
const products =
document.querySelectorAll(".product");
```

---

## Dashboard

```javascript
const cards =
document.querySelectorAll(".card");
```

---

# Common Interview Questions

### Difference Between querySelector and querySelectorAll?

`querySelector()`

Returns first matching element.

---

`querySelectorAll()`

Returns all matching elements.

---

### What is NodeList?

Collection of DOM nodes returned by `querySelectorAll()`.

---

### What is HTMLCollection?

Collection of HTML elements returned by class and tag selectors.

---

### Can HTMLCollection use forEach?

No.

Must convert into an array first.

---

### Why is querySelector popular?

Supports CSS selectors and provides cleaner syntax.

---

# 🔑 Key Learnings

* Learned how DOM selectors work.
* Understood getElementById().
* Explored getElementsByClassName().
* Explored getElementsByTagName().
* Learned querySelector().
* Learned querySelectorAll().
* Understood NodeList.
* Understood HTMLCollection.
* Compared NodeList and HTMLCollection.
* Learned Array.from() conversion.
* Explored real-world DOM selection scenarios.

---

# 📚 Summary

Today's session focused on DOM selectors, which are the foundation of DOM manipulation in JavaScript. I learned how to access elements using IDs, classes, tags, and CSS selectors. The introduction to querySelector and querySelectorAll showed why these methods are preferred in modern development due to their flexibility and cleaner syntax.

The most important takeaway was understanding the difference between NodeList and HTMLCollection. Knowing when a collection supports forEach and when it needs conversion to an array is a common interview topic and an essential practical skill. These concepts form the basis of almost all frontend development and prepare me for advanced DOM manipulation and event handling.

---

## ✅ Progress

**Day 17**
**Topic: All DOM Selectors, NodeList and HTMLCollection**
