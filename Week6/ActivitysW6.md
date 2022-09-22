# Activity 1 (Tuesday)

## Square(n) Sum

``` javascript 

export function squareSum(numbers: number[]): number {
  return numbers.reduce(
    (prev: number, curr: number) => prev + Math.pow(curr, 2),
    0
  );
}

``` 

## A Wolf In Sheep's Clothing

``` javascript 

export function warnTheSheep(queue: string[]): string {
  const wolfPosition = queue.indexOf('wolf');
  if (wolfPosition == queue.length - 1)
    return 'Pls go away and stop eating my sheep';
  return `Oi! Sheep number ${Math.abs(
    wolfPosition + 1 - queue.length
  )}! You are about to be eaten by a wolf!`;
}

``` 

# Activity 2 (Wednesday)

## A Rule Of Divisibility By 13

``` javascript 

const rem = [1, 10, 9, 12, 3, 4];
export function process(n: number): number {
  let reversedNumber: string[] = n.toString().split('').reverse();
  let index = 0;
  let result = reversedNumber.reduce((total: number, digit: string) => {
    if (index > 5) index = 0;
    return total + Number(digit) * rem[index++];
  }, 0);
  if (result === n) return result;
  return process(result);
}
export function thirt(n: number): number {
  return process(n);
}

``` 

## Playing With Digits

``` javascript 

export class G964 {
  public static digPow = (n: number, p: number) => {
    const sum = n
      //1. Convertir primero a string, porque solo está en number hasta ahorita
      .toString()
      //2. Hay que convertir de string a array porque .map solo utiliza arrays
      .split('')
      //3. Encuentra el entero positivo k * n = a^(n)+b^(n+1)+c^(n+2);
      .map(Number)
      //4. Hacer la suma cuando ya tengas cada numero expresado a su correspondiente potencia
      .reduce((prev: number, curr: number) => prev + Math.pow(curr, p++), 0);
    //5. Si el entero positivo es correcto, return k. always a positive number is using Math.abs(n);
    if (sum % n === 0) return sum / n;
    // Sino return -1
    return -1;
  };
}

``` 

# Activity 3 (Thursday) 

## Tile

``` javascript 

//Write a definition for a class named Tile that represents Scrabble tiles.
//The instance variables should be a string named letter and an number named value.
class Tile {
    letter: string;
    value: number;
//Write a constructor that takes parameters named letter and value and initializes the instance variables.
    constructor(letter: string, value: number;) {
        this.letter = letter;
        this.value = value;
    }
//Write a method named printTile that prints the instance variables in a reader-friendly format (not the { ... } format way).
    printTile(); {
    console.log(`
      ==================
        Letter: ${this.letter}
        Value: ${this.value}
      ==================
        `);
    }

}

``` 

# Time

``` javascript 

//Write a definition for the class name Time this class would be use to build a digital clock.
//This class should have 3 attributes of type number. hour, minute and second.
export class Time {
    hour: number;
    minute: number;
    second: number;
//Write a constructor that takes parameters named hour, minute and second and initializes the instance variables.
    constructor(hour: number, minute: number, second: number) {
        this.hour = hour;
        this.minute = minute;
        this.second = second;
    }
//Write a method called getInSeconds that returns a number representing the actual time in the instance represented in seconds.
    getInSeconds(): number {
        const minutes = this.hour * 60 + this.minute;
        return minutes * 60 + this.second;
    }
//Write a method named printTime that prints the instance variables in a reader-friendly format (not the { ... } format way).
    printTime() {
        console.log(` 
        ===========================
          Hours: ${this.hour}
          Minutes: ${this.minute}
          Seconds: ${this.second}
        ===========================
        `)
    }
}

//import Main from './Main';
//const main = new Main();
//main.start();

``` 

# Rational

``` javascript 

//Create a new class named Rational. A Rational object should have two number instance variables to store the numerator and denominator.
class Rational {
    numerator: number;
    denominator: number;
//Write a constructor for your class that takes two arguments and that uses them to initalize the instance variables.
    constructor(numerator: number, denominator: number) {
        this.numerator = numerator;
        this.denominator = denomintator;
    }
//Write a method called printRational that prints the object in some reasonable format.
    printRational {
        console.log(`${this.numerator} / ${this.denominator}`);
    }
//Write a method called invert that inverts the number by swapping the numerator and denominator. This method should modify the instance variables.
    invert {
        [numerator: number, denominator: number] = [denominator: number, numerator: number];
    }
//Write a method called toFloat that converts the rational number to a floating-point number and returns the result. This method is a pure function it does not modify the object.
    toFloat {
        return this.numerator / this.denominator;
    }
//Write method named reduce that reduces a rational number to its lowest terms by finding the greatest common divisor (GCD) of the numerator and denominator and dividing through.
    gcd(n: number, d: number): number {
        if(d == 0) return n;
        return this.gcd(d, n % d);
    }
    reduce() {
        const gcd = this.gcd(this.numerator, this.denominator);
        this.numerator = this.numerator / gcd;
        this.denominator = this.denominator /gcd;
    }
//This method should modify the instance variables. To calculate the GCD you can search for Euclidian Algorithm: GCD.
}

``` 
