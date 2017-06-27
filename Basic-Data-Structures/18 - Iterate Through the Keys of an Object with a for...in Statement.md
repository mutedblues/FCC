# Basic Data Structures: Iterate Through the Keys of an Object with a for...in Statement

Sometimes you may need to iterate through all the keys within an object. This requires a specific syntax in JavaScript called a for...in statement. For our users object, this could look like:

```javascript
for (let user in users) {
  console.log(user);
};

// logs:
Alan
Jeff
Sarah
Ryan
```
In this statement, we defined a variable user, and as you can see, this variable was reset during each iteration to each of the object's keys as the statement looped through the object, resulting in each user's name being printed to the console.

#### NOTE:
Objects do not maintain an ordering to stored keys like arrays do; thus a keys position on an object, or the relative order in which it appears, is irrelevant when referencing or accessing that key.

### Instructions

We've defined a function, countOnline; use a for...in statement within this function to loop through the users in the users object and return the number of users whose online property is set to true.

## Code

### Original

```javascript
let users = {
  Alan: {
    age: 27,
    online: false
  },
  Jeff: {
    age: 32,
    online: true
  },
  Sarah: {
    age: 48,
    online: false
  },
  Ryan: {
    age: 19,
    online: true
  }
};

function countOnline(obj) {
  // change code below this line

  // change code above this line
}

console.log(countOnline(users));
```

### Solution

```javascript
let users = {
  Alan: {
    age: 27,
    online: false
  },
  Jeff: {
    age: 32,
    online: true
  },
  Sarah: {
    age: 48,
    online: false
  },
  Ryan: {
    age: 19,
    online: true
  }
};

function countOnline(obj) {
  // change code below this line
  let n = 0;
  for (let user in obj) if (obj[user].online) n++;
    return n;
  // change code above this line
}

console.log(countOnline(users));
```

## My Notes

Let's break this down...

`let n = 0 `: We declare `n` and set it to 0 because we need to be able to track how many users are online - we're adding to our number with each loop

`for (let user in obj)`: Allows us to iterate through all keys within the object. We've created a new variable `user` as a generic reference for the individual users in the `users` object. Could have named `user` anything really, but `user` makes sense here. `obj` is the variable name that here relates to the `users` object but with our code we could run the function on a different object - we'd simply pass that object name in the console.log above.

`if (obj[user].online) n++`: If the `user` in the `users` object is online (equals `true`), then add 1 to `n`. We can't use dot notation for `user` since it is a variable not a string. We could change this to `obj[user]["online"]` but dot notation is more succinct for accessing the `online` property.

