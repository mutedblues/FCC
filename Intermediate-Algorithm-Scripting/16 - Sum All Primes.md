# Intermediate Algorithm Scripting: Sum All Primes

### Instructions

Sum all the prime numbers up to and including the provided number.

A prime number is defined as a number greater than one and having only two divisors, one and itself. For example, 2 is a prime number because it's only divisible by one and two.

The provided number may not be a prime.

Remember to use Read-Search-Ask if you get stuck. Try to pair program. Write your own code.

## Code

### Original

```javascript
function sumPrimes(num) {
  return num;
}

sumPrimes(10);
```

### Solution

```javascript
function isPrime(value) {
      for(var i = 2; i < value; i++) {
          if(value % i === 0) {
              return 0;
          }
      }
      return value;
  }

function sumPrimes(num) {
  
  let result = 0;
  
  for (let i = 2; i <= num; i++) {
    result += isPrime(i);
    }
  return result;
  
}

sumPrimes(10);
```

## My Notes

Helpful discussion at https://www.thepolyglotdeveloper.com/2015/04/determine-if-a-number-is-prime-using-javascript/
