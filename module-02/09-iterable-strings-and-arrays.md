# Iterable strings and arrays
When two JavaScript developers discuss a subject related to work, sometimes you might hear the word iterable being mentioned. But what exactly does iterable mean? Well, in JavaScript an iterable is any datatype that can be iterated over using a for of loop. Some of the data types you can iterate over are arrays and strings. In this video, you will learn about the array characteristics of strings, and you will also explore further string manipulation using the concatenation operator. In the world of JavaScript, it can often be said that strings behave like arrays as strings are array-like.

### Examples
**For loop over arrays:**
```js
var letters = ['a', 'b', 'c'];

for (var i=0; i < letters.length; i++) {
  console.log(letters[i]);
}
```
```bash
# Result
a
b
c
```

**For loop over strings:**
```js
var letters = 'abc';

for (var i=0; i < letters.length; i++) {
  console.log(letters[i]);
}
```
```bash
# Result
a
b
c
```

### Other examples

**Arrays are iterable**
```js
var veggies = ['onion', 'parsley', 'carrot'];

console.log(veggies.length);
// 5

for (var i =0; i < veggies.length; i++) {
  console.log(veggies[i]);
}
```
```bash
# Result 
onion
parsley
carrot
```

**Strings are iterable, too!**
```js
var greeting = 'Howdy';

console.log(greeting.length);
// 5

for (var i =0; i < greeting.length; i++) {
  console.log(greeting[i]);
}
```
```bash
# Result 
H
o
w
d
y
```

**Concatenating strings**
Example of concatenating strings using operator "+" or using method concat()

```js
var greet = 'hello';
var user = 'Jhon';

console.log(greet + user);
// Hello Jhon

console.log(greet.concat(user));
// Hello Jhon
```

# String cheat sheet
By the end of this reading, you'll be able to:

- Identify examples of String functions and explain how to call them

In this cheat sheet, I'll list some of the most common and most useful properties and methods available on strings.

For all the examples, I'll be using either one or both of the following variables:
```js
var greet = "Hello, ";
var place = "World"
```

Note that whatever string properties and methods I demo in the following examples, I could have ran it on those strings directly, without saving them to a variable such as the ones I named **greet** and **place**.

In some of the examples that follow, for the sake of clarity, instead of using a variable name, I'll use the string itself.

All strings have at their disposal several built-in properties, but there's a single property that is really useful: the **length** property, which is used like this:
```js
greet.length; // 7
```

To read each individual character at a specific index in a string, starting from zero, I can use the `charAt()` method:
```js
greet.charAt(0); 
// 'H'
```

The `concat()` method joins two strings:
```js
"Wo".concat("rl").concat("d"); 
// 'World'
```

The `indexOf` returns the location of the first position that matches a character: 
```js
"ho-ho-ho".indexOf('h'); // 0
"ho-ho-ho".indexOf('o'); // 1
"ho-ho-ho".indexOf('-'); // 2
```

The `lastIndexOf` finds the last match, otherwise it works the same as `indexOf`.

The `split` method chops up the string into an array of sub-strings:
```js
"ho-ho-ho".split("-"); // ['ho', 'ho', 'ho']
```

There are also some methods to change the casing of strings. For example:
```js
greet.toUpperCase(); // "HELLO, "
greet.toLowerCase(); // "hello, "
```

Here's a list of all the methods covered in this cheat sheet:
- charAt() 
- concat() 
- indexOf() 
- lastIndexOf() 
- split() 
- toUpperCase() 
- toLowerCase()  


# Exercise
**Tasks to complete**

1 - Create a new empty array literal and assign it to the variable clothes.

2 - Add 5 of your favorite items of clothing as strings using the push() method.

3 - Remove the fifth piece of clothing from the array using the pop() method.

4 - Add a new piece of clothing using the push() method.

5 - Use console.log to show the third item from the clothes array in the console.

6 - Create a new empty object literal and assign it to the variable favCar.

7 - Using the dot notation, assign a color property to the favCar object and give it a string value with the color of your choice.

8 - Using the dot notation, assign a covertible property to the favCar object and give it a boolean value of your choice.

9 - Use the console to log the entire favCar object.

> *Tips*
> - Remember to use the object literal syntax: {}.
> - Remember to use the array literal syntax: [].

**Response:**
```js
var clothes = [];
clothes.push('Black t-shirt');
clothes.push('Jeans');
clothes.push('Nike sneakers');
clothes.push('Watch 7');
clothes.push('White cap')
clothes.pop();
clothes.push('Black cap');

console.log(clothes[2]);
// Nike sneakers

var favCar = {};
favCar.color = 'black';
favCar.covertible = true;

console.log(favCar);
// { color: 'black', covertible: true }
```



