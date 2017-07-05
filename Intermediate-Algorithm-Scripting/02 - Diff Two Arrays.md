# Intermediate Algorithm Scripting: Diff Two Arrays

### Instructions

Compare two arrays and return a new array with any items only found in one of the two given arrays, but not both. In other words, return the symmetric difference of the two arrays.

Remember to use Read-Search-Ask if you get stuck. Try to pair program. Write your own code.

#### Note

You can return the array with its elements in any order.

## Code

### Original

```javascript
function diffArray(arr1, arr2) {
  var newArr = [];
  // Same, same; but different.
  return newArr;
}

diffArray([1, 2, 3, 5], [1, 2, 3, 4, 5]);
```

### Solution

```javascript
function diffArray(arr1, arr2) {
  
  
  let set1 = new Set(arr1);
  let set2 = new Set(arr2);
  
  let diff1 = arr1.filter(x => !set2.has(x));
//   console.log(diff1);
  
  let diff2 = arr2.filter(x => !set1.has(x));
//   console.log(diff2);

  
  let newArr = diff1.concat(diff2);
  
  console.log(newArr);

  // Same, same; but different.
  return newArr;
}

diffArray([1, 2, 3, 5], [1, 2, 3, 4, 5]);
```
