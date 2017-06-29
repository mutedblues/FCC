# Basic Algorithm Scripting: Boo who

### Instructions

Check if a value is classified as a boolean primitive. Return true or false.

Boolean primitives are true and false.

Remember to use Read-Search-Ask if you get stuck. Try to pair program. Write your own code.

## Code

### Original

```javascript
function booWho(bool) {
  // What is the new fad diet for ghost developers? The Boolean.
  return bool;
}

booWho(null);
```

### Solution

```javascript
function booWho(bool) {
  // What is the new fad diet for ghost developers? The Boolean.
  return typeof bool === 'boolean';
}

booWho(null);
```

## My Notes

From [MDN](https://developer.mozilla.org/en/docs/Web/JavaScript/Reference/Operators/typeof):

> The typeof operator returns a string indicating the type of the unevaluated operand.

So, if we have `typeof true` it will return `'boolean'` (remember, it returns the type in string format).

Testing for `typeof var === 'boolean'` will return `true` if `var` equals `true` or `false` and will return `false` if `var` equals anything else.

The `typeof` operator has some quirks (like returning 'number' for NaN and 'object' for Null). This discussion (https://javascriptweblog.wordpress.com/2011/08/08/fixing-the-javascript-typeof-operator/) is a bit beyond my current comfort level but will surely be handy in the future.
