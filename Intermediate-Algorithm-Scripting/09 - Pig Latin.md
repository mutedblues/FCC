# Intermediate Algorithm Scripting: Pig Latin

### Instructions

Translate the provided string to pig latin.

Pig Latin takes the first consonant (or consonant cluster) of an English word, moves it to the end of the word and suffixes an "ay".

If a word begins with a vowel you just add "way" to the end.

Input strings are guaranteed to be English words in all lowercase.

Remember to use Read-Search-Ask if you get stuck. Try to pair program. Write your own code.

Run tests (ctrl + enter)


## Code

### Original

```javascript
function translatePigLatin(str) {
  return str;
}

translatePigLatin("consonant");
```

### Solution

```javascript
function translatePigLatin(str) {
  
  let reVowels = new RegExp(/[aeiou]/i);
    
  let vowelIndex = str.search(reVowels);
    
  if (str.charAt(0).match(reVowels)) {
    return str.split('').concat("way").join('');
  } else if (vowelIndex !== 0 && vowelIndex !== -1) {
    return str.substr(vowelIndex) + str.substr(0, vowelIndex) + "ay"; 
  } else {
    return str + "ay";
  }
  
}

translatePigLatin("consonant");
```
