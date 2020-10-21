---
title: 3 - Conditionals
---

1a. Comparison of different types
1b.
```js
// JS converts values to numbers if they are different types
alert('2' > 1);     // true
alert(true == 1);   // true
```

2a. == (loose equality)
2b.
```js
// Converts different types to a common one when comparing
alert(0 == false);    // true
```

3a. === (strict equality)
3b.
```js
// Consider operands of different types to be different
alert(0 === false);   // false
```

4a. if...else statement
4b.
```js
// Executes statement if condition is true
// Otherwise another statement can be executed
if (condition1) {
  // Code block 1
} else if (condition2) {
  // Code block 2
} else {
  // Code block 3
}
```

5a. || (OR)
5b. Return true if any operand is true, false otherwise. In a chain of OR, it returns the first true value or the last value if none is found.

6a. && (AND)
6b. Return true if all operands are true, false otherwise. In a chain of AND, it returns the first false value or the last value if none is found.

7a. ! (NOT)
7b. Convert the operand to boolean type and return the inverse value.

8a. Conditional operator
8b.
```js
// Shortcut for the if statement
let result = conditon ? value1 : value2;
```

9a. switch statement
9b.
```js
// Evaluate an expression and matching value to a case
switch (expression) {
  case x:
    // Code block x
    break;
  case y:
    // Code block y
    break;
  default:
    // Default code block
}
```