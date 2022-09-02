# functional programming
In programming, there are two commonly used paradigms. Functional programming, sometimes abbreviated as FP, and object-oriented programming, sometimes abbreviated as OOP. You can think of these paradigms as different approaches to writing code. But the result is still the same, instructing a computer to perform a set of operations.

In this lesson, you will learn about functional programming. Let's now focus on the functional programming style. There is a clear distinction between data and functions in functional programming as data can exist outside of functions. For example, you may recall that when functions need some data you pass them the values in the form of arguments. Then the function perform some work on the given data and returns some values that you can then use somewhere else in your program. An alternative paradigm is the object-oriented programming paradigm, where you combine both data and functions into objects. You'll learn more about object oriented programming later.

### Example
Now let's examine a practical implementation of the functional programming style using a coding example to calculate currency conversion.

In functional programming, data and functions that operate on it are clearly separated, not combined inside objects.
```js
var currencyOne = 100;
var currencyTwo = 0;
var exchangeRate = 1.2;

function convertCurrency(amount, rate) {
  return amount * rate;
}

currenctyTwo = convertCurrency(currencyOne, exchangeRate);

console.log(currencyTwo);

// 120
```

# Return values from functions
Many functions, by default, return the value of **undefined**.

An example is the **console.log()** function.

If I run:
```js
console.log('Hello');
```

... here's the output in the console:
```bash
Hello
undefined
```

Because the **console.log()** function is built so as to not have the explicitly set return value, it gets the default return value of **undefined**.

I'll now code my own implementation of **console.log()**, which doesn't return the value of **undefined**:
```js
function consoleLog(val) {
    console.log(val)
    return val
}
```

I'm using the **console.log()** function inside my custom **consoleLog** function declaration. And I'm specifying it to return the value of its argument.

Now when I run my custom **consoleLog()** function:
```js
consoleLog('Hello')
```

I get the following output:
```bash
Hello
'Hello'
```

So, the value is output in the console, but it's also returned.

Why is this useful?

It's useful because I can use return values from one function inside another function.

Here's an example.

I'll first code a function that returns a double of a number that it received:
```js
function doubleIt(num) {
    return num * 2
}
```

Now I'll code another function that builds an object with a specific value:
```js
function objectMaker(val) {
    return {
        prop: val
    }
}
```

I can call the **objectMaker()** function with any value I like, such as:
```js
objectMaker(20);
```

The returned value will be an object with a single **prop** key set to **20**:
```js
{prop:20}
```

Now consider this code:
```js
doubleIt(10).toString()
```

The above code returns the number **20** as a string, that is: "**20**".

I can even combine my custom function calls as follows:
```js
objectMaker( doubleIt(100) );
```

This will now return the following value:
```js
{prop: 200}
```

What does all of this mean?

It means that by JavaScript allowing me to use the **return** keyword as described above, I can have multiple function calls, returning data and manipulating values, based on whatever coding challenge I have in front of me.

Being able to return custom values is one of the foundations that makes functional programming possible.
