---
title: 8 - Constructor
---

1a. Define object
1b.
```js
// Object literal
const myObject = {
  property: 'Value',
  otherProperty: 77,
  'obnoxious property': function() {
    // Code block
  }
};
```

2a. Access object
2b.
```js
// Dot notation
myObject.property;

// Bracket notation
let prop = 'property';
myObject[prop];
```

3a. Object constructor
3b.
```js
// Create object via constructor
function Player(name, marker) {
  this.name = name;
  this.marker = marker;
  // Object can have function
  this.sayName = function() {
    console.log(name);
  }
}

// Call constructor with new keyword
const player = new Player('Steve', 'X');
player.sayName();   // Steve
```

4a. Prototype
4b. Every object in JS inherits from a prototype.The object has access to all of its prototype's methods and properties.

5a. Prototype property
5b.
```js
/* Every function has a default empty prototype property.
Methods and properties can be attached to the prototype to pass it on to instances of that prototype. */
function PrintStuff(myDocuments) {
  this.documents = myDocuments;
}

// Add print() method to prototype
PrintStuff.prototype.print = function() {
  console.log(this.documents);
}

// newObj inherit all properties and methods
const newObj = new PrintStuff('I am a new object and I can print');
newObj.print();   // I am a new object and I can print
```

5a. Prototype attribute
5b. 
```js
/* Characteristics inherited from parent of the object. 
Normally referred to as prototype object and points to the parent. */

function Account() {
  // Code block
}

// Prototype attribute of userAccount is Account.prototype
const userAccount = new Account();
```

6a. Prototype chain
6b. JS only has one construct: object. Each object has a private property which holds a link to its object prototype. That prototype has its own prototype and so on until null is the final link in the prototype chain.

7a. Object.create()
7b.
```js
// Creates a new object, using an existing object as prototype
const person = {
  isHuman: false,
  printIntro: function() {
    console.log(`My name is ${this.name}. Am I human? ${this.isHuman}`);
  }
};

const matt = Object.create(person);
matt.name = 'Matthew';
matt.isHuman = true;

matt.printIntro();    // My name is Matthew. Am I human? true
```

8a. Constructor property
8b.
```js
// All objects have a constructor property that points to the original constructor function
function Person() {
  // Code block
}

const person1 = Person();
person1.constructor;    // Person()
```

9a. Prototype performance
9b. Lookup time for properties high up the prototype chain can have negative impact on perfromance. Trying to access nonexistant properties will always traverse the full prototype chain.

10a. .hasOwnProperty()
10b. When iterating over the properties of an object, every enumerable property chain will be enumerated. To check if an objet has a property defined on itself and not its prototype chain, use .hasOwnProperty(). It's the only method that deals with properties but does not traverse the prototype chain.