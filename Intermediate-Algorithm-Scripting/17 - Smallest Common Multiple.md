# Intermediate Algorithm Scripting: Smallest Common Multiple

### Instructions

Find the smallest common multiple of the provided parameters that can be evenly divided by both, as well as by all sequential numbers in the range between these parameters.

The range will be an array of two numbers that will not necessarily be in numerical order.

For example, if given 1 and 3, find the smallest common multiple of both 1 and 3 that is also evenly divisible by all numbers between 1 and 3. The answer here would be 6.

Remember to use Read-Search-Ask if you get stuck. Try to pair program. Write your own code.

## Code

### Original

```javascript
function smallestCommons(arr) {
  return arr;
}
smallestCommons([1,5]);
```

### Solution

```javascript
//LCM = (a * b) / GCD(a, b) **OR** LCM = a / GCD (a,b) * b

function gcd(a, b) {
  if (b === 0) {
    return a;
  } else if (a >= b && b > 0) {
    return gcd(b, a % b);
  } else {
    return gcd(b, a);
  }
}

function lcm(a, b){
  return a / gcd(a, b) * b;
}


function smallestCommons(arr) {
  let min = Math.min(...arr);
  let max = Math.max(...arr);
  
  let range = [];
  for (let i = max; i >= min; i--) {
    range.push(i);
  }
  
  return range.reduce(function (prev, curr){
    return lcm(curr, prev);
  });
}


smallestCommons([1,5]);
```

## My Notes

The formula that the Mod mentioned in the comments at https://teamtreehouse.com/community/javascript-find-least-common-multiple made it possible to work through the math.
