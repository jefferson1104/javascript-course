# Object Oriented Programming
In programming, there is something known as the programming paradigms. You can think of this as a classification, a style or just a general way to write code. You may already be familiar with one of these paradigms.

The **object oriented programming paradigm**, often referred to as **OOP**. OOP revolves around the idea of organizing our programs using objects to group related data and functionality.

This is in contrast to the functional programming approach, where the data used in the app needs to be kept separate from functions that operate on that data. Let's explore this concept further using some code examples from the two paradigms.

**Functional programming example**
```js
var shoes = 100;
var stateTax = 1.2;

function totalPrice(shoes, tax) {
  return shoes * tax;
}

var toPay = totalPrice(shoes, stateTax);

console.log(toPay);
// 120
```


**object oriented programming example**
```js
var purchase1 = {
  shoes: 100,
  stateTax: 1.2,
  totalPrice: function() {
    var calculation = this.shoes * this.stateTax;
    console.log('Total price:', calculation);
  }
}

purchase1.totalPrice(); // 120
purchase1.stateTax; // 1.2
```

```js
var purchase2 = {
  shoes: 50,
  stateTax: 1.2,
  totalPrice: function() {
    var calculation = this.shoes * this.stateTax;
    console.log('Total price:', calculation);
  }
}

purchase1.totalPrice(); // 60
purchase1.stateTax; // 1.2
```