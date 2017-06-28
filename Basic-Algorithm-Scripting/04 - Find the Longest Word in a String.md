# Basic Algorithm Scripting: Find the Longest Word in a String

### Instructions

Return the length of the longest word in the provided sentence.

Your response should be a number.

Remember to use Read-Search-Ask if you get stuck. Write your own code.

## Code

### Original

```javascript
function findLongestWord(str) {
  return str.length;
}

findLongestWord("The quick brown fox jumped over the lazy dog");
```

### Solution

```javascript
function findLongestWord(str) {
  
  // convert string to array and find length of each array item
  let arr = str.split(' ').map(word => word.length);
  console.log(arr);
  //iterate over array to find longest word
  let max = Math.max(...arr);
  console.log(max);
  return max;
  
}

findLongestWord("The quick brown fox jumped over the lazy dog");
```
