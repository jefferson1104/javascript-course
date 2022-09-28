# De-structuring arrays and objects
JavaScript objects can have properties that define their characteristics, you will learn how to D structure, objects and arrays and also how to use the D structuring syntax, to extract new variables from objects and arrays.


**Examples:**
```js
myObject = {
  name: 'jefferson',
  lastName: 'soares',
  age: 28,
}

let { name } = myObject

console.log(name) 
// jefferson
```

```js
let { PI } = Math;
PI;
// 3.141592653589793

let { pi } = Math;
pi;
// undefined

PI === Math.PI;
// true
```