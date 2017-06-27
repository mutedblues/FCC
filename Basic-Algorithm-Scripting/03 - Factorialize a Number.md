# Basic Algorithm Scripting: Factorialize a Number

### Instructions

Return the factorial of the provided integer.

If the integer is represented with the letter n, a factorial is the product of all positive integers less than or equal to n.

Factorials are often represented with the shorthand notation n!

For example: 5! = 1 * 2 * 3 * 4 * 5 = 120

Only integers greater than or equal to zero will be supplied to the function.

Remember to use Read-Search-Ask if you get stuck. Write your own code.

## Code

### Original

```javascript
function factorialize(num) {
  return num;
}

factorialize(5);
```

### Solution

```javascript
function factorialize(num) {
  let prevNum = 0;
  let newNum = 1;
  while (prevNum < num) {
    prevNum++;
    console.log('this is the prevNum' + prevNum);
    newNum *= prevNum;
    console.log('this is the newNum' + newNum);
  }
  return newNum;
}

factorialize(5);
```

## My Notes

This [medium article](https://medium.freecodecamp.org/how-to-factorialize-a-number-in-javascript-9263c89a4b38) breaks down 3 well-commented ways to solve this problem.
Quite different from my own solution.
