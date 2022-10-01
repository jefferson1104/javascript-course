# JavaScript modules
In JavaScript, complex programs can be useful for multiple applications and it wouldn't make sense to rewrite them over and over thankfully. Since version ES6, they can be saved and used elsewhere as modules.

JavaScript modules are standalone units of code that you can reuse again and again. Being standalone means that you can add them to your program, remove them and replace them with other modules and everything will still work.

But before we continue, let's explore what things were like before modules entered the picture. In all versions of JS, all functions that are defined on the window object are global. While useful for simple projects, this created some issues when third party libraries or multiple developers became involved. For example, a global function from one script could override a function from another one using the same variable name, techniques were developed to bypass these issues but they were not without flaws. And so for a long time, JavaScript lacked built in natively supported module functionality. An engineer at Mozilla named Kevin Bangor tried to fix this through a project called **Server JS** which was later renamed to **Common JS**.

**CommonJS** is designed to specify how modules should work outside of the browser environment. It is mostly used on server side JavaScript namely **NodeJS** a downside of **CommonJS** is that browsers don't understand its syntax. That is certain keywords that **CommonJS** relies on, such as require and **module.exports** don't work as expected in browsers.

## Examples
#### Regular scripts 

regular-scripts.html
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Regular script</title>
</head>
<body>
  Regular, "old school" JS script.
  <script type="text/javascript">
    console.log('Hello from script tag');
  </script>
  <script>
    console.log('The text/javascript is the default value.');
    console.log('So we do not even have to use it with the script tag.');
    console.log('It is implied.');
  </script>
</body>
</html>
```

browser console:
```console
Hello from script tag

The text/javascript is the default value.

So we do not even have to use it with the script tag.

It is implied.
```

#### ES6 module scripts
es6module-scripts.html
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>ES6 modules script</title>
</head>
<body>
  JS scripts as modules.
  <script type="module">
    import { informalGreeting } from './greeting.js';
    informalGreeting('Jane');
  </script>
  <script type="module">
    import { informalGreeting, formalGreeting } from './greeting.js';
    import greeting from './greeting.js';
    formalGreeting('Jhon');
    greeting();
  </script>
</body>
</html>
```

greeting.js
```js
export const informalGreeting = (person) => {
  console.log(`Hello, ${person}`);
}

export const formalGreeting = (person) => {
  console.log(`Good day, ${person}`);
}

const greeting = () => {
  console.log(`Howdy!`);
}

export default greeting;
```

browser console:
```console
Hello, Jane

Good day, Jhon

Howdy!
```

**NOTE**: For it to work well you need to run it in your vscode with an extension called "**Live server**".