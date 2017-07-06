# Intermediate Algorithm Scripting: Spinal Tap Case

### Instructions

Convert a string to spinal case. Spinal case is all-lowercase-words-joined-by-dashes.

Remember to use Read-Search-Ask if you get stuck. Try to pair program. Write your own code.

## Code

### Original

```javascript
function spinalCase(str) {
  // "It's such a fine line between stupid, and clever."
  // --David St. Hubbins
  return str;
}

spinalCase('This Is Spinal Tap');
```

### Solution

```javascript
function spinalCase(str) {
  // "It's such a fine line between stupid, and clever."
  // --David St. Hubbins
  return str.split(/(?=[A-Z])|[\W_]|\s/).join('-').toLowerCase();
  
}

spinalCase('This Is Spinal Tap');
```
