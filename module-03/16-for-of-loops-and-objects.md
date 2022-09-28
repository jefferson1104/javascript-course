# For of loops and objects
You'll learn how the for of loop works conceptually.

To begin, it's important to know that a for of loop cannot work on an object directly, since an **object is not iterable**. For example:
```js
const car = {
    speed: 100,
    color: "blue"
}

for(prop of car) {
    console.log(prop)
}
```

Running the above code snippet will throw the following error:  
```js
Uncaught TypeError: car is not iterable
```

Contrary to objects, arrays are iterable. For example:  
```js
const colors = ['red','orange','yellow']
for (var color of colors) {
    console.log(color);
}
```

This time, the output is as follows:  
```bash
red
orange
yellow
```

Luckily, you can use the fact that a for of loop can be run on arrays to loop over objects.

But how?

Before you can properly answer this question, you first need to review three built-in methods: `Object.keys()`, `Object.values()`, and `Object.entries()`.

### Built-in methods
**The `Object.keys()` method**

The `Object.keys()` method receives an object as its parameter. Remember, this object is **the object you want to loop over**. It's still too early to explain how you'll loop over the object itself; for now, focus on the returned array of properties when you call the `Object.keys()` method.

Here's an example of running the `Object.keys()` method on a brand new `car2` object:
```js
const car2 = {
    speed: 200,
    color: "red"
}
console.log(Object.keys(car2)); 
// ['speed','color']
```

So, when I run `Object.keys()` and pass it my `car2` object, **the returned value is an array of strings**, where each string is a property key of the properties contained in my `car2` object.

**The `Object.values()` method**

Another useful method is `Object.values()`:
```js
const car3 = {
    speed: 300,
    color: "yellow"
}
console.log(Object.values(car3));
// [300, 'yellow']
```

**The `Object.entries()` method**

Finally, there's another useful method, `Object.entries()`, which returns an array listing both the keys and the values.  
```js
const car4 = {
    speed: 400,
    color: 'magenta'
}
console.log(Object.entries(car4));
```

What gets returned from the invocation of the `Object.entries()` method is the following:  
```js
[ ['speed', 400], ['color', 'magenta'] ]
```

This time, the values that get returned are 2-member arrays nested inside an array. In other words, you get an array of arrays, where each array item has two members, the first being a property's key, and the second being a property's value.

Effectively, it's as if you was listing all of a given object's properties, a bit like this:
```js
[
    [propertyKey, propertyVal],
    [propertyKey, propertyVal],
    ...etc
]
```

To summarise, you learned that you can loop over arrays using the `for of` loop.  You also learned that you can extract object's keys, values, or both, using the `Object.keys()`, `Object.values()` and `Object.entries()` syntax.

### Examples
You now have all the ingredients that you need to **loop over any object's own property keys and values**.

Here's a very simple example of doing just that:
```js
var clothingItem = {
    price: 50,
    color: 'beige',
    material: 'cotton',
    season: 'autumn'
}

for( key of Object.keys(clothingItem) ) {
    console.log(keys, ":", clothingItem[key])
}
```

The trickiest part to understand in this syntax is probably the `clothingItem[key]`.

Luckily, this is not too hard to comprehend, especially since you've already covered the concept previously when you were learning **how to access an object's member using the brackets notation**. 

Recall that you also learned how you can dynamically access a property name.

To revisit this concept and show a practical demo of how that works, let's code a function declaration that randomly assigns either the string `speed` or the string `color` to a variable name, and then build an object that has only two keys: a `speed` key and a `color` key.

After this setup, you will be able to dynamically access either one of those properties on a brand new `drone` object, using the brackets notation.

Here's the example's code:
```js
function testBracketsDynamicAccess() {
  var dynamicKey = Math.random() > 0.5 ? "speed" : "color";

    var drone = {
      speed: 15,
      color: "orange"
    }

    console.log(drone[dynamicKey]);
}
testBracketsDynamicAccess();
```

This example might feel a bit convoluted, but its purpose is to demo the fact that you're getting either one or the other value from an object's key, based on the string that got assigned to the `dynamicKey` variable, and accessed without issues, using the brackets notation.

Feel free to run the `testBracketsDynamicAccess()` function a few times, and you'll notice that sometimes the value that gets output is `15`, and sometimes it's `orange`, although I'm always accessing the `drone[dynamicKey]` key. Since the `dynamicKey` is an expression that gets evaluated, based on the `Math.random()` invocation, sometimes that expression evaluates to `drone["speed"]`, and other times that expression evaluates to `drone["color"]`.

You have now learned about the building blocks that make the for of loop useful to iterate over objects - although objects are not iterables. 

Next, you'll have a go at a practical example of working with both the for of and the for in loop. Each loops have their place and can be considered useful in different situations.


# OTHERS EXAMPLES
Now you know how to differentiate between for-in and for-of loops.


##### example 01
```js
const car = {
  engine: true,
  steering: true,
  speed: "slow"
}
const sportsCar = Object.create(car);
sportsCar.speed = "fast";
console.log("The sportsCar object: ", sportsCar);


console.log("----- for-in is unreliable -----");
for (prop in sportsCar) {
  console.log(prop);
}
console.log("🤔", "Iterating over object AND its prototype!");


console.log("----- for-of is reliable -----");
for (prop of Object.keys(sportsCar)) {
  console.log(prop + ": " + sportsCar[prop]);
}
console.log("🎯", "Iterating over object's OWN PROPERTIES only!");
```

output:
```bash
The sportsCar object:  { speed: 'fast' }

----- for-in is unreliable -----
speed
engine
steering
🤔 Iterating over object AND its prototype!

----- for-of is reliable -----
speed: fast
🎯 Iterating over object's OWN PROPERTIES only!
```

##### example 02
```js
const car = {
  engine: true
}
const sportsCar = Object.create(car);
sportsCar.speed = "fast";
console.log("The sportsCar object: ", sportsCar);

for (prop in sportsCar) {
  console.log(prop);
}

for (prop of Object.keys(sportsCar)) {
  console.log("🎯", prop + ": " + sportsCar[prop]);
}
```

output:
```bash
The sportsCar object:  { speed: 'fast' }

speed
engine

🎯 speed: fast
```