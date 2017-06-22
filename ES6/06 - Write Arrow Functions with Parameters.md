# ES6: Write Arrow Functions with Parameters

Just like a normal function, you can pass arguments into arrow functions.

```javascript
// doubles input value and returns it
const doubler = (item) => item * 2;
```
You can pass more than one argument into arrow functions as well.

### Instructions

Rewrite the myConcat function which appends contents of arr2 to arr1 so that the function uses arrow function syntax.

## Code

### Original

```javascript
// change code below this line
var myConcat = function(arr1, arr2) {
  return arr1.concat(arr2);
}
// change code above this line
// test your code
console.log(myConcat([1, 2], [3, 4, 5]));
```

### Answer

```javascript
'use strict';
// change code below this line
const myConcat = (arr1, arr2) => arr1.concat(arr2);

// change code above this line
// test your code
console.log(myConcat([1, 2], [3, 4, 5]));
```
