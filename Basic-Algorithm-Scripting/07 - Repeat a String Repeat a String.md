# Basic Algorithm Scripting: Repeat a String Repeat a String

### Instructions

Repeat a given string str (first argument) for num times (second argument). Return an empty string if num is not a positive number.

Remember to use Read-Search-Ask if you get stuck. Write your own code.

## Code

### Original

```javascript
function repeatStringNumTimes(str, num) {
  // repeat after me
  return str;
}

repeatStringNumTimes("abc", 3);
```

### Solution

```javascript
function repeatStringNumTimes(str, num) {
  // repeat after me
  let newStr = '';
  
  // with a 'for' loop
  //   for (i = 0; i < num; i++) {
  //     newStr += str;
  //   }
  
  // with a 'while' loop
  while (num > 0) {
    newStr += str;
    num--;
  }
  return newStr;
}

repeatStringNumTimes("abc", 3);
```
