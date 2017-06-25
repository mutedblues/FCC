# Debugging: Use typeof to Check the Type of a Variable

You can use typeof to check the data structure, or type, of a variable. This is useful in debugging when working with multiple data types. If you think you're adding two numbers, but one is actually a string, the results can be unexpected. Type errors can lurk in calculations or function calls. Especially take care when you're accessing and working with external data in the form of a JavaScript object (JSON).

Here are some examples using typeof:

```javascript
console.log(typeof ""); // outputs "string"
console.log(typeof 0); // outputs "number"
console.log(typeof []); // outputs "object"
console.log(typeof {}); // outputs "object"
```
JavaScript recognizes six primitive (immutable) data types: Boolean, Null, Undefined, Number, String, and Symbol (new with ES6) and one type for mutable items: Object. Note that in JavaScript, arrays are technically a type of object.

### Instructions

Add two console.log() statements to check the typeof each of the two variables seven and three in the code.

## Code

### Original

```javascript
let seven = 7;
let three = "3";
console.log(seven + three);
// Add your code below this line
```

### Solution

```javascript
let seven = 7;
let three = "3";
console.log(seven + three);
// Add your code below this line
console.log(typeof seven);
console.log(typeof three);
```
