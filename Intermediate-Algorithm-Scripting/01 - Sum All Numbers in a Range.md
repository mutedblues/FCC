# Intermediate Algorithm Scripting: Sum All Numbers in a Range

### Instructions

We'll pass you an array of two numbers. Return the sum of those two numbers plus the sum of all the numbers between them.

The lowest number will not always come first.

Remember to use Read-Search-Ask if you get stuck. Try to pair program. Write your own code.

## Code

### Original

```javascript
function sumAll(arr) {
  return 1;
}

sumAll([1, 4]);
```

### Solution

```javascript
function sumAll(arr) {
  let start = Math.min.apply(null, arr);
  let end = Math.max.apply(null, arr);
  
  let val = start;
  for (let i = start + 1; i <= end; i++){
    val += i;
  }
  return val;
}

sumAll([1, 4]);
```
