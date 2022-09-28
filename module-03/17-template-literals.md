# Template literals examples
The aim of this reading is to help you understand how template literals work.

### What are template literals?
Template literals are an alternative way of working with strings, which was introduced in the ES6 addition to the JavaScript language.

Up until ES6, the only way to build strings in JavaScript was to delimit them in either single quotes or double quotes:
```js
'Hello, World!'
"Hello, World!"
```

Alongside the previous ways to build strings, ES6 introduced the use of backtick characters as delimiters:  
```js
`Hello, World!`
```

The above code snippet is an example of a template string, which is also known as a template literal.

**Note**: _On most keyboards, the backtick character can be located above the TAB key, to the left of the number 1 key._

### Differences between a template and regular string
There are several ways in which a template string is different from a regular string.

- First, it allows for **variable interpolation**:
```js
let greet = "Hello";
let place = "World";
console.log(`${greet} ${place} !`)
```

The above console log will output:
```js
Hello World !
```

Essentially, using template literals allows programmers to embed variables directly in between the backticks, without the need to use the `+` operator and the single or double quotes to delimit string literals from variables. In other words, in ES5, the above example would have to be written as follows:
```js
var greet = "Hello";
var place = "World";
console.log(greet + " " + place + "!");
```
- Besides variable interpolation, template strings can span multiple lines.

For example, this is perfectly good syntax:
```js
`Hello,
World
!
`
```

Notice that this can't be done using **string literals** (that is, strings delimited in single or double quotes):  
```js
"Hello,
World"
```

The above code, when run, will throw a syntax error.

Put simply, template literals allow for multi-line strings - something that simply isn't possible with string literals.
- Additionally, the reason why it's possible to interpolate variables in template literals is because this syntax actually allows for **expression evaluation**. 

In other words, this:
```js
console.log(`${1 + 1 + 1 + 1 + 1} stars!`)
```

The above example will console log the following string: **`5 stars!`**.

This opens up a host of possibilities. For example, it's possible to evaluate a ternary expression inside a template literal.

Some additional use cases of template literals are **nested template literals** and **tagged templates**. However, they are a bit more involved and are beyond the scope of this reading. 

If you're curious about how they work, please refer to the additional reading provided at the end of this lesson.

# Working with template literals

Template literals no multiline
```js
// ES5 Strings
let noMultiline = "No
 mult-line strings in ES5";

 console.log("Did you know? ", noMultiline);

// SyntaxError: Invalid or unexpected token
```

Template literals multiline
```js
// ES6 Multi-line template literals
let multiline = `
  Using ES6
  backticks,
  multi-line
  strings are
  possible!
`;

 console.log("Did you know? ", multiline);

/* 
Did you know?  
  Using ES6
  backticks,
  multi-line
  strings are
  possible!
*/
```

Template literals variable interpolation
```js
// ES6 variable interpolation

let first = `He said, "Don't you know? ES6, it's got some great features!"`;
let second = `"Wouldn't you want to learn more?", he asked.`

console.log(`${first} - and I got curious. ${second}`);

// He said, "Don't you know? ES6, it's got some great features!" - and I got curious. "Wouldn't you want to learn more?", he asked.
```