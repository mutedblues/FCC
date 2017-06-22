# ES6: Use Destructuring Assignment to Assign Variables from Arrays

ES6 makes destructuring arrays as easy as destructuring objects.

One key difference between the spread operator and array destructuring is that the spread operator unpacks all contents of an array into a comma-separated list. Consequently, you cannot pick or choose which elements you want to assign to variables.

Destructuring an array lets us do exactly that:

```javascript
const [a, b] = [1, 2, 3, 4, 5, 6];
console.log(a, b); // 1, 2
```
The variable a is assigned the first value of the array, and b is assigned the second value of the array.

We can also access the value at any index in an array with destructuring by using commas to reach the desired index:

```javascript
const [a, b,,, c] = [1, 2, 3, 4, 5, 6];
console.log(a, b, c); // 1, 2, 5 
```
### Instructions

Use destructuring assignment to swap the values of a and b so that a receives the value stored in b, and b receives the value stored in a.

## Code

### Original

```javascript
let a = 8, b = 6;
// change code below this line

// change code above this line
console.log(a); // should be 6
console.log(b); // should be 8
```
### Solution

```javascript
'use strict';
let a = 8, b = 6;
// change code below this line
[b, a] = [a, b];
// change code above this line
console.log(a); // should be 6
console.log(b); // should be 8
```
