# Function calling and recursion
In JavaScript, functions that repeat tasks are similarly helpful, unless they run endlessly. I'll demonstrate what recursive functions are, and help you understand how to write them properly to avoid getting stuck in an infinite loop. 


### Code examples
I've built a function called example with three lines. When I run it, each of the lines will be executed one at a time in sequence producing three strings.
```javascript
function example() {
  console.log('line one');
  console.log('line two');
  console.log('line three');
}

example();

/* OUTPUT:
line one
line two
line three
*/
```

To make things interesting, let's add one more line to the example function. This time, type the name of the function itself. So that's example, parentheses, semicolon. Now, if I run the function again, it will repeat in an infinite loop. Obviously this wouldn't be useful.
```javascript
function example() {
  console.log('line one');
  console.log('line two');
  console.log('line three');

  example();
}

example();

// infinite loop
```

Now here's a correct example of making a recursive function and avoiding the infinite loop problem:
```javascript
let counter = 3;
function example() {
  console.log(counter);
  counter = counter - 1;
  if (counter === 0) return;
  example();
}

example();
```
