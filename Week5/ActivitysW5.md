# Activitys 

## Find The Missing Letter
 
``` javascript 

function findMissingLetter(array) {
  for (let i = 0; i < array.length; i++) {
    if (array[i].charCodeAt() + 1 !== array[i + 1].charCodeAt()) {
      return String.fromCharCode(array[i].charCodeAt() + 1);
    }
  }
}

``` 

## Reverse Or Rotate?

``` javascript 

function revrot(str, sz) {
  if (sz <= 0 || sz >= str.length || str === '') return '';
  let regex = new RegExp(`\\d{${sz}}`, 'g');
  let chunks = str.match(regex);
  let sum = 0;
  let chunkArray = [];
  let result = chunks.map((chunk) => {
    sum = chunk
      .split('')
      .map((digit) => Math.pow(+digit, 3))
      .reduce((prev, curr) => prev + curr, 0);
    chunkArray = chunk.split('');
    if (sum % 2 === 0) return chunkArray.reverse().join('');
    return chunkArray.push(chunkArray.shift()), chunkArray.join('');
  });
  return result.join('');
}

``` 

## What's Your Poison?

``` javascript 

function find(rats) {
  return rats.reduce((prev, curr) => {
    return prev + Math.pow(2, curr);
  }, 0);
}

``` 

## Array.diff

``` javascript 

function arrayDiff(a, b) {
  return a.filter((e) => b.indexOf(e) === -1);
}

``` 

