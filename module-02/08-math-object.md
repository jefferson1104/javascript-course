# Math object cheat sheet
JavaScript has handy built-in objects. One of these popular built-in objects is the Math object.

By the end of this reading, you'll be able to:

- Outline the built-in properties and methods of the Math object


### Number constants
Here are some of the built-in number constants that exist on the Math object: 

- The PI number: `Math.PI`
- The Euler's constant: `Math.E`
- The natural logarithm of 2: `Math.LN2`


### Rounding methods
These include: 
- `Math.ceil()` - rounds up to the closest integer 

- `Math.floor()` - rounds down to the closest integer 

- `Math.round()` - rounds up to the closest integer if the decimal is .5 or above; otherwise, rounds down to the closest integer 

- `Math.trunc()` - trims the decimal, leaving only the integer


### Arithmetic and calculus methods
Here is a non-conclusive list of some common arithmetic and calculus methods that exist on the `Math` object: 

- `Math.pow(2,3)` - calculates the number 2 to the power of 3, the result is 8 

- `Math.sqrt(16)` - calculates the square root of 16, the result is 4 

- `Math.cbrt(8)` - finds the cube root of 8, the result is 2 

- `Math.abs(-10)` - returns the absolute value, the result is 10 

- Logarithmic methods: `Math.log()`, `Math.log2()`, `Math.log10()` 

- Return the minimum and maximum values of all the inputs: `Math.min(9,8,7)` returns `7`, `Math.max(9,8,7)` returns `9`.

- Trigonometric methods: `Math.sin()`, `Math.cos()`, `Math.tan()`, etc.

# Math Object

### Random method
A part of the Math object that can generate a number between 0 and 0.99

example:
```js
// Generate a decimal number between 0 and 0.99
Math.random();

// Save it to a variable
var decimal = Math.random();

// Log te value of decimal to the console
console.log(decimal);

// Log the value of decimal multiplied by 10
console.log(decimal * 10);
```

result the logs:
```js
// 0.674322926681264

// 6.743229266812641
```


### Ceil method
A part of the Math object that rounds a decimal up to the nearest integer

example:
```js
var rounded1 =  Math.ceil(0.0001);
console.log(rounded1);
// 1

var rounded2 =  Math.ceil(0.5);
console.log(rounded2);
// 1

var rounded3 =  Math.ceil(0.99);
console.log(rounded3);
// 1

var rounded4 =  Math.ceil(1.01);
console.log(rounded4);
// 2

var rounded5 =  Math.ceil(1.5);
console.log(rounded5);
// 2

var rounded6 =  Math.ceil(2.99);
console.log(rounded6);
// 3
```


### Random integer
Get a random decimal number between 0 and 0.99... multiply by 10 and save it to a variable

Rounding up the value of decimal and log the value of rounded to the console.

```js
var decimal = Math.random() * 10;

var rounded = Math.ceil(decimal);

console.log(rounded);

// 10
```