# Basic Algorithm Scripting: Return Largest Numbers in Arrays

### Instructions

Return an array consisting of the largest number from each provided sub-array. For simplicity, the provided array will contain exactly 4 sub-arrays.

Remember, you can iterate through an array with a simple for loop, and access each member with array syntax arr[i].

Remember to use Read-Search-Ask if you get stuck. Write your own code.

## Code

### Original

```javascript
function largestOfFour(arr) {
  // You can do this!
  
  return arr;
}

largestOfFour([[4, 5, 1, 3], [13, 27, 18, 26], [32, 35, 37, 39], [1000, 1001, 857, 1]]);
```

### Solution

```javascript
function largestOfFour(arr) {
  // You can do this!
  
  let max = arr.map((elem) => Math.max.apply(null, elem));
  
  return max;
}

largestOfFour([[4, 5, 1, 3], [13, 27, 18, 26], [32, 35, 37, 39], [1000, 1001, 857, 1]]);
```

## My Notes

This was my first successful attempt. I was able to clean it up using map() and arrow functions.

```javascript
function largestOfFour(arr) {
  // You can do this!
  
  let max = [];
  
  for (let i = 0; i < arr.length; i++) {

     let elem = Math.max.apply(null, arr[i]);
     max.push(elem);
     console.log(max);
     }
     
  return max;
}

largestOfFour([[4, 5, 1, 3], [13, 27, 18, 26], [32, 35, 37, 39], [1000, 1001, 857, 1]]);

```
