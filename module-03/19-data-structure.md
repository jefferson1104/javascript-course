# Data Structures examples
In this reading, you'll learn about some of the most common examples of data structures.

The focus will be on working with the Object, Array, Map and Set data structures in JavaScript, through a series of examples.

> Note that this reading will not include a discussion of some data structures that exist in some other languages, such as Queues or Linked Lists.  Although these data structures (and other data structures too!) can be custom-coded in JavaScript, the advanced nature of these topics and the difficulty with implementing related exercises means they are beyond the scope of this reading. 

#### Working with arrays in JavaScript
Previously, you've covered a lot of concepts related to how to work with JavaScript arrays.

However, there are still a few important topics that can be covered, and one of those is, for example, working with some built-in methods.

In this reading, the focus is on three specific methods that exist on arrays:
- `forEach` 
- `filter`
- `map`
  
Let's explore these methods.

##### The forEach() method
Arrays in JavaScript come with a handy method that allows you to loop over each of their members. 

Here's the basic syntax:
```js
const fruits = ['kiwi','mango','apple','pear'];
function appendIndex(fruit, index) {
    console.log(`${index}. ${fruit}`)
}
fruits.forEach(appendIndex);
```

The result of running the above code is this: 
```js
0. kiwi
1. mango
2. apple
3. pear
```

To explain the syntax, the **`forEach()`** method accepts **a function that will work on each array item**. That function's first parameter is the current array item itself, and the second (optional) parameter is the index.

Very often, the function that the **`forEach()`** method needs to use is passed in directly into the method call, like this:
```js
const veggies = ['onion', 'garlic', 'potato'];
veggies.forEach( function(veggie, index) {
    console.log(`${index}. ${fruit}`);
});
```

This makes for more compact code, but perhaps somewhat harder to read. To increase readability, sometimes arrow functions are used. You can find out more about arrow functions in the additional reading.

##### The filter() method
Another very useful method on the array is the **`filter()`** method. It filters your arrays **based on a specific test**. Those array items that pass the test are returned.

Here's an example:
```js
const nums = [0,10,20,30,40,50];
nums.filter( function(num) {
    return num > 20;
})
```

Here's the returned array value:  
```js
[30,40,50]
```

Similar to the **`forEach()`** method, the **`filter()`** method also accepts a function and that function performs some work on each of the items in the array.

##### The map method
Finally, there's a very useful **`map`** method. 

This method is used to map each array item over to another array's item, based on whatever work is performed inside the function that is passed-in to the map as a parameter. 

For example:
```js
[0,10,20,30,40,50].map( function(num) {
    return num / 10
})
```

The return value from the above code is:  
```js
[0,1,2,3,4,5]
```

As already discussed, choosing a proper data structure affects the very code that you can write. This is because the data structure itself comes with some built-in functionality that makes it easier to perform certain tasks or makes it harder or even impossible without converting your code to a proper data structure.

Now that you've covered the methods, let's explore how to work with different built-in data structures in JavaScript.

#### Working with Objects in JavaScript
A lot of the information on how to work with objects in JavaScript has already been covered in this course.

The example below demonstrates how to use the object data structure to complete a specific task. This task is to convert an object to an array:
```js
const result = [];
const drone = {
    speed: 100,
    color: 'yellow'
}
const droneKeys = Object.keys(drone);
droneKeys.forEach( function(key) {
    result.push(key, drone[key])
})
console.log(result)
```

This is the result of executing the above code: 
```js
['speed',100,'color','yellow']
```

Although this is possible and works, having to do something like this might mean that you haven't chosen the correct data structure to work with in your code.

On the flip side, sometimes you don't get to pick the data structure you're working with. Perhaps that data comes in from a third-party data provider and all you can do is code your program so that it consumes it. You'll learn more about the interchange of data on the web when you learn about JSON (JavaScript Object Notation).

#### Working with Maps in JavaScript
To make a new Map, you can use the Map constructor:
```js
new Map();
```

A map can feel very similar to an object in JS.

However, it doesn't have inheritance. No prototypes! This makes it useful as a data storage.

For example:
```js
let bestBoxers = new Map();
bestBoxers.set(1, "The Champion");
bestBoxers.set(2, "The Runner-up");
bestBoxers.set(3, "The third place");

console.log(bestBoxers);
```

Here's the console output:  
```js
Map(3) {1 => 'The Champion', 2 => 'The Runner-up', 3 => 'The third place'}
```

To get a specific value, you need to use the **`get()`** method. For example:  
```js
bestBoxers.get(1); 
// 'The Champion'
```

#### Working with Sets in JavaScript
A set is a collection of unique values.

To build a new set, you can use the **`Set`** constructor:
```js
new Set();
```

The **`Set`** constructor can, for example, accept an array.

This means that we can use it to quickly filter an array for unique members.
```js
const repetitiveFruits = ['apple','pear','apple','pear','plum', 'apple'];
const uniqueFruits = new Set(repetitiveFruits);
console.log(uniqueFruits);
```

The above code outputs the following in the console:  
```js
{'apple', 'pear', 'plum'}
```

#### Other data structures in JavaScript
Besides the built-in data structures in JavaScript, it's possible to build non-native, custom data structures.

These data structures come built-in natively in some other programming languages  or even those other programming languages don't support them natively.

Some more advanced data structures that have not been covered include:
- Queues
- Linked lists (singly-linked and doubly-linked)
- Trees
- Graphs
