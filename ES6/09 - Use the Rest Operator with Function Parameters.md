# ES6: Use the Rest Operator with Function Parameters

In order to help us create more flexible functions, ES6 introduces the rest operator for function parameters. With the rest operator, you can create functions that take a variable number of arguments. These arguments are stored in an array that can be accessed later from inside the function.

Check out this code:

```javascript
function howMany(...args) {
  return "You have passed " + args.length + " arguments.";
}
console.log(howMany(0, 1, 2)); // You have passed 3 arguments
console.log(howMany("string", null, [1, 2, 3], { })); // You have passed 4 arguments.
```

The rest operator eliminates the need to check the args array and allows us to apply map(), filter() and reduce() on the parameters array.

### Instructions

Modify the function sum so that is uses the rest operator and it works in the same way with any number of parameters.

## Code

### Original

```javascript
function sum(x, y, z) {
    const array = [ x, y, z ];
    return array.reduce((a, b) => a + b, 0);
}
console.log(sum(1, 2, 3)); // 6
```
### Answer

```javascript
'use strict';
function sum(...elem) {
    return elem.reduce((a, b) => a + b, 0);
}
console.log(sum(1, 2, 3)); // 6
```

## My Notes

For the reduce() method, it's sometimes helpful to rename the `a` and `b` to `previous` and `current` to better understand how the values are returned. Passing `0` as the second argument means that it will be the `previous` value on the first iteration. What this is set to depends on the situation but by using an initial value it can help avoid issues.

### Reference

[MDN - Array.prototype.reduce()](https://developer.mozilla.org/en/docs/Web/JavaScript/Reference/Global_Objects/Array/reduce?v=control)

[Tutsplus - How to use Map, Filter, Reduce in Javascript](https://code.tutsplus.com/tutorials/how-to-use-map-filter-reduce-in-javascript--cms-26209)

[MDN - Rest parameters](https://developer.mozilla.org/en/docs/Web/JavaScript/Reference/Functions/rest_parameters)

[How three dots changed JavaScript](https://rainsoft.io/how-three-dots-changed-javascript/)
