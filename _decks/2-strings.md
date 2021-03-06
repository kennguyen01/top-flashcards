---
title: 2 - Strings
---

1a. String
1b. Data type used to represent and manipulate a sequence of characters.

2a. Declaring strings
2b.
```js
// Single or double quotes
let start = 'Hello';
let end = "World";
```

3a. Escaping characters
3b.
```js
// Escape characters with backslash \ to recognize them as text
let mood = 'I\'m feeling blue';
```

4a. Concatenating strings
4b.
```js
// Strings can be joined together using the + operator
let one = 'Hello, ';
let two = 'how are you?';
let joined = one + two;   // 'Hello, how are you?'
```

5a. Template literals
5b.
```js
// Expressions can be embedded with ${exp} using backtick `
let grade = 90;
let output = `I got a score of ${grade} on the last exam.';
```

6a. str.length
6b.
```js
// Property that returns the length of a string
let answer = 'Life, the universe and everything. Answer:';
let strLen = answer.length;   // 42
```

7a. str.indexOf()
7b.
```js
// Return the first index of a specified text, -1 if not found
let sentence = 'The quick brown fox jumps over the lazy dog.';
let foxIndex = sentence.indexOf('fox');   // 16
```  

8a. str.lastIndexOf()
8b.
```js
// Return the last index of a specified text, -1 if not found.
let phrase = 'I like reading but I like video games more.';
let likeIndex = phrase.lastIndexOf('like');   // 21
```

9a. str.search()
9b.
```js
// Search a string for specified value and returns position of the match
// Can be used with regular expression.
let paragraph = 'If the dog barked, was it reallly lazy?';
let regex = /[^\w\s]/g;

let searchPara = paragraph.search(regex);   // 17
```

10a. str.slice()
10b. 
```js
// Extract a section of a string and returns it as a new string, without modifying the original
let sentence = 'The quick brown fox jumps over the lazy dog.';
let fox = sentence.slice(4, 19);    // 'quick brown fox'
```

11a. str.substring()
11b.
```js
// Return the part of the string between the start and end indexes
let name = 'Mozilla';
let end = name.substring(2);    // 'zilla'
```

12a. str.substr()
12b.
```js
// Return a portion of the string, starting at index with a length parameter
let name = 'Mozilla';
let part = name.substr(1, 2);   // 'oz'
```

13a. str.replace()
13b.
```js
// Return a new string with specified replacement value
// Can be used with regular expression
let invite = 'Come visit Google';
let newInvite = invite.replace('Google', 'Microsoft');    // 'Come visit Microsoft'
```

14a. str.toUpperCase()
14b.
```js
// Return new string converted to uppercase
let say = 'i am not yelling';
let yell = say.toUpperCase();   // 'I AM NOT YELLING'
```

15a. str.toLowerCase()
15b.
```js
// Return new string converted to lowercase
let say = 'LET ME WHISPER THIS TO YOU';
let whisper = say.toLowerCase();    // 'let me whisper this to you
```

16a. str.concat()
16b.
```js
// Concatenate string arguments to the calling string and return a new string
let start = 'Hello ';
let end = 'World';
let word = start.concat(end);   // 'Hello World'
```

17a. str.trim()
17b.
```js
// Remove whitespace from both ends of a string
let word = '     Too much space     ';
let newWord = word.trim();    // 'Too much space'
```

18a. str.charAt()
18b.
```js
// Return the character at specified index
let saying = 'Hello there';
let first = saying.charAt(0);   // 'H'
```

19a. str.charCodeAt()
19b.
```js
// Return a UTF-16 code at specified index
let saying = 'Hello';
let firstCode = saying.charCodeAt(0);   // 72
```

20a. str.split()
20b.
```js
// Divide the string into array of substrings with optional separator
let letters = 'a,b,c,d,e';
let lettersArr = letters.split(',');    // [ 'a', 'b', 'c', 'd', 'e' ]
```