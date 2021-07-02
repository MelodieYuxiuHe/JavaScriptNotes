# Working with Numbers

### Introduction

```javascript
let score = 0;
const pi = 3.141592653589793;
const absoluteZero = -273.15;
const numberOfAtomsOnEarth = 1.33e+105;
```

| Change the value of a variable | Shorthand version |
| :----------------------------- | :---------------- |
| `score = score + 10;`          | `score += 10;`    |
| `score = score - 20;`          | `score -= 20;`    |
| `score = score * 5;`           | `score *= 5;`     |
| `score = score / 2;`           | `score /= 2;`     |

### Treating Strings as Numbers

```javascript
"10" + "5"
// this will return 105, it's not what we want

typeof("10")
// return string
```

```javascript
//using +
let a = 123;
typeof(+a);
//return "number"
```

```javascript
parseInt()
// parse a string to integer

typeof parseInt("abccc")

parseFloat()
// parse a string to float 

parseFloat('1.89 light years away')
//return 1.89
parseInt('That is so 2008')
//return NaN 
parseInt("202.99")
//return 202

//Note: it looks for a number at the begining of a string 
```

```javascript
document.write() 
// print the message variable to the web page
```

Exercise: https://teamtreehouse.com/library/introducing-the-practice-8#workspaces

# The Math Object

Primitive Data Types

```javascript
Math.round(2.2)
//return 2

//Math like a build in library

```

### Create a Random Number

- Math.random() : returns a random value from 0 up to but not including 1
- Math.ceil()
- Math.floor() 

| Math.floor()         | Return Value | Math.ceil()         | Return Value |
| :------------------- | :----------- | :------------------ | :----------- |
| `Math.floor()`       |              | `Math.ceil()`       |              |
| `Math.floor(1.2)`    | `1`          | `Math.ceil(1.2)`    | `2`          |
| `Math.floor(0.0012)` | `0`          | `Math.ceil(0.0012)` | `1`          |
| `Math.floor(5.028)`  | `5`          | `Math.ceil(5.028)`  | `6`          |
| `Math.floor(2)`      | `2`          | `Math.ceil(2)`      | `2`          |
| `Math.floor(0)`      | `0`          | `Math.ceil(0)`      | `0`          |

```javascript
Math.floor(Math.random() * 6)
```

```javascript
const dieRoll = Math.floor(Math.random() * 6 + 1)
console.log()
// using floor and +1 is to make sure to get a value between 1 and 6

```

Random Number Challenge

```javascript
// Collect input from a user
let num = prompt("Give me a number plz");

// Convert the input to a number

num = parseInt(num);
  
// Use Math.random() and the user's number to generate a random number

new_num = num/Math.random();
// Create a message displaying the random number

console.log(new_num);

```

Random Two Number 

```javascript
const inputHigh = prompt("Give a highest number");
const highNumber = parseInt(inputHigh)
//Note how the 'highNumber' is used in the if condition
if (highNumber){
  console.log("ok looks good")
}
else{
  console.log("Need to provide a number")
}
```













