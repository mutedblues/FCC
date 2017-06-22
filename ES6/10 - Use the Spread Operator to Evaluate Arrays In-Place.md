# ES6: Use the Spread Operator to Evaluate Arrays In-Place

ES6 introduces the spread operator, which allows us to expand arrays and other expressions in places where multiple parameters or elements are expected.

The ES5 code below uses apply() to compute the maximum value in an array:

```javascript
var arr = [6, 89, 3, 45];
var maximus = Math.max.apply(null, arr); // returns 89
```
We had to use Math.max.apply(null, arr) because Math.max(arr) returns NaN. Math.max() expects comma-separated arguments, but not an array.

The spread operator makes this syntax much better to read and maintain.

```javascript
const arr = [6, 89, 3, 45];
const maximus = Math.max(...arr); // returns 89
```
...arr returns an unpacked array. In other words, it spreads the array.

However, the spread operator only works in-place, like in an argument to a function or in an array literal. The following code will not work:

```javascript
const spreaded = ...arr; // will throw a syntax error
```

### Instructions
Copy all contents of arr1 into another array arr2 using the spread operator.

## Code
### Original

```javascript
const arr1 = ['JAN', 'FEB', 'MAR', 'APR', 'MAY'];
const arr2 = []; // change this line
arr1.push('JUN');
console.log(arr2); // arr2 should not be affected
```

### Answer

```javascript
'use strict';
const arr1 = ['JAN', 'FEB', 'MAR', 'APR', 'MAY'];
const arr2 = [...arr1]; // change this line
arr1.push('JUN');
console.log(arr2); // arr2 should not be affected
```
