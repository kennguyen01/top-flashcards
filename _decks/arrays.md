---
title: Arrays
---

1a. Array
1b. Ordered collection of objects. Elements can be of any type.

2a. Declaring array
2b.
```js
let arr = [];

// Initial elements can be included in array
let fruits = ['Apple', 'Banana', 'Orange'];
```

3a. Accessing array
3b.
```js
// Elements can be accessed using its index value
let letters = ['a', 'b', 'c'];
alert(letters[0]);    // 'a'
```

4a. Modifying array
4b.
```js
let cars = ['Toyota', 'Testla', 'BMW'];

// Replace element
cars[2] = 'Honda';  // ['Toyota', 'Testla', 'Honda']

// Add element
cars[3] = 'Ford';   // ['Toyota', 'Testla', 'Honda', 'Ford']
```

5a. arr.length
5b. Array length property.

6a. arr.pop()
6b.
```js
// Extract last element and return it

let fruits = ['Apple', 'Orange', 'Pear'];
fruits.pop();  // 'Pear'
```

7a. arr.push()
```js
// Append element to the end of array
// Can add multiple elements

let meats = ['Chicken', 'Beef'];
meats.push('Pork');   // ['Chicken', 'Beef', 'Pork']
```

8a. arr.shift()
8b.
```js
// Extract first element and return it

let fruits = ['Apple', 'Orange', 'Pear'];
fruits.shift(); // 'Apple'
```

9a. arr.unshift()
9b.
```js
// Add element to beginning of the array
// Can add multiple elements

let fruits = ['Orange', 'Pear'];
fruits.unshift('Apple');    // ['Apple', 'Orange', 'Pear']
```

10a. Looping through array
10b.
```js
let arr = ["Apple", "Orange", "Pear"];

// Loop over indexes
for (let i = 0; i < arr.length; i++) {
  alert(arr[i]);
}

// Loop over elements
for (let fruit of fruits) {
  alert(fruit);
}
```

11a. Multidimensional array
11b.
```js
// Array can contain other arrays
let matrix = [
  [1, 2, 3],
  [4, 5, 6],
  [7, 8, 9]
];
```

12a. arr.toString()
12b.
```js
// Return a string of comma separated elements

let arr = [1, 2, 3];
alert( arr ); // '1,2,3'
```

13a. arr.splice()
13b.
```js
/* arr.splice(start[, deleteCount, elem1, ..., elemeN])

Change the content of the array by removing, replacing, or adding elements.
Modify from index start, remove deleteCount, and insert elem1, ..., elemN at their place */

// Delete element
let arr = ["I", "study", "JavaScript"];
arr.splice(1, 1);   // from index 1 remove 1 element
alert(arr);       // ["I", "JavaScript"]


// remove 3 first elements and replace them with another
let arr = ["I", "study", "JavaScript", "right", "now"];
arr.splice(0, 3, "Let's", "dance");
alert(arr)      // now ["Let's", "dance", "right", "now"]
```

14a. Negative index
14b. Negative indexes specify the position from the end of the array.

15a. arr.slice()
15b.
```js
// arr.slice([start], [end])
// Return a new array from index start to end

let arr = ["t", "e", "s", "t"];
alert( arr.slice(1, 3) );     // ['e', 's'] (copy from 1 to 3)
alert( arr.slice(-2) );       // ['s', 't'] (copy from -2 till the end)
```

16a. arr.concat()
16b.
```js
// arr.concat(arg1, arg2...)
// Return a new array that includes values from other arrays and items

let arr = [1, 2];
console.log(arr.concat([3, 4], 5, 6));    // [1, 2, 3, 4, 5, 6]
```

17a. arr.forEach()
17b.
```js
// Execute function for every element in the array

arr.forEach(function(item, index, array) {
  // ... do something with item
});
```

18a. arr.includes()
18b.
```js
// Search for item starting at index from, return true if found

let arr = [1, 0, false];
alert(arr.includes(1));   // true
```

19a. arr.find()
19b.
```js
// Return the value of the first element satifying specific condition

let result = arr.find(function(item, index, array) {
  // if true is returned, item is returned and iteration is stopped
  // for falsy scenario return undefined
});
```

20a. arr.filter()
20b.
```js
// Return new array with elements matching specific condition

let results = arr.filter(function(item, index, array) {
  // if true item is pushed to results and the iteration continues
  // Return empty array if nothing found
});
```

21a. arr.map()
21b.
```js
// Call the function for each element and return the new array

let result = arr.map(function(item, index, array) {
  // returns the new value instead of item
});
```

22a. arr.sort()
22b.
```js
// Sort the array in place, changing the order of the elements.

// Convert to string for comparison by default
let arr = [ 1, 2, 15 ];
arr.sort();     // [1, 15, 2]

// Sorting numbers by providing comparison function
arr.sort((a, b) => a - b);    // [1, 2, 15]
```

23a. arr.reverse()
23b. Reverse the order of elements in an array.

24a. str.split()
24b.
```js
// Split string into array with optional delimiter

let names = 'Bilbo, Gandalf, Nazgul';
let arr = names.split(', ');

for (let name of arr) {
  alert(name);
}
```

25a. arr.join()
25b.
```js
// Return a new string by joining elements together with optional delimiter

let arr = ['Bilbo', 'Gandalf', 'Nazgul'];
let str = arr.join(', ');   // Bilbo, Gandalf, Nazgul
```

26a. arr.reduce()
26b.
```js
/* Calculate a single value based on the array.
 Result of previous function call is passed to the next as the first argument

let value = arr.reduce(function(accumulator, item, index, array) {
  // ...
}, [initial]);
*/

let arr = [1, 2, 3, 4, 5];

// removed initial value from reduce (no 0)
let result = arr.reduce((sum, current) => sum + current);

alert( result );    // 15
```