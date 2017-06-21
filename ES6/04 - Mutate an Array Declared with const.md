# ES6: Mutate an Array Declared with const

The const declaration has many use-cases in modern JavaScript.

Some developers prefer to assign all their variables using const by default, unless they know they will need to reassign the value. Only in that case, they use let.

However, it is important to understand that objects (including arrays and functions) assigned to a variable using const are still mutable. Using the const declaration only prevents reassignment of the variable identifier.

```javascript
"use strict";
const s = [5, 6, 7];
s = [1, 2, 3]; // throws error, trying to assign a const
s[7] = 45; // works just as it would with an array declared with var
```
As you can see, you can mutate the object ([5, 6, 7]) itself and the variable identifier (s) will still point to the altered array. Like all arrays, the array assigned to s is mutable, but because const was used, you cannot use the variable identifier, s, to point to a different array using the assignment operator.

To make an object immutable, you can use Object.freeze().

### Instructions
An array is declared as const s = [5, 7, 2]. Change the array to [2, 5, 7].

## Code

### Original
```javascript
const s = [ 5, 7, 2 ];
// change code below this line
s = [2, 5, 7];
// change code above this line
// Test your code
console.log(s);
```
### Answer
```javascript
'use strict';
const s = [ 5, 7, 2 ];
// change code below this line
s[0] = 2;
s[1] = 5;
s[2] = 7;
// change code above this line
// Test your code
console.log(s);
```

## My Notes
I tried to find a solution for replacing multiple array elements at the same time but didn't find anything useful. Will need to revisit in the future...would love to find out if this is possible here.
