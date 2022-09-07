# Global Scope and Local Scope
You may recall that all the code outside of functions is referred to as global scope, and all the code inside of a function is known as local scope.

Local scope states that a variable is only accessible in the function where it is declared.

**Example:**
```js
let name = "Jefferson"; // global scope

function example() {
  let name = "Joel"; // local scope
}
```

The ES6 version of JavaScript introduced a new variety of scope known as the block scope. Block scope states that a variable declared in a block of code is only accessible inside that block. All the other code outside of the code block cannot access it. Block scope is built when you declare variables using let or const. In other words when you build variables with let or const, they become immediately scoped to the code block they were created in.

# Var, Let, Const
Before ES6, the only way to declare a variable in JavaScript was to use the **var** keyword. The **var** keyword is very lenient. Let's outline some characteristics of variables that are declared with var.

First, you can use it in your code even before it is declared. Also, you can redeclare the same variable when you use **VAR**.
```js
var user = "John";
var user = "Mariah";

console.log(user);
// Mariah
```

With ES6, the suggested way to declare variables is to use the let or const keywords. Its syntax is very similar to the var syntax.
```js
let user = "John";
console.log(user);
// John

const email = "john.doe@gmail.com";
console.log(email);
// john.doe@gmail.com
```
In ES6 with let and const, you use the same syntax, only changing the var keyword to either let or const. Notice that the syntax is very similar.

You might be wondering what's the difference between var, let, and const. The simplest explanation is that the behavior of let and const is more strict. With a let or a const variable, you cannot use it in your code before you declare it.