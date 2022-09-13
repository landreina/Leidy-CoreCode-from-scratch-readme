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



