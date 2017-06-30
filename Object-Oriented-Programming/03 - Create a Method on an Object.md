# Object Oriented Programming: Create a Method on an Object

Objects can have a special type of property, called a method.

Methods are properties that are functions. This adds different behavior to an object. Here is the duck example with a method:

```javascript
let duck = {
  name: "Aflac",
  numLegs: 2,
  sayName: function() {return "The name of this duck is " + duck.name + ".";}
};
duck.sayName();
// Returns "The name of this duck is Aflac."
```
The example adds the sayName method, which is a function that returns a sentence giving the name of the duck.

Notice that the method accessed the name property in the return statement using duck.name. The next challenge will cover another way to do this.

### Instructions

Using the dog object, give it a method called sayLegs. The method should return the sentence "This dog has 4 legs."

## Code

### Original

```javascript
let dog = {
  name: "Spot",
  numLegs: 4,
  
};

dog.sayLegs();
```

### Solution

```javascript
let dog = {
  name: "Spot",
  numLegs: 4,
  sayLegs: function() {return "This dog has " + dog.numLegs + " legs.";}
};

dog.sayLegs();
```
