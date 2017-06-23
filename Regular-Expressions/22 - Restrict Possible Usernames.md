# Regular Expressions: Restrict Possible Usernames

Usernames are used everywhere on the internet. They are what give users a unique identity on their favorite sites.

You need to check all the usernames in a database. Here are some simple rules that users have to follow when creating their username.

1) The only numbers in the username have to be at the end. There can be zero or more of them at the end.

2) Username letters can be lowercase and uppercase.

3) Usernames have to be at least two characters long. A two-letter username can only use alphabet letter characters.

### Instructions

Change the regex userCheck to fit the constraints listed above.

## Code

### Original

```javascript
let username = "JackOfAllTrades";
let userCheck = /change/; // Change this line
let result = userCheck.test(username);
```

### Solution

```javascript
let username = "JackOfAllTrades";
let userCheck = /[a-z]{2,}\d*$/i; // Change this line
let result = userCheck.test(username);
console.log(result);
```

## My Notes

My solution passed the tests but it's much more complicated than the solution provided by FCC on github (thought I'd check my answer since it looked a bit crazy).

I used MDN's reference page to figure out how to only accept 2 or more characters using the really cool `{n,}` which: 

> Matches at least n occurrences of the preceding expression. N must be a positive integer.

> For example, /a{2,}/ will match "aa", "aaaa" and "aaaaa" but not "a"

FCC's Challenge Solution:

```
var username = "JackOfAllTrades";
var userCheck = /[a-zA-Z][a-zA-Z]+[0-9]*/; // Change this line
var result = userCheck.test(username);
```

This is definitely more simple...more elegant. Interesting to compare. Must remember to try to find simple solutions and not overcomplicate if possible.
