# Activity 1 (Monday) 

## Who Likes It?

``` javascript 

function likes(names) {
  if (names.length == 0) return 'no one likes this';
  if (names.length == 1) return names[0] + ' likes this';
  if (names.length == 2) return names[0] + ' and ' + names[1] + ' like this';
  if (names.length == 3)
    return names[0] + ', ' + names[1] + ' and ' + names[2] + ' like this';
  return (
    names[0] +
    ', ' +
    names[1] +
    ' and ' +
    (names.length - 2) +
    ' others like this'
  );
}

``` 

## Bit Counting

``` javascript 

var countBits = function (n) {
  let binaryNumber = n.toString(2);
  let oneBit = 0;
  for (let i = 0; i < binaryNumber.length; i++) {
    if (binaryNumber[i] === '1') oneBit++;
  }
  return oneBitCount;
};

``` 

## Your order, please

``` javascript 

function order(words) {
  let wordsArray = words.split(' ');
  wordsArray = wordsArray.sort(
    (w1, w2) => Number(w1.replace(/\D/g, '')) - Number(w2.replace(/\D/g, ''))
  );
  return wordsArray.join(' ');
}

``` 

# Activity 2 (Tuesday)

## Simple Pig Latin

``` javascript 

function pigIt(str){
  return str.replace (/(\w)(\w*)(\s|$)/g, '$2$1ay$3');
} 

``` 

## Counting Duplicates

``` javascript 

function duplicateCount(text){
  let duplicates = 0;
  text = text.toLowerCase(); // todo minuscula
  for(let i = 0; i < text.length; i++) {
    if(text.indexOf(text[i]) !== text.lastIndexOf(text[i])) {
      duplicates++;
      text = text.replace(new RegExp(`${text[i]}`, 'g'), '');
      i = i-1;
    }
  }
  return duplicates;
}

``` 

## Decode The Morse Code

``` javascript 

decodeMorse = function (morseCode) {
  return morseCode
    .split(' ')
    .map((word) => MORSE_CODE[word] || ' ')
    .join('')
    .replace(/  /g, ' ')
    .trim();
};

``` 

# Activity 3 (Wednesday)

## Valid Parentheses
 
``` javascript 

function validParentheses(parens) {
  let valid = 0;
  for (let i = 0; i < parens.length; i++) {
    if (parens[i] === ')') valid--;
    if (parens[i] === '(') valid++;
    if (valid < 0) return false;
  }
  return valid == 0;
}

``` 

## Convert String To Camel Case

``` javascript 

function toCamelCase(str) {
  return str
    .replace(/-/g, '_')
    .split('_')
    .map((word, i) => (i > 0 ? word.toUpperCase()[0] + word.substr(1) : word))
    .join('');
}

``` 

## Unique In Order

``` javascript 

var uniqueInOrder = function (iterable) {
  return [...iterable].filter((chr, i) => chr != iterable[i + 1]);
}; 

``` 

# Activity 4 (Thursday)

## Fold An Array

``` javascript 

function foldArray(a, n) {
  const r = [],
    c = a.slice();
  while (c.length) r.push(c.pop() + (c.shift() || 0));
  return n - 1 ? foldArray(r, n - 1) : r;
}

``` 

## Encrypt This!

``` javascript 

function encrypt(word) {
  if(word.length === 1) return `${word.charCodeAt(0)}`;
  const charBackup = word[1];
  word = word.replace(word[0], word.charCodeAt(0));
  word = word.replace(charBackup, word[word.length-1]);
  word = word.replace(/\w$/, charBackup);
  return word;
}

var encryptThis = function(text) {
  const textArray = text.split(' ');
  let result = '';
  textArray.forEach((w) => {
    // result = `${result === '' ? '' : `${result} `}${encrypt(w)}`;
    result = `${result} ${encrypt(w)}`;
  })
  return result.trim();
}

```

