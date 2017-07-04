# Functional Programming: Implement map on a Prototype

As you have seen from applying Array.prototype.map(), or simply map() earlier, the map method returns an array of the same length as the one it was called on. It also doesn't alter the original array, as long as its callback function doesn't.

In other words, map is a pure function, and its output depends solely on its inputs. Plus, it takes another function as its argument.

It would teach us a lot about map to try to implement a version of it that behaves exactly like the Array.prototype.map() with a for loop or Array.prototype.forEach().

Note: A pure function is allowed to alter local variables defined within its scope, although, it's preferable to avoid that as well.

### Instructions

Write your own Array.prototype.myMap(), which should behave exactly like Array.prototype.map(). You may use a for loop or the forEach method.

## Code

### Original

```javascript
// the global Array
var s = [23, 65, 98, 5];

Array.prototype.myMap = function(callback){
  var newArray = [];
  // Add your code below this line
  
  // Add your code above this line
  return newArray;

};

var new_s = s.myMap(function(item){
  return item * 2;
});
```

### Solution

```javascript
// the global Array
var s = [23, 65, 98, 5];

Array.prototype.myMap = function(callback){
  var newArray = [];
  // Add your code below this line
  this.forEach(function(elem) {
    newArray.push(callback(elem));
  });
  // Add your code above this line
  return newArray;

};

var new_s = s.myMap(function(item){
  return item * 2;
});

console.log(new_s);
```

## My Notes

Was trying to use `newArray.forEach` but nope...then I'm just looping through the `newArray` which is empty. `this.forEach()` refers to the the original array.

Using a `for` loop: 

```javascript
// the global Array
var s = [23, 65, 98, 5];

Array.prototype.myMap = function(callback){
  var newArray = [];
  // Add your code below this line
  for (let i = 0; i < this.length; i++){
    newArray.push(callback(this[i]));
  }
  // Add your code above this line
  return newArray;

};

var new_s = s.myMap(function(item){
  return item * 2;
});

console.log(new_s);
```


