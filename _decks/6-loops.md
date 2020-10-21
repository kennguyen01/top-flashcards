---
title: 6 - Loops
---

1a. while loop
1b.
```js
/* Creates a loop that executes as long as the test condition is true.
Condition is evaluated before execution. */
let n = 0;

while (n < 3) {
  n++;
}

console.log(n);   // 3
```

2a. do...while loop
2b.
```js
/* Creates a loop that executes until the test condition is false.
Condition is evaluated after execution. Statement executes at least once */
let result = '';
let i = 0;

do {
  i++;
  result += i;
} while (i < 5)

console.log(result);    // '12345'
```

3a. for loop
3b.
```js
/* Creates a loop with three optional expressions: initialization, condition, and step.
Any part of for loop can be skipped. */
let str = '';

for (let i = 0; i < 0; i++) {
  str += i;
}

console.log(str);   // '012345678'
```

4a. break statement
4b.
```js
/* Terminates current loop, switch, or label.
Transfer control the statement following the loop. */
let i = 0;

while (i < 6) {
  if (i === 3) {
    break;
  }
  i++;
}

console.log(i);   // 3
```

5a. continue statement
5b.
```js
/* Terminates execution of statements in current iteration.
Continues execution with next iteration. */
for (let i = 0; i < 10; i++) {
  if (i % 2 == 0) continue
  
  alert(i);   // 1, 3, 5, 7, 9
}
```

6a. label statement
6b.
```js
/* Identifier to refer to a loop. Used with break or continue statement.
Can break out of multiple nested loops. */
outer: 
for (let i = 0; i < 3; i++) {    // label must be above break/continue
  for (let j = 0; j < 3; j++) {
    let input = prompt(`Value at coords (${i}, ${j})`, '');

    // Break loop if empty string or canceled
    if (!input) break outer;

    // Do something with coordinates
  }
}
alert('Done');
```