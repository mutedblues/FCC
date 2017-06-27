# Basic Algorithm Scripting: Reverse a String

### Instructions

Reverse the provided string.

You may need to turn the string into an array before you can reverse it.

Your result must be a string.

Remember to use Read-Search-Ask if you get stuck. Write your own code.

## Code

### Original

```javascript
function reverseString(str) {
  return str;
}

reverseString("hello");
```

### Solution

```javascript
function reverseString(str) {
  return str.split('').reverse().join('');
}

reverseString("hello");
```

## My Notes

Code broken down step-by-step:

```javascript
function reverseString(str) {
  let arrayOfString = str.split('');
//   console.log(arrayOfString);
  let reverseOfArray = arrayOfString.reverse();
//   console.log(reverseOfArray);
  let reverseOfString = reverseOfArray.join('');
  console.log(reverseOfString);
  str = reverseOfString;
  return str;  
}

reverseString("hello");.
```
