# Basic Algorithm Scripting: Confirm the Ending

### Instructions

Check if a string (first argument, str) ends with the given target string (second argument, target).

This challenge can be solved with the .endsWith() method, which was introduced in ES2015. But for the purpose of this challenge, we would like you to use one of the JavaScript substring methods instead.

Remember to use Read-Search-Ask if you get stuck. Write your own code.

## Code

### Original

```javascript
function confirmEnding(str, target) {
  // "Never give up and good luck will find you."
  // -- Falcor

}

confirmEnding("Bastian", "n");
```

### Solution

```javascript
function confirmEnding(str, target) {
  // "Never give up and good luck will find you."
  // -- Falcor
  
  let reg = new RegExp(target + '$');
  return reg.test(str);
}

confirmEnding("Bastian", "n");
```

## My Notes

Using a regex allowed me to find an exact match at the end of a string with the `$` character. 

The tricky part was figuring out how to pass a variable to the regex. Using the regex constructor, I could build a pattern by concatenating a variable and a regex character. I found [Janet Riley's post](http://janetriley.net/2014/12/javascript-regular-expression-with-a-variable.html) on this helpful.

I then used the test() method to search for a match between the regular expression and the string. It returns true or false so I didn't have to include anything further. 

See [MDN - RegExp.prototype.test()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/RegExp/test) for more info.
