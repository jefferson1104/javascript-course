# Try catch blocks
Next, you'll learn about some of the different JavaScript tools used to catch these errors.

You may recall that when your code contains an error, it stops running.

Well, in JavaScript, there are some built in statements to help your code continue to run even if an error occurs.

You will learn about the statements **throw**, **try** and **catch** and how they can be used to work with errors in JavaScript and prevent your code from stopping. This process is more commonly known as error handling. 

First, let's explore the **try**, **catch** statement that uses the key words, try and catch.


If a piece of code throws an error, it can get wrapped inside a try block. Then you can catch the error with the catch block, and use it to do something. For example, output the error message to the console.
```js
try {
  console.log(c + d);
} catch (err) {
  // do something here...
}

console.log('This line now runs');
```

Another key word that you need to be aware of is that throw keyword. Using the throw keyword, you can force an error to be thrown from the try block to the catch block.
```js
try {
  throw new Error();
} catch (err) {
  console.log(err)
}

console.log('This line now runs');
```

### Examples
```js
console.log(a + b);
console.log('This line is never reached');

// ReferenceError: a is not defined
```
The line containing **console.log("This line is never reached")** will not be executed as the code will stop as it contains an error, because variables "**a**" and "**b**" were not declared.


```js
try {
  console.log(a + b);
} catch(err) {
  console.log(err);
  console.log('There was an error');
  console.log('The error was saved in the error log');
}

console.log('My program does not stop');
```
The benefit of using try catch is that even if JavaScript throws an error while going through our code, it will not stop program execution.

In order for the code to continue executing the next lines without stopping, we use **try** and **catch** to handle the error.

It's important to understand here that the error is output because I logged it to the console.


```js
try {
  throw new ReferenceError();
} catch(err) {
  console.log(err);
  console.log('There was an error');
}

console.log('My program does not stop');
```
In this example, the try block contains the throw statement to throw a new reference error. In the catch block there are two console logs. The first one outputs the error object and the second outputs the string, there was a reference error. Outside the try catch blocks, the program ends with a console logs to output the string, My program does not stop. When I run this code, notice that the reference error is output. This is the error that was thrown in the try block and then output using the error object in the catch block.