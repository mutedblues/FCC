# Intermediate Algorithm Scripting: Missing letters

### Instructions

Find the missing letter in the passed letter range and return it.

If all letters are present in the range, return undefined.

Remember to use Read-Search-Ask if you get stuck. Try to pair program. Write your own code.

## Code

### Original

```javascript
function fearNotLetter(str) {
  return str;
}

fearNotLetter("abce");
```

### Solution

```javascript
function fearNotLetter(str) {
  
  let codeArr = [];
  let missingNum;
  
// create an array containing the unicode chars
  for (let i = 0; i < str.length; i++) {
    codeArr.push(str.charCodeAt(i));
  }
  
// loop through the array of numbers
  for (let i = 1; i < codeArr.length; i++){
    
// find the missing consecutive number in the array
    if (codeArr[i] - codeArr[i-1] !== 1) {
      missingNum = codeArr[i] - 1;
// convert missing number back to character and return it
      return String.fromCharCode(missingNum);
    } 
  }
}

fearNotLetter("abce");
```
