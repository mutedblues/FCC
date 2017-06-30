# Object Oriented Programming: Use a Constructor to Create Objects

Here's the Bird constructor from the previous challenge:

```javascript
function Bird() {
  this.name = "Albert";
  this.color  = "blue";
  this.numLegs = 2;
  // "this" inside the constructor always refers to the object being created
}

let blueBird = new Bird();
```
Notice that the new operator is used when calling a constructor. This tells JavaScript to create a new instance of Bird called blueBird. Without the new operator, this inside the constructor would not point to the newly created object, giving unexpected results.

Now blueBird has all the properties defined inside the Bird constructor:

```javascript
blueBird.name; // => Albert
blueBird.color; // => blue
blueBird.numLegs; // => 2
```
Just like any other object, its properties can be accessed and modified:

```javascript
blueBird.name = 'Elvira';
blueBird.name; // => Elvira
```

### Instructions

Use the Dog constructor from the last lesson to create a new instance of Dog, assigning it to a variable hound.

## Code

### Original

```javascript
function Dog() {
  this.name = "Rupert";
  this.color = "brown";
  this.numLegs = 4;
}
// Add your code below this line
```

### Solution

```javascript
function Dog() {
  this.name = "Rupert";
  this.color = "brown";
  this.numLegs = 4;
}
// Add your code below this line

let hound = new Dog();
```
