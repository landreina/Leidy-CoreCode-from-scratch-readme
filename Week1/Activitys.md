# Activity 1 (Tuesday)

## **Interpreted And Compiled Programming Languages**

- Una de las pautas presentes en programación, es que cada programa es único y totalmente diferente, una solución puede tener diversos caminos de ser efectivo ya que es libre interpretación pero sin olvidar el fin. 
- Al especificar lenguajes de programación como por ejemplo java, es tomar un camino de ampliación de conocimientos en base a una teoría-práctica a aprender, interpretar, entender y hasta evaluar... Por lo general cada lenguaje está basado en otro, ya sea para mejorar o bien para ampliar tomando un camino que tocaría un mejor camino o simplificando un poco... 
- Según lo anterior podemos resumir lo siguiente, Java es un lenguaje de programación compilado, pero en lugar de compilar directamente en un código de máquina ejecutable, compila en una forma binaria intermedia llamada código de bytes JVM. Luego, el código de bytes se compila y/o interpreta para ejecutar el programa...


## Pseudocode currency converter

```
  START
  Amount <-- GET
  BTCprice <-- GET FROM (https://www.coindesk.com/price/bitcoin/)
  Total <-- Amount * BTCprice
  PRINT Total
  END

```

# Activity 2 (Wednesday)

## Your date of birth in the matrix?

| Year Date | Binary Code  | 
| --------- | ------------ | 
|    1984   |  11111000000 |  



## MIPS

### Create a program to add two numbers given by the user:


```
  .data
        num1: .asciiz "\nIngrese el primer numero: "
        num2: .asciiz "\nIngrese el segundo numero: "
        resultado: .asciiz "\nEl resultado es: "

  .text
  	    main:
              li $v0, 4
              la $a0, num1
              syscall

              li $v0, 5
              syscall

              move $t0, $v0

              li $v0, 4
              la $a0, num2 
              syscall

              li $v0, 5
              syscall

              move $t1, $v0

              add $t2, $t0, $t1

              li $v0, 4
              la $a0 resultado
              syscall

              li $v0, 1
              move $a0, $t2
              syscall
 
```

### Program that display your name:


```
  .data
	      my_name: .asciiz "\nLeidy\n"
  .text
	      main:
              li $v0, 4
              la $a0, my_name
              syscall
              
```


# Activity 3 (Thursday)

## Print special numbers 

#### In this exercise you must use an iterative flow control to be able to print all the even numbers in the range of numbers from 0 to 100. Remember that you should not print each number, you should use a flow control structure to perform the exercise

``` javascript 

for (var i = 0; i <= 100; i++) {
  if (i % 2 == 0)
  console.log(i);
}

```

## Bad Code

#### The code shown below is not working in the right way, as a task you must find the error made by the developer who programmed this code and correct it, for this exercise you must explain what the error is and place the correct code

```javascript

var cond = false;
if ((cond = true)) {
  console.log('The cond variable is true');
} else {
  console.log('The cond variable is false');
}

```

#### The corrected code, after observing that you want to print the 'false' variable, the condition for its output is adapted...

``` javascript 

var cond = false;
if (cond == true) {
  console.log('The cond variable is true');
} else {
  console.log('The cond variable is false');
}

``` 

## Bad Code 2

#### You must create the code that follows the following logic, if the given number is 100, take this number as special and show the following message: "This is a special number!", but if the number is less than 1000, multiple of 10 and different from 100, you must show the following message: "This number is almost special". if none of the given conditions are met show the following message: "Just a regular number". Another developer was trying to program the logic, but apparently couldn't, you need to fix the code to work properly

``` javascript 

var n = 100;

if (n == 100) {
  console.log('This is a special number!');
}
if (n < 1000) {
  console.log('');
} else {
  console.log('Just a regular number');
}
if (n % 10 == 0) {
  console.log('This number is multiple of 10');
}

``` 

#### A correct answer can be...

``` javascript 

var n = 100;
if (n == 100) {
  console.log('This is a special number...!');
} else
  if (n < 1000 && n % 10==0 && n!==100) {
    console.log('This number is almost special');
  }
  else {
  console.log('Just a regular number');
  }

``` 


