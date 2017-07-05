# Functional Programming: Combine an Array into a String Using the join Method

The join method is used to join the elements of an array together to create a string. It takes an argument for the delimiter that is used to separate the array elements in the string.

Here's an example:

```javascript
var arr = ["Hello", "World"];
var str = arr.join(" ");
// Sets str to "Hello World"
```

### Instructions

Use the join method (among others) inside the sentensify function to make a sentence from the words in the string str. The function should return a string. For example, "I-like-Star-Wars" would be converted to "I like Star Wars". For this challenge, do not use the replace method.

## Code

### Original

```javascript
function sentensify(str) {
  // Add your code below this line
  
  
  // Add your code above this line
}
sentensify("May-the-force-be-with-you");
```

### Solution

```javascript
function sentensify(str) {
  // Add your code below this line
  return str.split(/\W/).join(" ");
  // Add your code above this line
}
sentensify("May-the-force-be-with-you");
```
