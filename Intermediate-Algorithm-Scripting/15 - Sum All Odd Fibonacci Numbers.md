# Intermediate Algorithm Scripting: Sum All Odd Fibonacci Numbers

### Instructions

Given a positive integer num, return the sum of all odd Fibonacci numbers that are less than or equal to num.

The first two numbers in the Fibonacci sequence are 1 and 1. Every additional number in the sequence is the sum of the two previous numbers. The first six numbers of the Fibonacci sequence are 1, 1, 2, 3, 5 and 8.

For example, sumFibs(10) should return 10 because all odd Fibonacci numbers less than or equal to 10 are 1, 1, 3, and 5.

Remember to use Read-Search-Ask if you get stuck. Try to pair program. Write your own code.

## Code

### Original

```javascript
function sumFibs(num) {
  return num;
}

sumFibs(4);
```

### Solution

```javascript
function sumFibs(num) {
  
  let prev = 0, current = 1, result = 0;
  
  while (current <= num) {
    if (current % 2 !== 0) {
      result += current;
    }
      current += prev;
      prev = current - prev;
  }
  return result;
}

sumFibs(4);
```
