# Intermediate Algorithm Scripting: Convert HTML Entities

### Instructions

Convert the characters &, <, >, " (double quote), and ' (apostrophe), in a string to their corresponding HTML entities.

Remember to use Read-Search-Ask if you get stuck. Try to pair program. Write your own code.

## Code

### Original

```javascript
function convertHTML(str) {
  // &colon;&rpar;
  return str;
}

convertHTML("Dolce & Gabbana");
```

### Solution

```javascript
function convertHTML(str) {
  // &colon;&rpar;
  
  let pattern = /[&<>/"/']/g;
  
  return str.replace(pattern, function(elem){
    switch(elem) {
      case '&':
        return '&amp;';
      case '<':
        return '&lt;';
      case '>':
        return '&gt;';
      case '\"':
        return '&quot;';
      case "\'":
        return '&apos;';
      default:
        return elem;
    }
  });
  
}

convertHTML("Dolce & Gabbana");
```
