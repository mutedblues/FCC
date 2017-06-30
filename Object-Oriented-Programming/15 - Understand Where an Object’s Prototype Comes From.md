# Object Oriented Programming: Understand Where an Object’s Prototype Comes From

Just like people inherit genes from their parents, an object inherits its prototype directly from the constructor function that created it. For example, here the Bird constructor creates the duck object:

```javascript
function Bird(name) {
  this.name = name;
}

let duck = new Bird("Donald");
```
duck inherits its prototype from the Bird constructor function. You can show this relationship with the isPrototypeOf method:

```javascript
Bird.prototype.isPrototypeOf(duck);
// returns true
```

### Instructions

Use isPrototypeOf to check the prototype of beagle.

## Code

### Original

```javascript
function Dog(name) {
  this.name = name;
}

let beagle = new Dog("Snoopy");

// Add your code below this line
```

### Solution

```javascript
function Dog(name) {
  this.name = name;
}

let beagle = new Dog("Snoopy");

// Add your code below this line

Dog.prototype.isPrototypeOf(beagle);
```
