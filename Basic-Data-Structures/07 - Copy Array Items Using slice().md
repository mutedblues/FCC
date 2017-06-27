# Basic Data Structures: Copy Array Items Using slice()

The next method we will cover is slice(). slice(), rather than modifying an array, copies, or extracts, a given number of elements to a new array, leaving the array it is called upon untouched. slice() takes only 2 parameters — the first is the index at which to begin extraction, and the second is the index at which to stop extraction (extraction will occur up to, but not including the element at this index). Consider this:

```javascript
let weatherConditions = ['rain', 'snow', 'sleet', 'hail', 'clear'];

let todaysWeather = weatherConditions.slice(1, 3);
// todaysWeather equals ['snow', 'sleet'];
// weatherConditions still equals ['rain', 'snow', 'sleet', 'hail', 'clear']
```
In effect, we have created a new array by extracting elements from an existing array.

### Instructions

We have defined a function, forecast, that takes an array as an argument. Modify the function using slice() to extract information from the argument array and return a new array that contains the elements 'warm' and 'sunny'.

## Code

### Original

```javascript
function forecast(arr) {
  // change code below this line
  
  return arr;
}

// do not change code below this line
console.log(forecast(['cold', 'rainy', 'warm', 'sunny', 'cool', 'thunderstorms']));
```

### Solution

```javascript
function forecast(arr) {
  // change code below this line
    
    return arr.slice(2, 4);
}

// do not change code below this line
console.log(forecast(['cold', 'rainy', 'warm', 'sunny', 'cool', 'thunderstorms']));
```

## My Notes

I had first tried to use the following code:

```
arr.slice(2, 4);
return arr;
```
This returns the original array since I'm not storing the [new array](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/slice) in a new variable created by slice().

A more verbose statement would be:

```
function forecast(arr) {
  // change code below this line
    arr = arr.slice(2, 4);
    console.log(arr);
    return arr;
}

// do not change code below this line
console.log(forecast(['cold', 'rainy', 'warm', 'sunny', 'cool', 'thunderstorms']));
```

But if we simply want to return the new value to the caller (in this case `forecast()`), using `return arr.slice(2, 4);` seems to be the cleanest method.

From [stackoverflow](https://stackoverflow.com/questions/7187114/when-to-use-return-and-what-happens-to-returned-data):

> In which cases should I use return?
> When the function is generating some value and you want to pass it back to the caller. Take Math.pow for example. It takes two arguments, the base and the exponent and returns the base raised to the exponent.

> When a value is returned from a function, what happens to it? is it stored somewhere?
> If you want to store the return value, then you have to assign it to a variable

> `var value = someFunction();`

> This stores the return value of someFunction in value. If you call the function without assigning the return value, then the value is just silently dropped:

> `someFunction();`

