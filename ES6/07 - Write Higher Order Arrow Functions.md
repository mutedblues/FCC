# ES6: Write Higher Order Arrow Functions

It's time we see how powerful arrow functions are when processing data.

Arrow functions work really well with higher order functions, such as map(), filter(), and reduce(), that take other functions as arguments for processing collections of data.

Read the following code:

```javascript
FBPosts.filter(function(post) {
  return post.thumbnail !== null && post.shares > 100 && post.likes > 500;
})
```
We have written this with filter() to at least make it somewhat readable. Now compare it to the following code which uses arrow function syntax instead:

```javascript
FBPosts.filter((post) => post.thumbnail !== null && post.shares > 100 && post.likes > 500)
```
This code is more succinct and accomplishes the same task with fewer lines of code.

### Instructions

Use arrow function syntax to compute the square of only the positive integers (fractions are not integers) in the array realNumberArray and store the new array in the variable squaredIntegers.

## Code

### Original

```javascript
const realNumberArray = [4, 5.6, -9.8, 3.14, 42, 6, 8.34];
// change code below this line
var squaredIntegers = realNumberArray;
// change code above this line
// test your code
console.log(squaredIntegers);
```

### Answer

```javascript
'use strict';
const realNumberArray = [4, 5.6, -9.8, 3.14, 42, 6, 8.34];
// change code below this line

const squaredIntegers = realNumberArray.filter((number) => number % 1 === 0
).map((elem) => elem * elem);
// change code above this line
// test your code
console.log(squaredIntegers);
```

## My Notes

Needed to filter the realNumberArray first to find only positive integers. What's cool is that with this syntax I could use dot notation to add the map method(). 

Remember, 'number' and 'elem' are just random names for the arguments - I could name them anything. Important thing is that the args tell the methods what to look for while looping through the array.

`number % 1 === 0` makes sure that the array number is a positive integer by using the remainder operator.

### Reference

[MDN - Array.prototype.filter()](https://developer.mozilla.org/en/docs/Web/JavaScript/Reference/Global_Objects/Array/filter?v=control)

[MDN - Array.prototype.map()](https://developer.mozilla.org/en/docs/Web/JavaScript/Reference/Global_Objects/Array/map?v=control)
