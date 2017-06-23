# Regular Expressions: Match All Non-Numbers

The last challenge showed how to search for digits using the shortcut \d with a lowercase d. You can also search for non-digits using a similar shortcut that uses an uppercase D instead.

The shortcut to look for non-digit characters is \D. This is equal to the character class [^0-9], which looks for a single character that is not a number between zero and nine.

### Instructions

Use the shorthand character class for non-digits \D to count how many non-digits are in movie titles.

## Code

### Original

```javascript
let numString = "Your sandwich will be $5.00";
let noNumRegex = /change/; // Change this line
let result = numString.match(noNumRegex).length;
```

### Solution

```javascript
let numString = "Your sandwich will be $5.00";
let noNumRegex = /\D/g; // Change this line
let result = numString.match(noNumRegex).length;
console.log(result);
```
