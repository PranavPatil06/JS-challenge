# 📅 Day 16

# Filter, Map & Reduce in JavaScript

## 🎥 Video

**Filter Map and Reduce in JavaScript | Chai aur JavaScript**

---

# 📚 Introduction

Modern JavaScript provides powerful array methods that allow developers to process data efficiently without writing complex loops.

Among the most important and frequently used methods are:

* `filter()`
* `map()`
* `reduce()`

These methods are heavily used in:

* React Applications
* Node.js Projects
* API Data Processing
* Dashboards
* E-Commerce Platforms
* Data Analytics

Understanding these methods is essential because they form the foundation of functional programming in JavaScript.

---

# 🔹 Why Use Filter, Map, and Reduce?

Traditionally, we use loops:

```javascript
const numbers = [1, 2, 3, 4, 5];

const result = [];

for(let i = 0; i < numbers.length; i++){

    if(numbers[i] > 3){

        result.push(numbers[i]);

    }

}
```

Modern JavaScript provides cleaner alternatives:

```javascript
const result = numbers.filter(num => num > 3);
```

More readable and easier to maintain.

---

# 🔹 filter()

The `filter()` method creates a new array containing only elements that satisfy a condition.

---

## Syntax

```javascript
array.filter(callback)
```

---

## Basic Example

```javascript
const numbers = [1,2,3,4,5,6];

const result = numbers.filter((num) => {
    return num > 4;
});

console.log(result);
```

Output:

```javascript
[5,6]
```

---

# How filter Works

For each element:

```text
Condition True  → Keep Element
Condition False → Ignore Element
```

---

## Example

```javascript
const nums = [10,20,30,40,50];

const result = nums.filter((num) => num >= 30);
```

Output:

```javascript
[30,40,50]
```

---

# filter vs forEach

### Using forEach

```javascript
const newNums = [];

nums.forEach((num) => {

    if(num > 20){

        newNums.push(num);

    }

});
```

---

### Using filter

```javascript
const newNums = nums.filter((num) => num > 20);
```

Cleaner and shorter.

---

# Array of Objects Example

Very common in APIs.

```javascript
const books = [

    {
        title: "Book One",
        genre: "History",
        publish: 1981
    },

    {
        title: "Book Two",
        genre: "Science",
        publish: 2000
    }

];
```

---

## Filter by Genre

```javascript
const historyBooks = books.filter((book) => {

    return book.genre === "History";

});
```

Output:

```javascript
[
    {
        title:"Book One",
        genre:"History"
    }
]
```

---

## Filter by Year

```javascript
const modernBooks = books.filter((book) => {

    return book.publish >= 2000;

});
```

Useful when working with API datasets.

---

# Real-World Uses of filter()

### E-Commerce

```javascript
products.filter(product => product.price < 1000);
```

Show affordable products.

---

### Social Media

```javascript
posts.filter(post => post.likes > 100);
```

Popular posts.

---

### Job Portals

```javascript
jobs.filter(job => job.remote === true);
```

Remote jobs only.

---

# 🔹 map()

The `map()` method transforms each element of an array and returns a new array.

---

## Syntax

```javascript
array.map(callback)
```

---

## Basic Example

```javascript
const numbers = [1,2,3,4,5];

const result = numbers.map((num) => {

    return num * 10;

});
```

Output:

```javascript
[10,20,30,40,50]
```

---

# How map Works

```text
Input Array
↓
Transformation
↓
New Array
```

Original array remains unchanged.

---

## Example

```javascript
const users = ["Pranav","Rahul","Amit"];

const usernames = users.map((user) => {

    return user.toUpperCase();

});
```

Output:

```javascript
["PRANAV","RAHUL","AMIT"]
```

---

# Chaining Methods

One of the most powerful JavaScript features.

```javascript
const nums = [1,2,3,4,5];

const result = nums
    .map((num) => num * 10)
    .map((num) => num + 1);
```

Output:

```javascript
[11,21,31,41,51]
```

---

# Combining map and filter

```javascript
const nums = [1,2,3,4,5,6,7,8];

const result = nums
    .map((num) => num * 10)
    .filter((num) => num > 40);
```

Output:

```javascript
[50,60,70,80]
```

---

# Real-World Uses of map()

### E-Commerce

```javascript
products.map(product => product.name);
```

Get product names.

---

### API Data

```javascript
users.map(user => user.email);
```

Extract emails.

---

### Dashboards

```javascript
sales.map(item => item.amount);
```

Extract sales amounts.

---

# 🔹 reduce()

The most powerful array method.

Used to reduce multiple values into a single value.

Examples:

* Total cart price
* Sum of marks
* Average score
* Product statistics
* Analytics calculations

---

# Syntax

```javascript
array.reduce(callback, initialValue)
```

---

# Understanding Parameters

```javascript
array.reduce((accumulator, currentValue) => {

}, initialValue)
```

---

### accumulator

Stores running result.

### currentValue

Current array element.

---

# Basic Example

```javascript
const numbers = [1,2,3];

const total = numbers.reduce((acc, curr) => {

    return acc + curr;

}, 0);
```

Output:

```javascript
6
```

---

# Step-by-Step Execution

Array:

```javascript
[1,2,3]
```

Initial:

```javascript
acc = 0
```

---

Iteration 1:

```javascript
0 + 1 = 1
```

---

Iteration 2:

```javascript
1 + 2 = 3
```

---

Iteration 3:

```javascript
3 + 3 = 6
```

Final Result:

```javascript
6
```

---

# Shopping Cart Example

```javascript
const cart = [

    {
        item: "JS Course",
        price: 999
    },

    {
        item: "React Course",
        price: 1999
    }

];
```

---

## Total Price

```javascript
const totalPrice = cart.reduce((acc, item) => {

    return acc + item.price;

}, 0);
```

Output:

```javascript
2998
```

---

# Why reduce is Powerful

Can perform:

* Sum
* Average
* Count
* Grouping
* Object creation
* Statistics

All using a single method.

---

# Comparison

## filter()

Returns:

```javascript
Array
```

Purpose:

```text
Select Elements
```

---

## map()

Returns:

```javascript
Array
```

Purpose:

```text
Transform Elements
```

---

## reduce()

Returns:

```javascript
Single Value
```

Purpose:

```text
Combine Elements
```

---

# Quick Visual Difference

### Filter

```javascript
[1,2,3,4]
```

↓

```javascript
[3,4]
```

---

### Map

```javascript
[1,2,3]
```

↓

```javascript
[10,20,30]
```

---

### Reduce

```javascript
[1,2,3]
```

↓

```javascript
6
```

---

# Real-World Applications

## E-Commerce

```javascript
cart.reduce(...)
```

Calculate total bill.

---

## Social Media

```javascript
posts.filter(...)
```

Popular posts.

---

## User Management

```javascript
users.map(...)
```

Extract usernames.

---

## Analytics

```javascript
sales.reduce(...)
```

Calculate total revenue.

---

## Dashboards

```javascript
data
.filter(...)
.map(...)
.reduce(...)
```

Process large datasets efficiently.

---

# Common Interview Questions

### Difference Between filter and map?

`filter()` selects elements.

`map()` transforms elements.

---

### Does filter modify original array?

No.

Returns a new array.

---

### Does map modify original array?

No.

Returns a new transformed array.

---

### What does reduce return?

Usually a single value.

---

### Which is most powerful?

`reduce()`

Because it can perform many operations.

---

# 🔑 Key Learnings

* Learned the purpose of filter().
* Understood how filter selects data.
* Explored filtering arrays of objects.
* Learned the purpose of map().
* Understood data transformation.
* Learned method chaining.
* Combined map and filter together.
* Explored reduce().
* Understood accumulator and current value.
* Calculated totals using reduce().
* Connected these methods to real-world applications.

---

# 📚 Summary

Today's session introduced three of the most important array methods in JavaScript: filter, map, and reduce. I learned how filter helps select specific data from arrays, how map transforms data into a new format, and how reduce combines multiple values into a single result. These methods provide cleaner and more readable alternatives to traditional loops.

The most valuable takeaway was understanding how these methods work together. In real-world applications, developers often chain filter, map, and reduce to process API responses, calculate statistics, generate reports, and build dynamic user interfaces. Mastering these methods feels like a major step toward writing modern, professional JavaScript code.

---

## ✅ Progress

**Day 16**
**Topic: Filter, Map & Reduce in JavaScript**
