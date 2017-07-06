# Intermediate Algorithm Scripting: Roman Numeral Converter

### Instructions

Convert the given number into a roman numeral.

All roman numerals answers should be provided in upper-case.

Remember to use Read-Search-Ask if you get stuck. Try to pair program. Write your own code.

## Code

### Original

```javascript
function convertToRoman(num) {
 return num;
}

convertToRoman(36);
```

### Solution

```javascript
function convertToRoman(num) {
  
  let result = '';
  
  let romanNums = {
    M: 1000,
    CM: 900,
    D: 500,
    CD: 400,
    C: 100,
    XC: 90,
    L: 50,
    XL: 40,
    X: 10, 
    IX: 9,
    V: 5,
    IV: 4,
    I: 1
  };
  
  for (let val in romanNums) {
    for (let i = romanNums[val]; num >= i; num -= i) result += val;
  }
  console.log(result);
  
  return result;
  
}

convertToRoman(36);
```
