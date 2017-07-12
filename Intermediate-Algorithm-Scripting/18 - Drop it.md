# Intermediate Algorithm Scripting: Drop it

### Instructions

Given the array arr, iterate through and remove each element starting from the first element (the 0 index) until the function func returns true when the iterated element is passed through it.

Then return the rest of the array once the condition is satisfied, otherwise, arr should be returned as an empty array.

Remember to use Read-Search-Ask if you get stuck. Try to pair program. Write your own code.

## Code

### Original

```javascript
function dropElements(arr, func) {
  // Drop them elements.
  return arr;
}

dropElements([1, 2, 3], function(n) {return n < 3; });
```

### Solution

```javascript
function dropElements(arr, func) {
  // Drop them elements.
  
  let index = arr.findIndex(func);
  
  return index === -1 ? [] : arr.slice(index);
}

dropElements([1, 2, 3], function(n) {return n < 3; });
```

## My Notes

[Array.prototype.find()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/find) was already a lifesaver - its cousin [Array.prototype.findIndex()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/findIndex) did the trick in this instance.

Extra Credit: [Drop It Like It's Hot](https://www.youtube.com/watch?v=GtUVQei3nX4)
