# Functional Programming: Introduction to Currying and Partial Application

The arity of a function is the number of arguments it requires. Currying a function means to convert a function of N arity into N functions of arity 1.

In other words, it restructures a function so it takes one argument, then returns another function that takes the next argument, and so on.

Here's an example:

```javascript
//Un-curried function
function unCurried(x, y, z) {
  return x + y + z;
}

//Curried function
function curried(x) {
  return function(y) {
    return x + y;
  }
}
curried(1)(2) // Returns 3
```
This is useful in your program if you can't supply all the arguments to a function at one time. You can save each function call into a variable, which will hold the returned function reference that takes the next argument when it's available. Here's an example using the curried function in the example above:

```javascript
// Call a curried function in parts:
var funcForY = curried(1);
var funcForZ = funcForY(2);
console.log(funcForZ(3)); // Prints 6
```
Similarly, partial application can be described as applying a few arguments to a function at a time and returning another function that is applied to more arguments.

Here's an example:

```javascript
//Impartial function
function impartial(x, y, z) {
  return x + y + z;
}
var partialFn = impartial.bind(this, 1, 2);
partialFn(10); // Returns 13
```

### Instructions

Fill in the body of the add function so it uses currying to add parameters x, y, and z.

## Code

### Original

```javascript
function add(x) {
  // Add your code below this line
  
  
  // Add your code above this line
}
add(10)(20)(30);
```

### Solution

```javascript
function add(x) {
  // Add your code below this line
  return function(y) {
    return function (z) {
      return x + y + z;
    };
  };
  
  // Add your code above this line
}
add(10)(20)(30);
```

## My Notes

Further reading: https://www.sitepoint.com/currying-in-functional-javascript/
