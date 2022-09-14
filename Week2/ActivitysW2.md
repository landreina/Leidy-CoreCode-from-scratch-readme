# Activity 1 (Tuesday)

## Multiply

``` javascript 

function multiply(a, b) {
  let m = a * b;
  return m;
}

```

## ASCII Total

``` javascript 

function uniTotal (string) {
  let long = string.length;
  let suma = 0;
  for (let i = 0; i < long; i++){
    suma = suma + string.charCodeAt(i);
  }
  return suma;
}

``` 


# Activity 2 (Wednesday)

## Char From ASCII Value

``` javascript 

function getChar(c) {
  return String.fromCharCode(c);
}

```

## Binary Addition

``` javascript 

function addBinary(a,b) {
  return (a + b).toString(2); 
}

```

## Student's Final Grade

``` javascript 

function finalGrade (exam, projects) {
  let result = 0;
  if (exam > 90 || projects > 10) {
    result = 100;
  } else 
    if (exam > 75 && projects >= 5) {
      result = 90;
    } else
      if (exam > 50 && projects >= 2) {
        result = 75;
      }
  return result; 
}

``` 

# Activity 3 (Thursday)

## Remove All Exclamation Marks From The End Of Sentence

``` javascript 

function remove (string) {  
  let result = '';
  let exclamationMark = string.length - 1;
  for (let i = exclamationMark; i > 0; i--){
    if (string[i] !== '!') {
      result = string.substring(0, i + 1);
      break;
    }
  }
  return result;
}

``` 

## Vowel Remover

``` javascript 

function shortcut(string) {
  let result = '';
  for (let i = 0; i < string.length; i++) {
    if (string[i] == 'a' || string[i] == 'e' || string[i] == 'i' || string[i] == 'o' || string[i] == 'u') {
      continue;
    }
    result = result + string[i];
  }
  return result;
}

``` 

## Rock Paper Scissors!

``` javascript 

const rps = (p1, p2) => {
  if (p1 === p2) return 'Draw!';
  if (p1 === 'rock' && p2 === 'scissors') return 'Player 1 won!';
  if (p1 === 'scissors' && p2 === 'paper') return 'Player 1 won!';
  if (p1 === 'paper' && p2 === 'rock') return 'Player 1 won!';
  return 'Player 2 won!';
};

``` 

## Persistent Bugger

``` javascript 

function persistence(num) {
  let numString = num.toString();
  let cantDigits = numString.length;
  if (cantDigits == 1) {
    return 0;
  }
  let i = 0;
  let mult = 0;
  for(; cantDigits >= 2; i++) {
    mult = 1;
    for(let j = 0; j < numString.length; j++) {
      mult = Number(mult) * Number(numString[j]);
    }
    numString = mult.toString();
    cantDigits = numString.length;
  } 
  return i;
}

```




