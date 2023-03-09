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

##Type conversions
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

# Midterm Review
## Video
