# Spread operator
The spread operator is another of the many great new editions that came to the JavaScript language in its ES6 update. It is the shortest and simplest method to copy the properties of an object onto a newly created object. Think of the spread operator as a magical multi-purpose tool that can spread out array items and join objects together.


#### Example
no need for spread operator
```js
let top3 = {
  "The Colosseum",
  "Trevi Fountain",
  "The Vatican City",
}

function showItinerary(place1, place2, place3) {
  console.log("Visit " + place1);
  console.log("Then visit " + place2);
  console.log("Finish with a visit to " + place3);
}

showItinerary(top3[0], top3[1], top3[2]);
```

using spread operator
```js
let top3 = {
  "The Colosseum",
  "Trevi Fountain",
  "The Vatican City",
}

function showItinerary(place1, place2, place3) {
  console.log("Visit " + place1);
  console.log("Then visit " + place2);
  console.log("Finish with a visit to " + place3);
}

showItinerary(...top3);
```

# Rest operator
You might already know, that a spread operator in JavaScript, is used to unpack a box, for example, to unpack an array. The rest operator, on the other hand, is used to build a smaller box, and pack items into it.

#### Example
```js
const top7 = [
  "The Colosseum",
  "The Roman Forum",
  "The Vatican",
  "Trevi Fountain",
  "The Pantheon",
  "Piazza Venezia",
  "The Palatine Hill",
]

const [first, second, third, ...secondVisit] = top7;

console.log(secondVisit)
```

console log output:
```js
[
  'Trevi Fountain',
  'The Pantheon',
  'Piazza Venezia',
  'The Palatine Hill'
]
```

# Using Spread and Rest
In this reading, you'll learn how to join arrays, objects using the rest operator. You will also discover how to use the spread operator to:
- Add new members to arrays without using the **`push()`** method,
- Convert a string to an array and
- Copy either an object or an array into a separate object 

**Recall that the `push()` and `pop()` methods are used to add and remove items from the end of an array.**

#### Join arrays, objects using the rest operator
Using the spread operator, it's easy to concatenate arrays:
```js
const fruits = ['apple', 'pear', 'plum']
const berries = ['blueberry', 'strawberry']
const fruitsAndBerries = [...fruits, ...berries] // concatenate
console.log(fruitsAndBerries); // outputs a single array

// ['apple', 'pear', 'plum', 'blueberry', 'strawberry']
```

It's also easy to join objects:  
```js
const flying = { wings: 2 }
const car = { wheels: 4 }
const flyingCar = {...flying, ...car}
console.log(flyingCar) 

// {wings: 2, wheels: 4}
```

#### Add new members to arrays without using the push() method
Here's how to use the spread operator to easily add one or more members to an existing array:
```js
let veggies = ['onion', 'parsley'];
veggies = [...veggies, 'carrot', 'beetroot'];
console.log(veggies);

// ['onion', 'parsley', 'carrot', 'beetroot']
```

#### Convert a string to an array using the spread operator
Given a string, it's easy to spread it out into separate array items:
```js
const greeting = "Hello";
const arrayOfChars = [...greeting];
console.log(arrayOfChars); 

//  ['H', 'e', 'l', 'l', 'o']
```

#### Copy either an object or an array into a separate one
Here's how to copy an object into a completely separate object, using the spread operator.
```js
const car1 = {
    speed: 200,
    color: 'yellow'
}
const car 2 = {...car1}

car1.speed = 201

console.log(car1.speed, car2.speed)

// 201, 200
```

You can copy an array into a completely separate array, also using the spread operator, like this:
```js
const fruits1 = ['apples', 'pears']
const fruits2 = [...fruits]
fruits1.pop()
console.log(fruits1, "not", fruits2)

// ['apples'] 'not' ['apples','pears']
```
