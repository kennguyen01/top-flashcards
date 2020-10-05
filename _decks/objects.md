---
title: Objects
---

1a. Object
1b. Keyed collection of various data types.

2a. Declaring object
2b.
```js
// Object literal syntax
let user = {
  name: 'John',           // Property with key-value pair
  'Likes birds': true,    // Multiword property is quoted
  age: 30,                // Trailing comma with last property
};
```

3a. Accessing object
3b.
```js
// Get property values of object
alert(user.name);   // 'John'
alert(user.age);    // 30
```

4a. Modifying object
4b.
```js
// Remove property
delete user.age;

// Setting new members, can be functions
user.farewell = function() {
  alert('Bye');
}
```

5a. Bracket notation
5b.
```js
// Square brackets provide a way to obtain property name from expression
let key = prompt('What do you want to know about the user?', 'name');

// Access by variable
alert(user[key]);   // 'John' (if enter 'name')
```

6a. Computed properties
6b.
```js
// Square brackets can be used to create object (computed properties)
let fruit = prompt('Which fruit to buy?', 'apple');

let bag = {
  [fruit]: 5,   // Property name taken from variable fruit
};
```

7a. Property value shorthand
7b.
```js
// When properties have the same names as variables, shorthand can be used
function makeUser(name, age) {
  return {
    name,     // same as name: name
    age,      // same as age: age
  };
}
```

8a. in (property existence)
8b.
```js
// Nonexisting property returns undefined
alert('age' in user);       // true, user.age exists
alert('blabla' in user);    // false, return undefined
```

9a. Looping over object
9b.
```js
// Loop over object keys with 'for...in'
for (let key in user) {
  alert(key);         // name, age
  alert(user[key]);   // John, 30
}
```

10a. Order of object
10b.
```js
// Int properties are sorted, others appear in creation order
// Int property means a string can be converted to int without change

let codes = {
  "49": "Germany",
  "41": "Switzerland",
  "44": "Great Britain",
  "1": "USA"
};

for (let code in codes) {
  alert(code); // 1, 41, 44, 49
}
```

11a. this
11b.
```js
/* 'this' keyword refers to the current object the code is being written inside.

It ensures that the correct values are used when a member's context changed. */
const person1 = {
  name: 'Chris',
  greeting: function() {
    alert("Hi! I'm " + this.name + '.');
  },
}

const person2 {
  name: 'Deepti',
  greeting: function() {
    alert("Hi! I'm " + this.name + '.');
  },
}
```