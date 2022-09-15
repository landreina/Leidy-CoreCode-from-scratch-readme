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
 


