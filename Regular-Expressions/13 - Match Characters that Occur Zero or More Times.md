# Regular Expressions: Match Characters that Occur Zero or More Times

The last challenge used the plus + sign to look for characters that occur one or more times. There's also an option that matches characters that occur zero or more times.

The character to do this is the asterisk or star: *.

```javascript
let sWord1 = "seed";
let sWord2 = "saw";
let kWord = "kite";
let sRegex = /s.*/; // Searches for words starting with s
sRegex.test(sWord1); // Returns true
sRegex.test(sWord2); // Returns true
sRegex.test(kWord); // Returns false
```

### Instructions

Create a regex starWarsRegex that uses the * character to match all the movie titles that start with "Star Wars". Your regex does not need flags.

## Code

### Original

```javascript
let starWars = "Star Wars";
let starWarsRegex = /change/; // Change this line
let result = starWars.match(starWarsRegex);
```

### Solution

```javascript
let starWars = "Star Wars";
let starWarsRegex = /Star Wars*/; // Change this line
let result = starWars.match(starWarsRegex);
console.log(result);
```

## My Notes

Couldn't understand how the answer resulted in my regex not matching "The Clone Wars" when the `*` matches characters that occur *zero* or more times. 

[MDN](https://developer.mozilla.org/en/docs/Web/JavaScript/Guide/Regular_Expressions) offers this example: 

```
Matches the preceding expression 0 or more times. Equivalent to {0,}.

For example, /bo*/ matches 'boooo' in "A ghost booooed" and 'b' in "A bird warbled" but nothing in "A goat grunted".
```

So I guess as long as any of the characters, in that order, appear in the example they will match. 'A goat grunted' doesn't match because 'o' isn't preceded by 'b'. If we changed the expression to /b*/, I imagine it would match all of the strings... 
