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
Insert directly using <script> or referect using src attribute
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
# Midterm Review
## Video
