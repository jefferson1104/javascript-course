# JavaScript Object Notation (JSON)

Now you know how to:
- Convert JSON strings to JS
- Use stringify to convert JS objects to JSON

It's worth remembering that JSON is basically just an object represented in the form of a string. It has some specific formatting but it's a string nonetheless. So to work with JSON, it is common to convert it back to a JavaScript object to work with its properties and methods. To do this you need to use the global built in JSON object and its parse method, let me demonstrate this now.

### Convert JSON strings to JS
First I will sign the JSON string to a variable named `jsonStr` using the `const` keyword.
```js
const jsonStr = '{"greating":"hello"}';
```

Next I'll run the JSON parse method on this variable by typing `JSON.parse()` and then `jsonStr` inside the parentheses. I press enter and notice that a regular JavaScript object is returned.
```js
JSON.parse(jsonStr);
// {greeting: 'hello'}
```

I want to save this object as a variable. So I assigned the JSON parse method to a variable named `aPlainObj` using the `const` keyword. Okay, so now that my JSON string is stored in a regular JavaScript object. I can manipulate it just like any other JavaScript object. Let me demonstrate this now by reassigning the value of the greeting property, I type the object name followed by a dot and then the object property equals hi. Press enter and notice that the word hi is output.
```js
const aPlainObj = JSON.parse(jsonStr);

aPlainObj.greeting = 'hi';
// 'hi'

aPlainObj
// {greeting: 'hi'}
```

Okay, that's how you convert a JSON string to a JavaScript object.
```js
const jsonStr = '{"greating":"hello"}';

const parsedJson = JSON.parse(jsonStr);

// {greeting: 'hello'}
```

### Convert regular Object to JSON
You can also go the other way and convert a regular object to a JSON string. Using the string of my method of the JSON object. Let me demonstrate this now. 

For example, let's start by declaring an object named data and assign it some properties and values. To run the JSON string of my method on this object, I'll type `JSON.stringfy()` and place the objects name inside the parentheses. The result is a JSON string.

example:
```js
const data = {
  firstName: "John",
  lastName: "Doe",
  greeting: "Hello",
}

JSON.stringify(data)
// '{"firstName":"John","lastName":"Doe","greeting":"Hello"}'
```

Notice that both the objects keys and its values are double quoted strings in the JSON syntax. It's important to remember that while plain JavaScript objects can hold functions, JSON strings cannot. Another limitation is that valid JSON doesn't allow the use of JavaScript comments. Also when you stringfy a JavaScript object containing a method, that method will be excluded from the stringfy operation. 