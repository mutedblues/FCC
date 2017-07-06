# Intermediate Algorithm Scripting: Seek and Destroy

### Instructions

You will be provided with an initial array (the first argument in the destroyer function), followed by one or more arguments. Remove all elements from the initial array that are of the same value as these arguments.

#### Note
You have to use the arguments object.

Remember to use Read-Search-Ask if you get stuck. Write your own code.

## Code

### Original

```javascript
function destroyer(arr) {
  // Remove all the values
  return arr;
}

destroyer([1, 2, 3, 1, 2, 3], 2, 3);
```

### Solution

```javascript
function destroyer(arr) {
  // Remove all the values

  let fnArgs = Array.from(arguments);
  let baseArr = fnArgs[0];
  
  let argsArr = fnArgs.slice(1);
  
  return baseArr.filter(elem => argsArr.indexOf(elem) < 0);
  
}


destroyer([1, 2, 3, 1, 2, 3], 2, 3);
```
