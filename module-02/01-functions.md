# Functions
Have you ever wondered how when you turn on the dial or press a different button on your washing machine for a specific wash, it just knows what to do. You select sports wash and the machine runs a wash cycle at the same temperature every time or you turn the dial to synthetics and the machine runs a wash for the exact same length of time. Each time functions work just like this, running the same set of stored instructions repeatedly without requiring you to adjust the settings every time. Over the next few minutes you learn about the advantages of using functions in JavaScript, you will learn how functions are structured and how to declare a function in your code with the use of parameters. Finally, you will discover how to call or invoke a function with your code with the use of arguments. But first, what is a function and what does it do? One of the basic principles of programming can be summed with the acronym DRY in other words don't repeat yourself. And it's thanks to functions that you can avoid repetition. With functions you can take several lines of code that performs a set of related actions and then group them together under a single label. Then when you need to run the code that you've saved, you just invoke or call the function. You can run the code as many times as you want.
```js
function myFunc() {
  console.log("Hello World!");
}

myFunc();

// Output: Hello World!
```

For example, suppose you want to add two numbers. The process could be as follows. First creates two variables a and b. And assign each a number value, then create another variable c, which holds the value of a and b added together. Finally output the value of c to the console.
```js
var a = 10;
var b = 20;
var c = a + b;

console.log(c);

// Output: 30
```

This piece of code works and adds two numbers together. But what if you want to execute this code more than once? Well you can do this by placing this block of code inside a function. You declare a function by typing the keyword function, then space and then the name of the function. You can name the function nearly anything you want. In this example it's named addTwoNums after the function name. Place a left and right parenthesis. Finally place a left and a right curly brace to complete the function. The code to be executed will then be placed in between the left and right curly braces. And this is known as the body of the function.

It's important to remember that a function declaration on its own doesn't execute the code. It's just specifying what operations should be performed. Once the function is executed to run the functions code you need to call or invoke the function and this is achieved by typing the function named followed by the opening and closing parenthesis. Instead of saying run a function developers may say that they call a function or invoke a function but don't worry. All these terms mean the same thing to execute the code inside the functions body. Next let's explore another major advantage of functions. The use of values. Did you notice how the add to numbs example was just adding the numbers 10 and 20. These numbers are are chosen values for this function but this is just one example of the use of values with functions you can use any values you want take for example the add to numbs function created earlier. The function accepted, no arguments in other words, no parameters were defined while variables can be used to produce results. There are limitations as variables a and b have specific values and the function would always give the same result. So let's change this function to make it more flexible to do this. You need to pass values to the function. These values are known as function parameters and are placed inside the function definition.

The values passed to the function are called arguments. Let's explore this a little further now by setting a and b as parameters instead of using variables. I can easily plug in any two numbers that I want to add parameters are sort of like variable names. They allow us to set changeable values on each function call. Functions with parameters can accept any kind of value and result in clean. More efficient code building functions this way allows you to write flexible functions that can be reused with various values as many times as you need. For example by passing values as arguments to our function, addTwoNums. We can call it as many times as we want and as long as we send it to values, it will add them together and output the result. In this lesson you learned about functions in JavaScript first you created a function without parameters and assigned fixed values inside the body of the function itself. Then you learned about function parameters to pass values to functions. It's important to remember that function parameters act sort of like variable names. The actual values that these variables will be assigned will come in the form of function arguments. At the time the function is invoked.

```js
function addTwoNums(a,b) {
  var c = a + b;
  console.log(c);
}

addTwoNums(2, 2);
// Output: 4

addTwoNums(5, 10);
// Output: 15
```