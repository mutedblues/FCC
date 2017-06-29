# Basic Algorithm Scripting: Falsy Bouncer

### Instructions

Remove all falsy values from an array.

Falsy values in JavaScript are false, null, 0, "", undefined, and NaN.

Hint: Try converting each value to a Boolean.

Remember to use Read-Search-Ask if you get stuck. Write your own code.

## Code

### Original

```javascript
function bouncer(arr) {
  // Don't show a false ID to this bouncer.
  return arr;
}

bouncer([7, "ate", "", false, 9]);
```

### Solution

```javascript
function bouncer(arr) {
  // Don't show a false ID to this bouncer.
  let newArr = arr.filter(function(elem){
    return Boolean(elem);
  });
  
  return newArr;
}

bouncer([7, "ate", "", false, 9]);
```

##My Notes

From [MDN - Boolean](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean):

> The value passed as the first parameter is converted to a boolean value, if necessary. If the value is omitted or is 0, -0, null, false, NaN, undefined, or the empty string (""), the object has an initial value of false.
