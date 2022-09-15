# Default Parameters
A useful a ES6 feature allows me to set a default parameter inside a function definition  First, .

What that means is, I'll use an ES6 feature which allows me to set a default parameter inside a function definition, which goes hand in hand with the defensive coding approach, while requiring almost no effort to implement.

For example, consider a function declaration without default parameters set:
```js
function noDefaultParams(number) {
    console.log('Result:', number * number)
}
```

Obviously, the `noDefaultParams` function should return whatever number it receives, squared.

However, what if I call it like this:
```js
noDefaultParams(); // Result: NaN
```

JavaScript, due to its dynamic nature, doesn't throw an error, but it does return a non-sensical output.

Consider now, the following improvement, using default parameters:
```js
function withDefaultParams(number = 10) {
    console.log('Result:', number * number)
}
```

Default params allow me to build a function that will run with default argument values even if I don't pass it any arguments, while still being flexible enough to allow me to pass custom argument values and deal with them accordingly.

This now allows me to code my classes in a way that will promote easier object instantiation.

Consider the following class definition:
```js
class NoDefaultParams {
    constructor(num1, num2, num3, string1, bool1) {
        this.num1 = num1;
        this.num2 = num2;
        this.num3 = num3;
        this.string1 = string1;
        this.bool1 = bool1;
    }
    calculate() {
        if(this.bool1) {
            console.log(this.string1, this.num1 + this.num2 + this.num3);
            return;
        }
        return "The value of bool1 is incorrect"
    }
}
```

Now I'll instantiate an object of the `NoDefaultParams` class, and run the `calculate()` method on it. Obviously, the `bool1` should be set to `true` on invocation to make this work, but I'll set it to false on purpose, to highlight the point I'm making.
```js
var fail = new NoDefaultParams(1,2,3,false);
fail.calculate(); // 'The value of bool1 is incorrect'
```

This example might highlight the reason sometimes weird error messages appear when some software is used - perhaps the developers just didn't have enough time to build it better.

However, now that you know about default parameters, this example can be improved as follows:
```js
class WithDefaultParams {
    constructor(num1 = 1, num2 = 2, num3 = 3, string1 = "Result:", bool1 = true) {
        this.num1 = num1;
        this.num2 = num2;
        this.num3 = num3;
        this.string1 = string1;
        this.bool1 = bool1;
    }
    calculate() {
        if(this.bool1) {
            console.log(this.string1, this.num1 + this.num2 + this.num3);
            return;
        }
        return "The value of bool1 is incorrect"
    }
}
var better = new WithDefaultParams();
better.calculate(); // Result: 6
```

This approach improves the developer experience of my code, because I no longer have to worry about feeding the `WithDefaultParameters` class with all the arguments. For quick tests, this is great, because I no longer need to worry about passing the proper arguments.

Additionally, this approach really shines when building inheritance hierarchies using classes, as it makes it possible to provide only the custom properties in the sub-class, while still accepting all the default parameters from the super-class constructor.

In conclusion, in this reading I've covered the following:
- How to approach designing an object-oriented program in JavaScript 
- The role of the `extends` and `super` keywords 
- The importance of using default parameters.
