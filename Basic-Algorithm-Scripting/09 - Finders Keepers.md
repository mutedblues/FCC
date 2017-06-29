# Basic Algorithm Scripting: Finders Keepers

### Instructions

Create a function that looks through an array (first argument) and returns the first element in the array that passes a truth test (second argument). If no element passes the test, return undefined.

Remember to use Read-Search-Ask if you get stuck. Try to pair program. Write your own code.

## Code

### Original

```javascript
function findElement(arr, func) {
  var num = 0;
  return num;
}

findElement([1, 2, 3, 4], function(num){ return num % 2 === 0; });
```

### Solution

```javascript
function findElement(arr, func) {
  return arr.find(func);

}

findElement([1, 2, 3, 4], function(num){ return num % 2 === 0; });
```

## My Notes

Finding the right built-in method...

[Array.prototype.map()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/map): Started here since I know it will go over every element of an array. We don't want to return a new array - instead the first number that matches the truth statement so map() doesn't work.

[Array.prototype.filter()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/filter): Looked at filter() next since again I know it looks over all elements of an array. Again, it creates a new array with all elements that pass the test.

[Array.prototype.some()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/some): This method tests whether some element passes the test. It returns true or false but we want the number to return. Getting closer...

[Array.prototype.find()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/find): The find() method returns the value of the first element in the array that satisfies the testing function. Otherwise `undefined` is returned. This is the one!
