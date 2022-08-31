# JavaScript Errors
In JavaScript and some other programming languages, we say that an error is thrown. An error can be defined as a faulty piece of code that prevents the program from further execution, an error gets thrown and the program stops. JavaScript does its best with reporting error by outputting an error message to the console. 

In JavaScript, there are many error types and some of the most common are **syntax error**, **type error**, and **reference error**.

Let's explore syntax error and type error briefly now.

**Syntax error:**
```js
var world = "hello;

// SyntaxError: Invalid or unexpected token
```


**Type error:**
```js
(5).pop;

// TypeError: 5.pop is not a function
```

**Reference error:**
```js
console.log(c + d);

// ReferenceError: c is not defined
```
