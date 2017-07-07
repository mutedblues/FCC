# Intermediate Algorithm Scripting: DNA Pairing

### Instructions

The DNA strand is missing the pairing element. Take each character, get its pair, and return the results as a 2d array.

Base pairs are a pair of AT and CG. Match the missing element to the provided character.

Return the provided character as the first element in each array.

For example, for the input GCG, return [["G", "C"], ["C","G"],["G", "C"]]

The character and its pair are paired up in an array, and all the arrays are grouped into one encapsulating array.

Remember to use Read-Search-Ask if you get stuck. Try to pair program. Write your own code.

## Code

### Original

```javascript
function pairElement(str) {
  return str;
}

pairElement("GCG");
```

### Solution

```javascript
function pairElement(str) {
  let arr = str.split('');
  let pairs = [];
  
  let search = function(char){
      switch (char) {
        case 'A':
          pairs.push(['A', 'T']);
          break;
        case 'T':
          pairs.push(['T', 'A']);
          break;
        case 'G':
          pairs.push(['G', 'C']);
          break;
        case 'C':
          pairs.push(['C', 'G']);
          break;
    }
  };
  
  arr.forEach(function(char){
    search(char);
  });
  
  return pairs;
}

pairElement("GCG");
```
