# ES6: Use getters and setters to Control Access to an Object

You can obtain values from an object, and set a value of a property within an object.

These are classically called getters and setters.

Getter functions are meant to simply return (get) the value of an object's private variable to the user without the user directly accessing the private variable.

Setter functions are meant to modify (set) the value of an object's private variable based on the value passed into the setter function. This change could involve calculations, or even overwriting the previous value completely.

```javascript
class Book {
  constructor(author) {
    this._author = author;
  }
  // getter
  get writer(){
    return this._author;
  }
  // setter
  set writer(updatedAuthor){
    this._author = updatedAuthor;
  }
}
const lol = new Book('anonymous');
console.log(lol.writer);
lol.writer = 'wut';
console.log(lol.writer);
```
Notice the syntax we are using to invoke the getter and setter - as if they are not even functions.

Getters and setters are important, because they hide internal implementation details.

### Instructions

Use class keyword to create a Thermostat class. The constructor accepts Farenheit temperature.

Now create getter and setter in the class, to obtain the temperature in Celsius scale.

Remember that F = C * 9.0 / 5 + 32, where F is the value of temperature in Fahrenheit scale, and C is the value of the same temperature in Celsius scale

#### Note

When you implement this, you would be tracking the temperature inside the class in one scale - either Fahrenheit or Celsius.

This is the power of getter or setter - you are creating an API for another user, who would get the correct result, no matter which one you track.

In other words, you are abstracting implementation details from the consumer.

## Code

### Original

```javascript
/* Alter code below this line */
const Thermostat = undefined;
/* Alter code above this line */
const thermos = new Thermostat(76); // setting in Farenheit scale
let temp = thermos.temperature; // 24.44 in C
thermos.temperature = 26;
temp = thermos.temperature; // 26 in C
```
### Solution

```javascript
/* Alter code below this line */
class Thermostat {
  constructor(temp) {
    this._temp = temp;
  }
  // getter
    get temperature(){
      return this._temp;
    }
    // setter
    set temperature(updatedTemp){
      this._temp = (updatedTemp * 9.0 / 5 + 32);
    }
}
/* Alter code above this line */
const thermos = new Thermostat(76); // setting in Farenheit scale
let temp = thermos.temperature; // 24.44 in C
thermos.temperature = 26;
temp = thermos.temperature; // 26 in C
console.log(thermos.temperature); // So I can confirm it works
```

## My Notes

Found myself going down a rabbit hole of getters and setters. Some helpful articles I will return to:

1. [Getters, Setters, and Organizing Responsibility in JavaScript](http://raganwald.com/2015/08/24/ready-get-set-go.html)
2. [JavaScript Getters and Setters](http://javascriptplayground.com/blog/2013/12/es5-getters-setters/)
3. [Some Javascript constructor patterns, and when to use them](http://www.samselikoff.com/blog/some-Javascript-constructor-patterns/)



