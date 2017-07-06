# Intermediate Algorithm Scripting: Caesars Cipher

### Instructions

One of the simplest and most widely known ciphers is a Caesar cipher, also known as a shift cipher. In a shift cipher the meanings of the letters are shifted by some set amount.

A common modern use is the ROT13 cipher, where the values of the letters are shifted by 13 places. Thus 'A' ↔ 'N', 'B' ↔ 'O' and so on.

Write a function which takes a ROT13 encoded string as input and returns a decoded string.

All letters will be uppercase. Do not transform any non-alphabetic character (i.e. spaces, punctuation), but do pass them on.

Remember to use Read-Search-Ask if you get stuck. Try to pair program. Write your own code.

## Code

### Original

```javascript
function rot13(str) { // LBH QVQ VG!
  
  return str;
}

// Change the inputs below to test
rot13("SERR PBQR PNZC");
```

### Solution

```javascript
function rot13(str) { // LBH QVQ VG!
  
  let codeArr = [];
  
  
  for (let i = 0; i < str.length; i++) {
    codeArr.push(str.charCodeAt(i));
  }  
  
  let decodeArr = codeArr.map(function(code){
    if (code >= 65 && code <= 77) {
      return code + 13;
    } else if (code >= 78 && code <= 90) {
      return code - 13;
    } else if (code < 65) {
      return code;
    }
  });  
  
  return String.fromCharCode(...decodeArr);

}

// Change the inputs below to test
rot13("SERR PBQR PNZC");
```
