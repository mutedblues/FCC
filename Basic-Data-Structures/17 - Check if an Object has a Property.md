# Basic Data Structures: Check if an Object has a Property

Now we can add, modify, and remove keys from objects. But what if we just wanted to know if an object has a specific property? JavaScript provides us with two different ways to do this. One uses the hasOwnProperty() method and the other uses the in keyword. If we have an object users with a property of Alan, we could check for its presence in either of the following ways:

```javascript
users.hasOwnProperty('Alan');
'Alan' in users;
// both return true
```


### Instructions

We've created an object, users, with some users in it and a function isEveryoneHere, which we pass the users object to as an argument. Finish writing this function so that it returns true only if the users object contains all four names, Alan, Jeff, Sarah, and Ryan, as keys, and false otherwise.

## Code

### Original

```javascript
let users = {
  Alan: {
    age: 27,
    online: true
  },
  Jeff: {
    age: 32,
    online: true
  },
  Sarah: {
    age: 48,
    online: true
  },
  Ryan: {
    age: 19,
    online: true
  }
};

function isEveryoneHere(obj) {
  // change code below this line

  // change code above this line
}

console.log(isEveryoneHere(users));
```

### Solution

Using hasOwnProperty():

```javascript
function isEveryoneHere(obj) {
  // change code below this line
  if (obj.hasOwnProperty('Alan') && obj.hasOwnProperty('Jeff') && obj.hasOwnProperty('Sarah') && obj.hasOwnProperty('Ryan')){
    return true;
  } else {
    return false;
  }
  // change code above this line
}

console.log(isEveryoneHere(users));
```
And using `prop in objectName`:

```javascript
function isEveryoneHere(obj) {
  // change code below this line
  if ('Alan' in users && 'Jeff' in users && 'Sarah' in users && 'Ryan' in users) {
    return true;
  } else {
    return false;
  }
  // change code above this line
}
```
Or we could use the ternary operator:

```javascript
function isEveryoneHere(obj) {
  // change code below this line
  return ('Alan' in users && 'Jeff' in users && 'Sarah' in users && 'Ryan' in users) ? true : false;
  // change code above this line
}

console.log(isEveryoneHere(users));
```
The below passes the FCC test but ~~I'm not 100% on the code~~ it's wrong.

```javascript

let users = {
  Alan: {
    age: 27,
    online: true
  },
  Jeff: {
    age: 32,
    online: true
  },
  Sarah: {
    age: 48,
    online: true
  },
  Ryan: {
    age: 19,
    online: true
  }
};

function isEveryoneHere(obj) {
  // change code below this line
  if (obj.hasOwnProperty('Alan', 'Jeff', 'Sarah', 'Ryan')) {
    return true;
  } else {
    return false;
  }
  // change code above this line
}

console.log(isEveryoneHere(users));
```
I could add a bunch of properties, like `('Alan', 'Jeff', 'Sarah', 'Ryan', 'Otto', 'Oliver', 'Max')` and it would still return true. Why? Because it's only testing for the first property, `Alan`. 

## My Notes

From [Methods to determine if an Object has a given property](https://toddmotto.com/methods-to-determine-if-an-object-has-a-given-property/):
> The `in` operator is probably your best friend for checking the existence of a property, it’s also pretty concise.

Need to work on using the ternary operator.

From [MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Conditional_Operator)

> The conditional (ternary) operator is the only JavaScript operator that takes three operands. This operator is frequently used as a shortcut for the if statement.

Syntax
```
condition ? expr1 : expr2 
```
> If condition is true, the operator returns the value of expr1; otherwise, it returns the value of expr2.
