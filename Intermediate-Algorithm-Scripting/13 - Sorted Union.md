# Intermediate Algorithm Scripting: Sorted Union

### Instructions

Write a function that takes two or more arrays and returns a new array of unique values in the order of the original provided arrays.

In other words, all values present from all arrays should be included in their original order, but with no duplicates in the final array.

The unique numbers should be sorted by their original order, but the final array should not be sorted in numerical order.

Check the assertion tests for examples.

Remember to use Read-Search-Ask if you get stuck. Try to pair program. Write your own code.

## Code

### Original

```javascript
function uniteUnique(arr) {
  return arr;
}

uniteUnique([1, 3, 2], [5, 2, 1, 4], [2, 1]);
```

### Solution

Using Set object to store only unique valuse and remove duplicates

```javascript
function uniteUnique(arr) {
  let merged = [].concat(...arguments);
  return [...new Set(merged)];

}

uniteUnique([1, 3, 2], [5, 2, 1, 4], [2, 1]);
```

Using filter() to iterate through the merged array and indexOf of each element to find unique values.

```javascript
function uniteUnique(arr) {
  let merged = [].concat(...arguments);
  
  let unique = merged.filter((elem, index, arr) => arr.indexOf(elem) === index);
  return unique;
}

uniteUnique([1, 3, 2], [5, 2, 1, 4], [2, 1]);
```

## My Notes

Helpful links:

* http://mikeheavers.com/tutorials/removing_duplicates_in_an_array_using_javascript/
* https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/arguments
