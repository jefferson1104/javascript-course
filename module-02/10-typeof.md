# Typeof
You'll learn how to use the type of operator to identify the data type of elements in JavaScript. The type of operator accepts and evaluates a parameter and returns the name of the data type represented as a string. To use it, you can type typeof followed by the parameter enclosed within parentheses.

### Examples

```js
// USING TYPEOF EXAMPLES

var test1 = typeof('what is this?');
console.log(test1);
// string

var test2 = typeof(10);
console.log(test2);
// number

var test3 = typeof(3.14);
console.log(test3);
// number

var test4 = typeof(true);
console.log(test4);
// boolean

var test5 = typeof(false);
console.log(test5);
// boolean

var test6 = typeof(1 < 2);
console.log(test6);
// boolean

var test7 = typeof([1, 2, 3]);
console.log(test7);
// object

var test8 = typeof({ firstProperty: 1 });
console.log(test8);
// object

var test9 = typeof(function abc(){ console.log('abc'); });
console.log(test9);
// function
```


