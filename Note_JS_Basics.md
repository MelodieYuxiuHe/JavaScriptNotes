Javascript Basics

# Hello, JavaScript!

How Javascript work?

Step1: Use CMD + OPTION + J to open the console 

Step2: Paste the javascript code into the console

Step3: Hit Enter to display the webpage

Functions:

```javascript
alert("Hello");
//Pop up an alert showing "Hello"

console.log("Hello");
//Returns Hello

document.write("<h1>Welcome to my page</h1>");
//Document refers to the current webpage, write to send message - this sends the text to the temporary webpage

//You can also use the css styled stuff in the document.write()
```

Examples:

```javascript
alert("Hello, Thanks for visiting!");
console.log("Hello from my console.");
document.write("<h1>Hey</h1>");
//Use shift + enter to switch to the next line
```

One statement needs to run after the previous command finish

### Add Javascript to HTML

![Screen Shot 2021-07-02 at 1.47.04 PM](/Users/melodie/Library/Application Support/typora-user-images/Screen Shot 2021-07-02 at 1.47.04 PM.png)

2 Ways to create a JS script:

Method1:

1) Create a script using script ending with .js

2)  Link/connect that to a HTML file using:

```javascript
<script src="js/test.js"></script>
//js/test.js is the path of the target javascript script

```

![Screen Shot 2021-07-02 at 1.56.51 PM](/Users/melodie/Library/Application Support/typora-user-images/Screen Shot 2021-07-02 at 1.56.51 PM.png)

Method2:

Add the 'alert' commend to the html script

![Screen Shot 2021-07-02 at 2.01.21 PM](/Users/melodie/Library/Application Support/typora-user-images/Screen Shot 2021-07-02 at 2.01.21 PM.png)

It will first run the test.js script, then go to the alert pop window "check check etc"

Note:

It's okay to have more then 2 scripts;

It's a good habbit to put your JavaScript code just before the closing `</body>` tag on a web page, users view the contents of the web page before the javascript program runs

Homework:

```javascript
// 1. Display an alert dialog with the content: "Warning! This message will self-destruct in"

alert("Warning! This message will self-destruct in");
// 2. Display a "3... 2... 1..." countdown using 3 alert dialog boxes
alert("3...");
alert("2...");
alert("1...");

// 3. This statement selects the <h1> element and replaces its text with "BOOM!".
document.querySelector("h1").textContent = "🔥BOOM!🔥";

// 4. Log "Message destroyed!" to the console
console.log("Message destroyed!");
```

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>JavaScript Basics – Challenge</title>
    <link href="css/style.css" rel="stylesheet">   
  </head>
  <body>
    <main>
      <h1>Hello, JavaScript!</h1>
    </main>
    <script src="js/script.js"></script>    
  </body>
</html>
```

# Storing and Tracking Information with Variables

```javascript
var score = 0;
//Assigning a value to a variable//
var message = "Hi";
console.log(message);
```

Reserved Words for javascript:[![reserved words](https://image-proxy-cdn.teamtreehouse.com/347d71ba1496c34ae9cfcedf954f49b75ee17fa7/687474703a2f2f74726565686f7573652d636f64652d73616d706c65732e73332e616d617a6f6e6177732e636f6d2f6a6176617363726970742d6261736963732f6173736574732f73325f72657365727665642d776f7264732e706e67)](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Lexical_grammar#Keywords)

| Not Allowed | Allowed          |
| :---------- | :--------------- |
| `9lives`    | `right1`         |
| `pricePer#` | `$price`         |
| `@home`     | `home_alone`     |
|             | `price_per_unit` |
|             | `pricePerUnit`   |

### Change the Value in a variable

```javascript
var score = 0;
score +=  10;
console.log(score);

bonusPts = 100;
var finalsScore = score + bonusPts;
console.log(finalScore);
```

### Define Variables with let and const

```javascript
var score = 0;

const score = 5;
console.log(score);
//Often most popular way to define a variable, cannot be changed //
// if we add score += 5, after defining score using const, it will return error//

let score = 5;
score += 10;
console.log(score);
//let almost is the same as score, but if you wrote the following code:
let score = 5;
let score = 100;
//it will return error: Identifier 'score' has already been declared

var score = 5;
var score = 10;
//there won't be an error
//let is more protective in terms of not defining the variable twice when you may forget that you have already defined the same variable before 

```

Practice 

```javascript
// 1. Attach this file -- practice.js -- to the index.html file using a <script> tag

// 2. In this JavaScript file, add a prompt dialog to capture input from the user and store it in a variable
var firstName = prompt("What is your first name?");

// 3. Add a second a prompt dialog to capture input from the user and store it in a second variable
var lastName = prompt("What is your last name?");

// 4. Create a third variable and which combines an uppercase version values in the two other variables separated by a space. For example, if the first two variables contain "sally" and "forth", this third variable should contain the string value "SALLY FORTH"
var completeName = firstName.toUpperCase() + ' ' + lastName.toUpperCase();

// 5. Create a fourth variable to store a number. The number should be the total number of characters in the third variable. 
var characterCount = completeName.length;

// 6. Add an alert dialog box that says "The string '[insert value of third variable here]' is X number of characters long." For example, if the third variable contained the string "SALLY FORTH" then the alert dialog should says "The string 'SALLY FORTH' is 11 characters long."
alert("The string \"" + completeName + "\" is " characterCount + " characters long.");
```

# Working with Strings

```javascript
const message = 'I \'m a girl';
console.log(message)

//escape the '

const message = "Haha \
this \
will continue!";
console.log(message)

//note that there shouldn't be a space after \, otherwise return error
```

Note: Don't write your javascript string line one by one, otherwise using \ to connect lines

### Transform and Manipulate Strings

```javascript
// .toUpperCase()

// .toLowerCase()

let a = "CheckThe Value";
console.log(a.toUpperCase());
console.log(a.toLowerCase());

// length (return the number of characters)
const b = "14144t3";
console.log(b.length);
```

### Capture Input

```javascript
prompt();

const name = prompt("What's your name?");
console.log(name)
```

### Combine Strings

```javascript
const name = prompt("Your name?");
const message = "Hello" + " " + name;
console.log(message)
```

```javascript
const name = prompt("Your name?");
let message = "Hello, " + name + ". Welcome to my music site. ";
message += "Next line";
message += "Ohhhhh next line \n";
message += "I can use += to have another line of code";
message += "Elegant";

//create multile line scripts
console.log(message);
```

```javascript
let firstName = "M";
let lastName = "H";
let role = 'developer';
let msg = firstName + " " + lastName + ": " + role;
msg = msg.toUpperCase();
```

### Template Literals

```javascript
//`I am a template Literals!` //upper left

const name = prompt("What is your name?");

const message = `Hello, ${name}. It's ${2 *3} o' clock`;

console.log(message);

//Here you don't need to escape '
```

### Display the Value of a String on a Page

```javascript
const stringToShout = prompt("What do you want to shout?");
const shout = stringToShout.toUpperCase();
const shoutMessage = `<h2>The message to shout is: ${shout}!!!!!</h2>`;
console.log(shoutMessage);
```

```javascript
document.querySelector('main');
//interactive with the brower to find the element you want to have access to

//go to the html, and return the first main html tag

document.querySelector('main').innerHTML = shoutMessage;
```

Resources:

MDM Web Docs: Javascript - String section

### Exercise1

```javascript
// 1. Declare variables and capture input.
let variable = prompt("Input a noun");

// 2. Combine the input with other words to create a story.

let msg =  `<p>Once upon a time, someone wants to eat ${variable}!!</p>`

// 3. Display the story as a <p> inside the <main> element.
document.querySelector('main').innerHTML = msg
```

### Exercise2

```javascript
const flavor = "Blueberry";
const type = "Smoothie";
const price = 4.99;
const drink = `${flavor} ${type}: \$${price}`;

//use \$ to type the real dollar sign
```

# Making Decisions in Your Code with Conditional Statements

### Introducing Conditional Statements

```javascript
const answer = prompt("Which Plant is closest to the sun?");
if (answer.toLowerCase() == 'mercury'){
  console.log("Correct");
}
else{
  console.log("Wrong you dumb ass")
}

//So similar to R f**k
```

```javascript
("Apple" < "Pear")
//will return True, because the first letter of the word Apple is alphatically

('3' == 3)
True
//JS will transform it to number

('3' === 3)
False
//JS is trying to compare the type of two objects

('JavaScript' === 'JavaScript' )
True
('javascript' === 'JavaScript' )
False

('10' !== 10)
True

```

Note: Better to use === and !==

### Boolean Values

```javascript
let correctGuess = false;
const number = 6;
const guess = prompt("Guess a number betwee 1 and 10");

// + before the guess, transform the string to a number
if (+guess === number){
  correctGuess = true;
}

if (correctGuess){
  console.log('You guessed the number');
}else{
  console.log(`The number is ${number}`);
}
```

```javascript
if (){
    
    } else if (){
               
               } else {
  
}
```

```javascript
// and operator
&&
  
// or operator 
||
  
 
```

### Document

```javascript
// this is a single-line comment

/* erwer wer
wrwerwer e this is a multiple line 
comment! 
*/
```

![Screen Shot 2021-07-02 at 4.52.25 PM](/Users/melodie/Library/Application Support/typora-user-images/Screen Shot 2021-07-02 at 4.52.25 PM.png)

```javascript
//Example
/*
    1. Store correct answers
   - When quiz begins, no answers are correct
     */
     let correct = 0;

// 2. Store the rank of a player
let rank;

// 3. Select the <main> HTML element
const main = document.querySelector('main');

/*
    4. Ask at least 5 questions

   - Store each answer in a variable
   - Keep track of the number of correct answers
     */
     const answer1 = prompt("Name a programming language that's also a gem.");
     if ( answer1.toUpperCase() === 'RUBY' ) {
       correct += 1;
     }
     const answer2 = prompt("Name a programming language that's also a snake.");
     if ( answer2.toUpperCase() === 'PYTHON' ) {
       correct += 1;
     }
     const answer3 = prompt("What language do you use to style web pages?");
     if ( answer3.toUpperCase() === 'CSS' ) {
       correct += 1;
     }
     const answer4 = prompt("What language do you use to build the structure of web pages?");
     if ( answer4.toUpperCase() === 'HTML' ) {
       correct += 1;
     }
     const answer5 = prompt("What language do you use to add interactivity to a web page?");
     if ( answer5.toUpperCase() === 'JAVASCRIPT' ) {
       correct += 1;
     }
/*

    5. Rank player based on number of correct answers

   - 5 correct = Gold
   - 3-4 correct = Silver
   - 1-2 correct = Bronze
   - 0 correct = No crown
     */
     if ( correct === 5 ) {
       rank = "Gold";
     } else if ( correct >= 3 ) {
       rank = "Silver";
     } else if ( correct >= 1 ) {
       rank = "Bronze";
     } else {
       rank = "None :(";
     }

// 6. Output results to the <main> element
main.innerHTML = `
  <h2>You got ${correct} out of 5 questions correct.</h2>
  <p>Crown earned: <strong>${rank}</strong></p>
`;
```







