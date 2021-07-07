# Create Reusable Code with Functions



### Introducing Functions in JavaScript

```javascript
function goToCoffeeShop(){
  alert("Your coffee is on the way");
}

goToCoffeeShop();

```

```javascript
function getRandomNumber(){
  const randomNumber = Math.floor(Math.random()*6) +1;
  return randomNumber;
}

console.log(getRandomNumber());
const dieRoll = getRandomNumber();

```

### Using Multiple return Statements

```javascript
function isFieldEmpty(){
  const field = document.querySelector('#info');
  if (field.value === ""){
    return true;
  } else{
    return false;
  }
}

const fieldTest = isFieldEmpty();

if (fieldTest === true){
  alert("Please provide your information"); 
}
```

