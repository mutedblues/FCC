# ES6: Explore Problems with the var Keyword

One of the biggest problems with declaring variables with the var keyword is that you can overwrite variable declarations without an error.

```javascript
var camper = 'James';
var camper = 'David';
console.log(camper);
// logs 'David'
```
In a small application, you might not run into this type of problem, but when your code becomes larger, you might accidently overwrite a variable that you did not intend to overwrite. Because this behaviour does not throw an error, searching and fixing bugs becomes more difficult.

Another problem with the var keyword is that it is hoisted to the top of your code when it compiles. This means that you can use a variable before you declare it.

```javascript
console.log(camper);
var camper = 'David';
// logs undefined
```
The code runs in the following order:

1. The variable camper is declared as undefined.
2. The value of camper is logged.
3. David is assigned to camper.

This code will run without an error.

A new keyword called let was introduced in ES6 to solve the problems with the var keyword. With the let keyword, all the examples we just saw will cause an error to appear. We can no longer overwrite variables or use a variable before we declare it. Some modern browsers require you to add "use strict"; to the top of your code before you can use the new features of ES6.

Let's try using the let keyword.

## Instructions

Fix the code so that it only uses the let keyword and makes the errors go away.

Note: Remember to add "use strict"; to the top of your code.

## Code
### Original
```javascript

var favorite = redNosedReindeer + " is Santa's favorite reindeer.";
var redNosedReindeer = "Rudolph";
var redNosedReindeer = "Comet";
```

### Answer

```javascript
'use strict';

let redNosedReindeer = "Rudolph";
let favorite = redNosedReindeer + " is Santa's favorite reindeer.";
```
