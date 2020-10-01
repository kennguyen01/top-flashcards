---
title: Functions
---

1a. Function
1b. Reusable piece of code.

2a. Defining function
2b.
```
function random(parameter) {
  return value;
}
```

3a. Invoking function
3b.
```
function myFunc() {
  return value;
}

myFunc();
```

4a. Anonymous function
4b.
```
// Function without a name, often used for event handler
let myBtn = document.querySelector('button');

myBtn.onclick = function() {
  alert('hello');
}
```

5a. Function scope
5b. Variables and things declared inside the function are inside their own separate scope, unreachable outside the function.

6a. Global scope
6b. Top level scope outside all functions. Variables declared here are accessible everywhere in the code.

7a. Functions inside functions
7b.
```
// Complex function can be broken down into smaller functions
function bigFunc() {
  subFunc1();
  subFunc2();
  subFunc3();
}
```

8a. Return value
8b. What a function returns when it finishes.

9a. Default parameter
9b.
```
// Named parameter can be initialized with default value if no value is passed
function multiply(a, b = 1) {
  return a * b;
}

alert(multiply(5));   // 5
```

10a. ?? (nullish coalescing operator)
10b.
```
// An expression is defined when it's either null nor undefined
function showCount(count) {
  alert(count ?? 'unknown');
}

showCount(0);       // 0
showCount(null);    // 'unknown'
```

11a. Empty return
11a.
```
// If function does not return a value, it returns undefined
function doNothing() {
  return;
}

alert(doNothing() === undefined);   // true
```

12a. Function expression
12b.
```
// Function can be defined and assigned to a variable explicitly
let sayHi = function() {
  alert('Hello');
};
```

13a. Callback function
13b.
```
// Callback function is a function passed into another function as argument
function greeting(name) {
  alert('Hello ' + name);
}

function processUserInput(callback) {
  let name = prompt('Please enter your name.');
  callback(name);
}

processUserInput(greeting);
```

14a. Arrow function
14b.
```
// Shortcut to regular function expression
let sum = function(a, b) {
  return a + b;
}

// Arrow function version
let sum = (a, b) => a + b;
```