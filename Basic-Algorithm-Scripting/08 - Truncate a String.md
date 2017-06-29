# Basic Algorithm Scripting: Truncate a String

### Instructions

Truncate a string (first argument) if it is longer than the given maximum string length (second argument). Return the truncated string with a ... ending.

Remember to use Read-Search-Ask if you get stuck. Write your own code.

## Code

### Original

```javascript
function truncateString(str, num) {
  // Clear out that junk in your trunk
  return str;
}

truncateString("A-tisket a-tasket A green and yellow basket", 8);
```

### Solution

```javascript
function truncateString(str, num) {
  // Clear out that junk in your trunk
  
  if (str.length > num) {
 
    let newStr = (str.substr(0, num) + '...');
    return newStr;
  } else {
    return str;
  }
}

truncateString("A-tisket a-tasket A green and yellow basket", 8);
```
