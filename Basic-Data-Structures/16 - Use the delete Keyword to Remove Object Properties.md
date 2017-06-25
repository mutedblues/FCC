# Basic Data Structures: Use the delete Keyword to Remove Object Properties

Now you know what objects are and their basic features and advantages. In short, they are key-value stores which provide a flexible, intuitive way to structure data, and, they provide very fast lookup time. Throughout the rest of these challenges, we will describe several common operations you can perform on objects so you can become comfortable applying these useful data structures in your programs.

In earlier challenges, we have both added to and modified an object's key-value pairs. Here we will see how we can remove a key-value pair from an object.

Let's revisit our foods object example one last time. If we wanted to remove the apples key, we can remove it by using the delete keyword like this:

```javascript
delete foods.apples;
```


### Instructions

Use the delete keyword to remove the oranges, plums, and strawberries keys from the foods object.

## Code

### Original

```javascript
let foods = {
  apples: 25,
  oranges: 32,
  plums: 28,
  bananas: 13,
  grapes: 35,
  strawberries: 27
};

// change code below this line

// change code above this line

console.log(foods);
```

### Solution

```javascript
let foods = {
  apples: 25,
  oranges: 32,
  plums: 28,
  bananas: 13,
  grapes: 35,
  strawberries: 27
};

// change code below this line
delete foods.oranges;
delete foods.plums;
delete foods.strawberries;
// change code above this line

console.log(foods);
```
