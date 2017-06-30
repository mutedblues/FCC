# Object Oriented Programming: Remember to Set the Constructor Property when Changing the Prototype

There is one crucial side effect of manually setting the prototype to a new object. It erased the constructor property! The code in the previous challenge would print the following for duck:

```javascript
console.log(duck.constructor)
// prints ‘undefined’ - Oops!
```
To fix this, whenever a prototype is manually set to a new object, remember to define the constructor property:

```javascript
Bird.prototype = {
  constructor: Bird, // define the constructor property
  numLegs: 2,
  eat: function() {
    console.log("nom nom nom");
  },
  describe: function() {
    console.log("My name is " + this.name); 
  }
};
```


### Instructions

Define the constructor property on the Dog prototype.

## Code

### Original

```javascript
function Dog(name) {
  this.name = name; 
}

// Modify the code below this line
Dog.prototype = {
  
  numLegs: 2, 
  eat: function() {
    console.log("nom nom nom"); 
  }, 
  describe: function() {
    console.log("My name is " + this.name); 
  }
};
```

### Solution

```javascript
function Dog(name) {
  this.name = name; 
}

// Modify the code below this line
Dog.prototype = {
  constructor: Dog,
  numLegs: 2, 
  eat: function() {
    console.log("nom nom nom"); 
  }, 
  describe: function() {
    console.log("My name is " + this.name); 
  }
};
```
