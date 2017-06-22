# ES6: Use Destructuring Assignment to Assign Variables from Nested Objects

We can similarly destructure nested objects into variables.

Consider the following code:

```javascript
const a = {
  start: { x: 5, y: 6},
  end: { x: 6, y: -9 }
};
const { start : { x: startX, y: startY }} = a;
console.log(startX, startY); // 5, 6
```
In the example above, the variable start is assigned the value of a.start, which is also an object.

### Instructions

Use destructuring assignment to obtain max of forecast.tomorrow and assign it to maxOfTomorrow.

## Code

### Original

```javascript
const forecast = {
  today: { min: 72, max: 83 },
  tomorrow: { min: 73.3, max: 84.6 }
};
// change code below this line
const maxOfTomorrow = undefined; // change this line
// change code above this line
console.log(maxOfTomorrow); // should be 84.6
```
### Solution

```javascript
'use strict';
const forecast = {
  today: { min: 72, max: 83 },
  tomorrow: { min: 73.3, max: 84.6 }
};
// change code below this line
const {tomorrow : {max: maxOfTomorrow}} = forecast; // change this line
// change code above this line
console.log(maxOfTomorrow); // should be 84.6
```

## My Notes

This destructuring thing is getting a bit easier. Important to keep in mind that we are assigning properties of the object to the new variable. Like `forecast.tomorrow.max`. 
