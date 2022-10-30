# Tests with Jest
**Jest** is a JavaScript testing framework. It's often used for testing code like React, a JavaScript library maintained by Meta and a community of individual developers and companies. Besides plain JavaScript and React code just allows you to test Babel, TypeScript, Node, Angular, Vue, and various other frameworks. Jest also supports code **coverage**. Code **coverage** is a measure of what percentage of my code is covered by tests.

If I say that I have an 80 percent code coverage, that means that only one-fifth of my entire code base is not covered by tests. But even 100 percent code coverage doesn't mean that you have tested for every conceivable expectation. It just means that there are some expectations tested for each line of my code. Still, code coverage is a handy tool to gauge the amount of my code base that's included in tests. The higher the code coverage, the lower the chance of having unidentified bugs. As a rule, the higher the percentage of code coverage, the lower the amount of time required to write new tests. This, however, depends on whether there are incomplete software requirements pending or if you are going to receive more requirements in the future.

#### Mocking
Next, let's cover the concept of mocking. Mocking allows you to separate the code that you are testing from it's related dependencies. In other words, you can use the mocking features to make sure that your unit testing is stand-alone. For example, you can test the front end functionality of your web app by mocking the data as if it came back from a server when in fact it came from the client. Mocking is especially helpful because very often web applications are built by teams of developers. Some developers work on the backend of a feature and others work on the front end. This could result in bottlenecks. Take an example where the team decides to build a new feature that lists the address book of users of the app on the front end. The actual user related data for this feature would come from the server. But what if a back-end developer was a bit late in developing their part of the feature? Then a front end developer would be stuck waiting for the back-end developer to complete their work before the front-end code can be built. With mocking you can avoid this bottleneck. Mocks, allow you to pretend that the users are already there. The needed data comes from the mock rather than from the backend. This allows the front-end developers to finish their site of the new feature independently. In certain cases, developers can use mocking to ship features faster. Some libraries, such as sign-on, focus specifically on mocking. But the great thing about Jest is that you use it's mock functions without any additional installations. In Jest you use mocking by employing Jest mock functions. It's also easy to test asynchronous code in Jest. There are no difficult setups and tests are relatively easy to code even for newcomers to the framework. Finally, Jest allows you to perform snapshot testing. Snapshot testing is used by developers to verify that there are no regressions in the DOM of our apps after some changes to the code base are made. You're now familiar with the concept of testing your JavaScript code using the Jest testing framework. Great work.

#### Writing tests with Jest
Now, you'll explore how to install the packages needed to test your JavaScript code and the Jest framework, as well as how to set up a test. Let's say I need to write a function that takes a value and adds 5 to it.

I'll start by creating a new file and naming it `addFive.js`. The code in the `addFive` function starts with function `addFive` and then vowel in parentheses. In between curly braces, I have returned vowel plus 5 on the next line, and then on a new line, I have `module.exports` equals `addFive`. This is a simple function which will make it easier to analyze when I write tests for it. I've also added a line to export this function so that it can be used by other files in this project.

**addFive.js**
```js
function addFive(value) {
  return value + 5;
}

module.exports = addFive;
```

Now I'll switch over to using the jest testing framework to write some expectations of how this function should behave.
```bash
# verify node version
$ node -v

# verify npm version
$ npm -v

# launch node modules to create package.json file in your project
$ npm init -y

# Install jest as a development dependency in your project.
$ npm install --save-dev jest

# start test command
$ npm run test
```

In the package.json file, I'll need to make a few changes to the script section. In the test entry, I replace the text that is assigned to test with jest within double-quotes and save it.
**package.json**
```json
...
"scripts": {
  "test": "jest",
}
...
```

Now, it makes sense to create a test file for this one JavaScript file. I'll name it addFive.test.js. In the naming convention I use, I add the dot test just before the dot js section of the file's name.
**addFive.test.js**
```js
const { default: TestRunner } = require('jest-runner');
const addFive = require('./addFive');

TestRunner('returns the number plus 5', () => {
  expect(addFive(1)).toBe(6)
})
```

![result test](https://i.ibb.co/gmXB4BT/Screen-Shot-2022-10-29-at-23-34-48.png)

First I exported the `addFive` function from my `addFive.js` file using a `const`. My expectation is that this function returns whatever value I input plus five. To check, I'll use the test method with a string as a parameter that describes the test. This string will be output in the command line when I run the test along with the words `pass` or `fail`. And the function to run when I execute the `npm run test` command. The function will check if my expectation is correct. 