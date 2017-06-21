# ES6: Declare a Read-Only Variable with the const Keyword

let is not the only new way to declare variables. In ES6, you can also declare variables using the const keyword.

const has all the awesome features that let has, with the added bonus that variables declared using const are read-only. They are a constant value, which means that once a variable is assigned with const, it cannot be reassigned.

```javascript
"use strict"
const FAV_PET = "Cats";
FAV_PET = "Dogs"; // returns error
```
As you can see, trying to reassign a variable declared with const will throw an error. You should always name variables you don't want to reassign using the const keyword. This helps when you accidentally attempt to reassign a variable that is meant to stay constant. A common practice is to name your constants in all upper-cases and with an underscore to separate words (e.g. EXAMPLE_VARIABLE).

### Instructions
Change the code so that all variables are declared using let or const. Use let when you want the variable to change, and const when you want the variable to remain constant. Also, rename variables declared with const to conform to common practices.

## Code

### Original
```javascript
// change 'var' to 'let' or 'const'
// rename constant variables
var pi = 3.14;
var radius = 10;
var calculateCircumference = function(r) {
  var diameter = 2 * r;
  var result = pi * diameter;
  return result;
};
// Test your code
console.log(calculateCircumference(radius));
```

### Answer
```javascript
'use strict';
// change 'var' to 'let' or 'const'
// rename constant variables
const PI = 3.14;
let radius = 10;
const CALCULATE_CIRCUMFERENCE = function(r) {
  var diameter = 2 * r;
  var result = PI * diameter;
  return result;
};
// Test your code
console.log(CALCULATE_CIRCUMFERENCE(radius));
```
