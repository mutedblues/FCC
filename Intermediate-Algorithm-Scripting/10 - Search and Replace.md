# Intermediate Algorithm Scripting: Search and Replace

### Instructions

Perform a search and replace on the sentence using the arguments provided and return the new sentence.

First argument is the sentence to perform the search and replace on.

Second argument is the word that you will be replacing (before).

Third argument is what you will be replacing the second argument with (after).

#### Note

Preserve the case of the first character in the original word when you are replacing it. For example if you mean to replace the word "Book" with the word "dog", it should be replaced as "Dog"

Remember to use Read-Search-Ask if you get stuck. Try to pair program. Write your own code.

## Code

### Original

```javascript
function myReplace(str, before, after) {
  return str;
}

myReplace("A quick brown fox jumped over the lazy dog", "jumped", "leaped");
```

### Solution

```javascript
function myReplace(str, before, after) {
  let firstChar;
  let reCase = new RegExp(/[A-Z]/);
  let upperIndex = before.search(reCase);
  
  // check for uppercase character
  if (upperIndex !== -1) {
    
    let upperAfter = after.substring(0, 1).toUpperCase() + after.substring(1);
    
    return str.replace(before, upperAfter);
    
  } else {
  
    return str.replace(before, after);
  }
}


myReplace("A quick brown fox jumped over the lazy dog", "jumped", "leaped");

```
