# 

### Instructions

Flatten a nested array. You must account for varying levels of nesting.

Remember to use Read-Search-Ask if you get stuck. Try to pair program. Write your own code.

## Code

### Original

```javascript
function steamrollArray(arr) {
  // I'm a steamroller, baby
  return arr;
}

steamrollArray([1, [2], [3, [[4]]]]);
```

### Solution

```javascript
function flatten(arr) {
  return [].concat(...arr);
}

function steamrollArray(arr) {
  // I'm a steamroller, baby

  return flatten (arr.map(function(elem) {
    return Array.isArray(elem) ? steamrollArray(elem) : elem;
    }));
}

steamrollArray([1, [2], [3, [[4]]]]);
```

## My Notes

`[].concat(...arr);` is the same as `[].concat.apply([], arr);` but the spread operator cleans things up.

An in-depth discussion of `concat()` - touching on `this` and `apply()`: https://www.reddit.com/r/learnjavascript/comments/29a3so/why_does_using_apply_with_concat_flatten_arrays/
