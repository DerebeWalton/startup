# startup
## Start up application repository

  This is my modification using VS Code

  This is my modification using Github

  This a change using Github and VS Code

I learned that using fetch, pull, commit, and push, are critical to using Git. I got caught a few times forgetting to use fetch.
# Startup Deliverable - Specification Assignment
## Pitch
  Did you ever want to play Connect 4 online? This is the way! With color customization and win/loss tracking, you can make it your own game. Play with a computer or go online to compete with other players. With every win, you can jump up the leaderboards and claim the crown! 
## Key Features
  Play against computers or players
  
  Customize the colors of the game
  
  Live chat with opponents
  
  Track wins and losses against CPU and Online Players
  
  Play from anywhere
## Sketch
  ![Four-In-A-Row Game Sketch](https://user-images.githubusercontent.com/21244160/215238250-3f4565ae-d5c4-4c1f-ac44-b97df4608af3.png)

In addition to the previous git notations, "git add <file>" must be done first.

During Simon, I continued to learn the power of git as I at one point replaced my index.html file (that previously had about me info) with the index.html from simon. I was able to backtrack and fix my mistake without git, but the assurance that git had the file the whole time reassured me.

Also during Simon, I loved using one VS Code window to make my file edits for git and deployment while having another VS Code window to check the files on my server. Additionally, the quick and easy deployment made for fast checking of versions and adjustments when I messed things up.
# Simon CSS
During this assignment, a few bugs gave me some difficulty. CSS, although it's easy to spot the problems once the server is updated, makes it difficult to easily notice in code where the problem is. It's possible that VSCode just is not as helpful as JetBrains IDEs are or that I don't have as helpful extensions installed.
Basically, I need to be more careful when typing out code in CSS in VSCode or find a good extension to help me.

While working, I realized that having the separate file for formatting made my life way easier. When actually debugging, it was way easier to find and fix the problems compared with interdependent languages such as Java.

I need to study html tags more :)

# JavaScript Basics
## Functions and output
```js
function join(a, b) {
  return a + ' ' + b;
}
```
```js
console.log(join('Hello', 'world'));
// OUTPUT: Hello world
```
## Comments

```js
// Line comment
```

```js
/*
Block comment
*/
```

It's good form to use braces and semicolons

# JS Console
## Log
```js
console.log('%c JavaScript Demo', 'font-size:1.5em; color:green;');
// OUTPUT: JavaScript Demo //in large green text
```

## Timers
```js
console.time('demo time');
// ... some code that takes a long time.

console.timeEnd('demo time');
// OUTPUT: demo time: 9762.74 ms
```

## Count
```js
console.count('a');
// OUTPUT: a: 1

console.count('a');
// OUTPUT: a: 2

console.count('b');
// OUTPUT: b: 1
```

# Adding JavaScript to HTML
Insert directly using <script> or reference using src attribute
## index.js
```js
function sayHello() {
  console.log('hello');
}
```
## index.html
```html
<head>
  <script src="javascript.js"></script>
</head>
<body>
  <button onclick="sayHello()">Say Hello</button>
  <button onclick="sayGoodbye()">Say Goodbye</button>
  <script>
    function sayGoodbye() {
      alert('Goodbye');
    }
  </script>
</body>
```
## onclick and other special attributes
```html
<button onClick="let i=1;i++;console.log(i)">press me</button>
<!-- OUTPUT: 2 -->
```

# JavaScript type and construct
## Variables
```let``` allows for changes and ```const``` does not
```js
let x = 1;

const y = 2;
```
## Primitive Types
| Type        | Meaning                                                    |
| ----------- | ---------------------------------------------------------- |
| `Null`      | The type of a variable that has not been assigned a value. |
| `Undefined` | The type of a variable that has not been defined.          |
| `Boolean`   | true or false.                                             |
| `Number`    | A 64 bit signed number.                                    |
| `BigInt`    | A number of arbitrary magnitude.                           |
| `String`    | A textual sequence of characters.                          |
| `Symbol`    | A unique value.                                            |

## Commonly used objects:
| Type       | Use                                                                                    | Example                  |
| ---------- | -------------------------------------------------------------------------------------- | ------------------------ |
| `Object`   | A collection of properties represented by name value pairs. Values can be of any type. | `{a:3, b:'fish'}`        |
| `Function` | An object that has the ability to be called.                                           | `function a() {}`        |
| `Date`     | Calendar dates and times.                                                              | `new Date('1995-12-17')` |
| `Array`    | An ordered sequence of any type.                                                       | `[3, 'fish']`            |
| `Map`      | A collection of key value pairs that support efficient lookups.                        | `new Map()`              |
| `JSON`     | A lightweight data-interchange format used to share information across programs.       | `{"a":3, "b":"fish"}`    |

## Common operators
Math operators:
 - ```+``` add
 - ```-``` subtract
 - ```*``` multiply
 - ```/``` divide
 - ```===``` equality
For String variables:
 - ```+``` concatenation
 - ```===``` equality

## Type conversions
JS is weakly typed, therefore variables can change type and can get weird
```js
2 + '3';
// OUTPUT: '23'
2 * '3';
// OUTPUT: 6
[2] + [3];
// OUTPUT: '23'
true + null;
// OUTPUT: 1
true + undefined;
// OUTPUT: NaN
```
Weird stuff especially with ```equality``` operator
```js
1 == '1';
// OUTPUT: true
null == undefined;
// OUTPUT: true
'' == false;
// OUTPUT: true
```
Use ```===``` and ```!==``` for strict equality and inequality
```js
1 === '1';
// OUTPUT: false
null === undefined;
// OUTPUT: false
'' === false;
// OUTPUT: false
```
Example:
```js
('b' + 'a' + +'a' + 'a').toLowerCase();
// OUTPUT: 'banana'
```

## Conditionals
JS supports common conditional constructs, including ```if```, ```else```, and ```else if```
```js
if (a === 1) {
  //...
} else if (b === 2) {
  //...
} else {
  //...
}
```
Ternary operator provides compact ```else if``` representation
```js
a === 1 ? console.log(1) : console.log('not 1');
```

Boolean operations also supported:
 - ```&&``` and
 - ```||``` or
 - ```!``` not

Example:
```js
if (true && (!false || true)) {
  //...
}
```

## Loops
### for

Note the introduction of the common post increment operation (`i++`) for adding one to a number.

```js
for (let i = 0; i < 2; i++) {
  console.log(i);
}
// OUTPUT: 0 1
```

### do while

```js
let i = 0;
do {
  console.log(i);
  i++;
} while (i < 2);
// OUTPUT: 0 1
```

### while

```js
let i = 0;
while (i < 2) {
  console.log(i);
  i++;
}
// OUTPUT: 0 1
```

### for in

The `for in` statement iterates over an object's property names.

```js
const obj = { a: 1, b: 'fish' };
for (const name in obj) {
  console.log(name);
}
// OUTPUT: a
// OUTPUT: b
```

For arrays the object's name is the array index.

```js
const arr = ['a', 'b'];
for (const name in arr) {
  console.log(name);
}
// OUTPUT: 0
// OUTPUT: 1
```

### for of

The `for of` statement iterates over an iterable's (Array, Map, Set, ...) property values.

```js
const arr = ['a', 'b'];
for (const val of arr) {
  console.log(val);
}
// OUTPUT: 'a'
// OUTPUT: 'b'
```

### Break and continue

All of the looping constructs demonstrated above allow for either a `break` or `continue` statement to abort or advance the loop.

```js
let i = 0;
while (true) {
  console.log(i);
  if (i === 0) {
    i++;
    continue;
  } else {
    break;
  }
}
// OUTPUT: 0 1
```

# JS String
Strings are a primitive type in JavaScript. A string variable is specified by surround a sequence of characters with single quotes (`'`), double quotes (`"`), or backticks (\`). The meaning of single or double quotes are equivalent, but the backtick defines a string literal that may contain JavaScript that is evaluated in place and concatenated into the string. A string literal replacement specifier is declared with a dollar sign followed by a curly brace pair. Anything inside the curly braces is evaluated as JavaScript. You can also use backticks to create multiline strings without having to explicitly escape the newline characters using `\n`.
```js
'quoted text'; // " also works

const l = 'literal';
console.log(`string ${l + (1 + 1)} text`);
// OUTPUT: string literal2 text
```

## Unicode support
JavaScript supports Unicode by defining a string as a 16-bit unsigned integer that represents UTF-16 strings. Unicode support allows JavaScript to represent most languages spoken on the planet. This includes those that are read from right to left.
However, there are several important steps you must take in order to make your web application fully internationalized. This includes handling of currency, time, dates, iconography, units of measure, keyboard layouts, and respecting local customs.

## String functions
Commonly used string object functions:
| Function    | Meaning                                                      |
| ----------- | ------------------------------------------------------------ |
| length      | The number of characters in the string                       |
| indexOf     | The starting index of a given substring                      |
| split       | Split the string into an array on the given delimiter string |
| startsWith  | True if the string has a given prefix                        |
| endsWith    | True if the string has a given suffix                        |
| toLowerCase | Converts all characters to lowercase                         |

```js
const s = 'Example:조선글';

console.log(s.length);
// OUTPUT: 11
console.log(s.indexOf('조선글'));
// OUTPUT: 8
console.log(s.split(':'));
// OUTPUT: ['Example', '조선글']
console.log(s.startsWith('Ex'));
// OUTPUT: true
console.log(s.endsWith('조선글'));
// OUTPUT: true
console.log(s.toLowerCase());
// OUTPUT: example:조선글
```

# Functions
Function begins with keyword ```function``` followed by 0 or more parameters and a body that may contain 0 or more return statements. Note: no type declarations, as the type is always inferred by the assignment of the value to the parameter.
```js
function hello(who) {
  return 'hello ' + who;
}

console.log(hello('world'));
// OUTPUT: hello world
```

Functions without return values also exist:
```js
function hello(who) {
  who.count++;
  console.log('hello ' + who.name);
}

hello({ name: 'world', count: 0 });
// OUTPUT: hello world
```

## Funcation parameters
If caller does not provide parameters, then the value is ```undefined``` when the function executes
```js
function labeler(value, title = 'title') {
  console.log(`${title}=${value}`);
}

labeler();
// OUTPUT: title=undefined

labeler('fish');
// OUTPUT: title=fish

labeler('fish', 'animal');
// OUTPUT: animal=fish
```

## Anonymous functions
Functions in JavaScript are commonly assigned to a variable so that they can be passed as a parameter to some other function or stored as an object property. To easily support this common use you can define a function anonymously and assign it to a variable.
```js
// Function that takes a function as a parameter
function doMath(operation, a, b) {
  return operation(a, b);
}

// Anonymous function assigned to a variable
const add = function (a, b) {
  return a + b;
};

console.log(doMath(add, 5, 3));
// OUTPUT: 8

// Anonymous function assigned to a parameter
console.log(
  doMath(
    function (a, b) {
      return a - b;
    },
    5,
    3
  )
);
// OUTPUT: 2
```

## Creating, passing, and returning functions
Here are examples of assigning functions to variables, as well as using functions as parameters and return values.
```js
// Anonymous declaration of the function that is later assigned to a variable
const add = function (a, b) {
  return a + b;
};

// Function that logs as a side effect of its execution
function labeler(label, value) {
  console.log(label + '=' + value);
}

// Function that takes a function as a parameter and then executes the function as a side effect
function addAndLabel(labeler, label, adder, a, b) {
  labeler(label, adder(a, b));
}

// Passing a function to a function
addAndLabel(labeler, 'a+b', add, 1, 3);
// OUTPUT: a+b=4

// Function that returns a function
function labelMaker(label) {
  return function (value) {
    console.log(label + '=' + value);
  };
}

// Assign a function from the return value of the function
const nameLabeler = labelMaker('name');

// Calling the returned function
nameLabeler('value');
// OUTPUT: name=value
```

## Inner functions
make life easier
```js
function labeler(value) {
  function stringLabeler(value) {
    console.log('string=' + value);
  }
  function numberLabeler(value) {
    console.log('number=' + value);
  }

  if (typeof value == 'string') {
    stringLabeler(value);
  } else if (typeof value == 'number') {
    numberLabeler(value);
  }
}

labeler(5);
// OUTPUT: number=5

labeler('fish');
// OUTPUT: string=fish
```

# JS arrow function
To make the code more compact the ```arrow``` syntax was created. This syntax replaces the need for the ```function``` keyword with the symbols ```=>``` placed after the parameter declaration.
arrow function syntax that returns 3:
```js
() => 3;
```
Sort of equivalent:
```js
const a = [1, 2, 3, 4];

// standard function syntax
a.sort(function (v1, v2) {
  return v1 - v2;
});

// arrow function syntax
a.sort((v1, v2) => v1 - v2);
```
## Return values
```return``` keyword is not required unless curly braces are used
```js
() => 3;
// RETURNS: 3

() => {
  3;
};
// RETURNS: undefined

() => {
  return 3;
};
// RETURNS: 3
```

## This pointer
arrow functions inherit ```this``` pointer from creation. Makes a ```closure```, which allows a function to continue referening its creation scope, even after it has passed out of scope. More to be discussed about ```scope``` later.

The function ```makeClosure``` returns an anonymous function using the arrow syntax. Notice that the ```a``` parameter is overridden, a new ```b``` variable is created, and both ```a``` and ```b``` are referenced in the arrow function. Because of that reference, they are both part of the closure for the returned function.
```js
function makeClosure(a) {
  a = 'a2';
  const b = 'b2';
  return () => [a, b];
}
```
Next, we declare the variables ```a``` and ```b``` at the top level scope, and call ```makeClosure``` with ```a```.
```js
const a = 'a';
const b = 'b';

const closure = makeClosure(a);
```
Now, when we call ```closure``` function it will output the values contained in scope where it was created instead of the current values of the variables.
```js
console.log(closure());
// OUTPUT: ['a2', 'b2']

console.log(a, b);
// OUTPUT: 'a' 'b'
```
Closures provide a valuable property when we do things like execute JavaScript within the scope of an HTML page, because it can remember the values of variables when the function was created instead of what they are when they are executed.

# JS array
JS array objects represent a sequence of other objects and primitives. It's zero based
```js
const a = [1, 2, 3];
console.log(a[1]);
// OUTPUT: 2

console.log(a.length);
// OUTPUT: 3
```

## Object functions
Array has several interesting static functions. A few:
| Function | Meaning                                                   | Example                       |
| -------- | --------------------------------------------------------- | ----------------------------- |
| push     | Add an item to the end of the array                       | `a.push(4)`                   |
| pop      | Remove an item from the end of the array                  | `x = a.pop`                   |
| slice    | Return a sub-array                                        | `a.slice(1,-1)`               |
| sort     | Run a function sort an array in place                     | `a.sort((a,b) => b-a)`        |
| values   | Creates an iterator for use with a `for of` loop          | `for (i of a.values()) {...}` |
| find     | Find the first item satisfied by a test function          | `a.find(i => i < 2)`          |
| forEach  | Run a function on each array item                         | `a.forEach(console.log)`      |
| reduce   | Run a function to reduce each array item to a single item | `a.reduce((a, c) => a + c)`   |
| map      | Run a function to map an array to a new array             | `a.map(i => i+i)`             |
| filter   | Run a function to remove items                            | `a.filter(i => i%2)`          |
| every    | Run a function to test if all items match                 | `a.every(i => i < 3)`         |
| some     | Run a function to test if any items match                 | `a.some(i => 1 < 1)`          |

```js
const a = [1, 2, 3];

console.log(a.map((i) => i + i));
// OUTPUT: [2,4,6]
console.log(a.reduce((v1, v2) => v1 + v2));
// OUTPUT: 6
console.log(a.sort((v1, v2) => v2 - v1));
// OUTPUT: [3,2,1]

a.push(4);
console.log(a.length);
// OUTPUT: 4
```




# Midterm Review
## Video
