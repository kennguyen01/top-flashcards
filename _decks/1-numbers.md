---
title: 1 - Numbers
---

1a. Number
1b. JS has only one type of number. It can be written with or without decimals.

2a. Declaring number
2b.
```js
let x = 3;
let y = 3.14;
```

3a. Numeric strings
3b. JS will try to convert strings to numbers in all numeric operations.

4a. Adding string and number
4b.
```js
let x = '10';
let y = '20;

console.log(x + y);   // result is string '1020'
```

5a. NaN (Not a Number)
5b. Reserved keyword indicating that a number is not legal. Trying to do arithmetic with non-numeric string will result in NaN.

6a. Infinity or -Infinity
6b. The value JS will return if you calculate a number outside the largest possible number. Division by zero also results in Infinity.

7a. Hexadecimal
7b. JS interprets numeric values as hex if they are preceded by 0x (0xFF will be 255).

8a. num.toString()
8b.
```js
// Return a string of the object with optional base 2 to base 36
let myNum = 10;

myNum.toString();     // string '10'
myNum.toString(2);    // binary '1010'
myNum.toString(16);   // hexadecimal 'a'
```

9a. Arithmetic operators
9b.
```js
+   // addition
-   // subtraction
*   // multiplication
/   // division
**  // exponentiation
%   // modulus (remainder)
```

10a. ++ (incrementing)
10b.
```js
// Postfix
let x = 3;
y = x++;    // y = 3, x = 4

// Prefix
let a = 2;
b = ++a;    // a = 3, b = 3
```

11a. -- (decrementing)
11b.
```js
// Postfix
let x = 3;
y = x--;    // y = 3, x = 2

// Prefix
let a = 2;
b = --a;    // a = 1, b = 1
```

12a. Math.pow(x, y)
12b. Produces the same result as x**y.

13a. - (unary)
13b.
```js
let x = 1;

x = -x;   // -1
```

14a. + (unary)
14b.
```js
// Convert non-numeric to number
let x = +true;    // 1
let y = +'2';     // 2
```

15a. = (assignment)
15b.
```js
// Calculations are done before assignment
let x = 2 * 2 + 1;    // 5

// Assignment operator writes the value and then returns it
let a = 1;
let b = 2
let c = 3 - (a = b + 1);    // a = 3, c = 0
```

16a. Chaining assignments
16b.
```js
let a, b, c;

// All variables share a single value
a = b = c = 2 + 2;
```

17a. Modify in-place
17b.
```js
let n = 2;

n += 5;   // n = 7
n *= 2;   // n = 14
```

18a. Comma
18b.
```js
// Evaluates multiple expressions, separated by comma
// Only return the last result
let a = (1 + 2, 3 + 4);   // Return 7
```

19a. Variable
19b.
```js
// Named reference for data declared with let keyword
let message = 'hello';

// Can be declared on one line
let x = 1, b = 2, c = 3;
```
