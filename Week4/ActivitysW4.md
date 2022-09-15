# Activitys

## Simple Validation Of A Username

``` javascript 

function validateUsr(username) {
  res = /^([a-z]+|\d+|_){4,16}$/.test(username);
  return res;
}

``` 

## Get Number From String

``` javascript 

function getNumberFromString(s) {
  return Number(s.replace(/\D/g, ''));
} 

``` 

## String Cleaning

``` javascript 

function stringClean(s) {
  return s.replace(/\d/g, '');
}

```

## Password Validation

``` javascript 

const REGEXP = /^(?=.*\d)(?=.*[a-z])(?=.*[A-Z])[a-zA-Z0-9]{6,}$/;

``` 

