# 📅 Day 16 

# High Order Array Loops in JavaScript

## 🎥 Video

**High Order Array Loops | Chai aur JavaScript**

---

# 📚 Introduction

As applications grow larger, manually looping through arrays using traditional `for` loops becomes less efficient and harder to read. JavaScript provides powerful built-in array methods known as **Higher Order Array Loops** that make working with collections easier and cleaner.

These methods are widely used in modern JavaScript, React, Node.js, and real-world applications.

In this session, I learned:

* What Higher Order Functions are
* `forEach()`
* `for...of`
* `for...in`
* Iterating Arrays
* Iterating Objects
* Iterating Maps
* Differences between looping methods

---

# 🔹 What is a Higher Order Function?

A Higher Order Function is a function that:

* Accepts another function as an argument
* Returns a function

Example:

```javascript
function greet(callback){
    callback();
}
```

Array methods like:

```javascript
forEach()
map()
filter()
reduce()
```

are Higher Order Functions.

---

# 🔹 forEach Loop

One of the most commonly used array methods.

### Syntax

```javascript
array.forEach(function(item){

})
```

---

### Example

```javascript
const coding = ["js", "java", "python"];

coding.forEach(function(item){
    console.log(item);
});
```

Output:

```text
js
java
python
```

---

# 🔹 Arrow Function with forEach

```javascript
coding.forEach((item) => {
    console.log(item);
});
```

This is the most common modern syntax.

---

# 🔹 Parameters in forEach

```javascript
coding.forEach((item, index, array) => {

});
```

---

### item

Current element.

### index

Current position.

### array

Entire array.

---

### Example

```javascript
coding.forEach((item, index) => {
    console.log(index, item);
});
```

Output:

```text
0 js
1 java
2 python
```

---

# 🔹 Passing Function Reference

```javascript
function printMe(item){
    console.log(item);
}

coding.forEach(printMe);
```

Output:

```text
js
java
python
```

---

# 🔹 Array of Objects

Very common in APIs.

```javascript
const users = [
    {
        name: "Pranav",
        age: 20
    },
    {
        name: "Rahul",
        age: 21
    }
];
```

---

### Iterating Objects

```javascript
users.forEach((user) => {
    console.log(user.name);
});
```

Output:

```text
Pranav
Rahul
```

---

# 🔹 forEach Limitations

Important Interview Question.

`forEach()`:

```text
Does not return values
Cannot use break
Cannot use continue
```

Example:

```javascript
const values = coding.forEach((item)=>{
    return item;
});

console.log(values);
```

Output:

```javascript
undefined
```

---

# 🔹 for...of Loop

Used for iterable objects.

Works with:

* Arrays
* Strings
* Maps

---

### Syntax

```javascript
for(const value of object){

}
```

---

### Array Example

```javascript
const arr = [1,2,3,4];

for(const num of arr){
    console.log(num);
}
```

Output:

```text
1
2
3
4
```

---

# 🔹 String Example

```javascript
const greetings = "Hello";

for(const char of greetings){
    console.log(char);
}
```

Output:

```text
H
e
l
l
o
```

---

# 🔹 Maps in JavaScript

A Map stores key-value pairs.

Unlike objects:

```text
Keys remain unique
Insertion order maintained
```

---

### Creating Map

```javascript
const map = new Map();

map.set("IN", "India");
map.set("USA", "United States");
map.set("FR", "France");
```

---

### Iterating Map

```javascript
for(const [key, value] of map){

    console.log(key, value);

}
```

Output:

```text
IN India
USA United States
FR France
```

---

# 🔹 for...in Loop

Used to iterate through object properties.

---

### Example

```javascript
const user = {
    name: "Pranav",
    age: 20,
    city: "Pune"
};
```

---

```javascript
for(const key in user){

    console.log(key);

}
```

Output:

```text
name
age
city
```

---

### Access Values

```javascript
for(const key in user){

    console.log(user[key]);

}
```

Output:

```text
Pranav
20
Pune
```

---

# 🔹 for...in with Arrays

```javascript
const coding = ["js","java","python"];

for(const key in coding){

    console.log(key);

}
```

Output:

```text
0
1
2
```

Returns indexes, not values.

---

# 🔹 for...of vs for...in

| Feature | for...of | for...in |
| ------- | -------- | -------- |
| Arrays  | Values   | Indexes  |
| Objects | ❌        | ✅        |
| Maps    | ✅        | ❌        |
| Strings | ✅        | ❌        |

---

# 🌍 Real-World Applications

## Social Media

```javascript
posts.forEach(post => {
    displayPost(post);
});
```

---

## E-Commerce

```javascript
products.forEach(product => {
    renderProduct(product);
});
```

---

## Dashboard

```javascript
for(const key in stats){
    console.log(stats[key]);
}
```

---

## API Responses

```javascript
users.forEach(user => {
    console.log(user.name);
});
```

---

# 🔑 Key Learnings

* Learned Higher Order Functions.
* Understood forEach().
* Explored callback functions.
* Learned forEach parameters.
* Iterated arrays of objects.
* Understood forEach limitations.
* Learned for...of loop.
* Explored Maps.
* Learned for...in loop.
* Compared for...of and for...in.
* Connected array loops to real-world applications.

---

# 📚 Summary

Today's session introduced Higher Order Array Loops, which provide cleaner and more readable ways to work with arrays and collections. I learned how forEach simplifies iteration, how for...of works with iterable objects like arrays and strings, and how for...in is used for object properties.

Understanding these looping techniques helped me move beyond traditional for loops and closer to modern JavaScript practices used in React, Node.js, and real-world applications.
