# Iterate Over an Array
In this exercise, you'll use the for....of loop to iterate over an array and to iterate over an object's own properties.

**Task 1**. You are given an array of dairy products:
```js
var dairy = ['cheese', 'sour cream', 'milk', 'yogurt', 'ice cream', 'milkshake']
```

Create a function called `logDairy`. Within it, console log each of the items in the dairy array, using the for...of loop.

The expected output should be:
```bash
cheese
sour cream
milk
yogurt
ice cream
milkshake
```

**Task 2**. You are given the following starter code:
```js
const animal = {

canJump: true

};

const bird = Object.create(animal);

bird.canFly = true;

bird.hasFeathers = true;
```

Create a function called birdCan, within it, loop over the bird object's properties and console log each one, using the for...of loop. Remember, you need to console log both the key and the value of each of the bird object's properties.

**Task 3**. Using the same starter code as in **Task 2**, create a function called `animalCan` and within it, loop over all the properties in both the bird object and its prototype - the animal object - using the for...in loop.


**SOLUTIONS:**
```js
// Task 1
var dairy = ['cheese', 'sour cream', 'milk', 'yogurt', 'ice cream', 'milkshake'];
function logDairy() {
    for (var d of dairy) {
        console.log(d)
    }
}
logDairy();

// Task 2
const animal = {
    canJump: true
};
const bird = Object.create(animal);
bird.canFly = true;
bird.hasFeathers = true;
function birdCan() {
    for (prop of Object.keys(bird)) {
        console.log(prop + ": " + bird[prop]);
    }
}
birdCan();

// Task 3
function animalCan() {
    for (prop in bird) {
        console.log(`${prop}: ${bird[prop]}`);
    }
}
animalCan();
```