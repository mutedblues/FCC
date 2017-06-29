# Basic Algorithm Scripting: Title Case a Sentence

### Instructions

Return the provided string with the first letter of each word capitalized. Make sure the rest of the word is in lower case.

For the purpose of this exercise, you should also capitalize connecting words like "the" and "of".

Remember to use Read-Search-Ask if you get stuck. Write your own code.

## Code

### Original

```javascript
function titleCase(str) {
  return str;
}

titleCase("I'm a little tea pot");
```

### Solution

```javascript
function titleCase(str) {
//   return str;
  let capArr = [];
  let newStr = '';
  let lowerCaseArr = str.toLowerCase().split(' ');
  
  for (let i = 0; i < lowerCaseArr.length; i++){
        
    capArr[i] = lowerCaseArr[i].charAt(0).toUpperCase() + lowerCaseArr[i].slice(1).toLowerCase();
  }
  
  return newStr = capArr.join(' ');
  
}

titleCase("I'm a little tea pot");
```
