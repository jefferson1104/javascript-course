# Classes 
In programming there are situations where you need to build many objects that have a certain specific set of properties and methods. For example, yo might need to build hundreds of car objects for a car racing game. To code this efficiently, you can use something called classes. They are essentially a blueprint that you can repeatedly use to build new objects of a certain kind, as many times as you like.

In JavaScript any class is built using the **class** keyword, followed by the name of the class starting with a capital letter and a pair of curly braces. 

Inside of the curly braces you have the **constructor** function which accepts as many parameters as needed. The role of the **constructor** function is to assign the passed in parameters to the future objects properties.

It is the **constructor** function that is used when instantiating new objects, instances of a given class. After the **constructor** is defined, you add as many methods as you want. It's important to remember that you don't use the function keyword here. Just the name of the method is needed.

### Example:
Create and define a class called Car:
```js
class Car {
  constructor(color, speed) {
    this.color = color;
    this.speed = speed;
  }

  turboOn() {
    console.log("Turbo is on!");
  }
}
```

Now that you have instantiation the car class and saved the instant of the class as **car1**.
```js
const car1 = new Car("red", 120);
```

You have access to its methods and properties. For example, to access the **turboOn()** method, you type the name of the object which is **car1**, then the dot and then the name of the method that exists on that object.
```js
car1.turboOn();

// OUTPUT: Turbo is on!
```

In this example, the **turboOn()** method, with a pair of parenthesis to invoke it. When invoked, the **turboOn()** method will work with the available data in the **car1** object to produce its output. Like with regular functions, you can also pass parameters to the class methods and then use them the same as with regular functions.

You learned about classes and how they can be used to build multiple object instances with specific properties.