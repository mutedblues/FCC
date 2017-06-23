# Regular Expressions: Find More Than the First Match

So far, you have only been able to extract or search a pattern once.

```javascript
let testStr = "Repeat, Repeat, Repeat";
let ourRegex = /Repeat/;
testStr.match(ourRegex);
// Returns ["Repeat"]
```
To search or extract a pattern more than once, you can use the g flag.

```javascript
let repeatRegex = /Repeat/g;
testStr.match(repeatRegex);
// Returns ["Repeat", "Repeat", "Repeat"]
```

### Instructions

Using the regex starRegex, find and extract both "Twinkle" words from the string twinkleStar.

#### Note
You can have multiple flags on your regex like /search/gi

## Code

### Original

```javascript
let twinkleStar = "Twinkle, twinkle, little star";
let starRegex = /change/; // Change this line
let result = twinkleStar; // Change this line
```

### Solution

```javascript
let twinkleStar = "Twinkle, twinkle, little star";
let starRegex = /twinkle/gi; // Change this line
let result = twinkleStar.match(starRegex); // Change this line
```
