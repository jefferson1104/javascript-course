# TDD (Test-Driven Development)
Every piece of software is built according to formal or informal requirements. The purpose of the requirements is to explain, in human language the intricacies of what the piece of software does. So how did the requirements tie in with the practice of test driven development? Let me explain test driven development. **TDD** for short is a streamlined process of writing code that will satisfy some requirements.

Let's unpack this process a bit on a high level. A software development teams work consists of the following receiving requirements which will become a feature of the app that's being developed. Writing a failing test for that to build feature before it gets built. Making this failing test pass by coding that given feature in comparison with the traditional development process, that TDD approach might seem somewhat upside down. I am now going to demonstrate the TDD approach by writing a failing test for a javascript file and then writing code to make this test pass to understand how TDD works. Consider the following real life situation. Suppose you have to perform a task, drive your car to work. You leave your house and walk up to your car, only to find out that you don't have your car keys with you. Then you remember you left your car keys in the cabinet and you simply forgot to take them what you did there. In this imagined scenario is the opposite of TDD. You first walk to your car and only then did you check if you had your car keys if you did these things using the TDD approach, you would do the following first. You check or test if you have your keys with you. Your test fails because you don't have them. They're in the cabinet. Then you perform the action of getting your keys from the cabinet. Finally, you check or test if you have your keys this time you have them. So your test now passes. What is described here is the essence of TDD.

Imagine that you need to write code in a test driven way. Since your coding the TDD way you first write the test, even before you've written any actual implementation, for example, you test if a function named status of keys exists, you then use some testing functions from a testing framework. Since you haven't written your source code implementation. The test fails. Next you run your test. The test fails because there's no status of keys. Function declared.
```js
test('returns true if statusOfKeys exists', function() {
  expect(statusOfKeys).toBeDefined()
})
```

The logic of your test code is expect that the function status of keys exists in your source code. You declare a function named status of keys. You run the test. Again, it checks if there is such a function and it confirms it exists.
```js
test('returns true if statusOfKeys exists', function() {
  expect(statusOfKeys).toBeDefined()
})

function statusOfKeys() {}
```

So the test passes, it's important to note that one of the rules of TDD is that you should write as little code as possible to make the test pass for this test to pass, it's enough to just declare a function with the name next you receive another requirement which is as follows except a keys variable, which should be set to true and console log the keys variable. So the requirement states the status of keys function should accept a previously declared keys variable, which should be set to true. The status of keys should then console log the value of the keys variable. 
```js
const statusOfKeys = require('./statusOfKeys');
const spyConsoleLog = jest.spyOn(console, 'log');

spyConsoleLog.mockImplementation(keys => keys);

test('returns true if statusOfKeys exists', function() {
  expect(statusOfKeys).toBeDefined();
});

test('test console log inside statusOfKeys', function() {
  statusOfKeys(true);
  expect(console.log).toBeCalled();

  expect(spyConsoleLog.mock.calls[0][0]).toBe(true);

  spyConsoleLog.mockReset();
  spyConsoleLog.mockRestore();
});

function statusOfKeys(keys) {
  console.log(keys);
}
```

Finally, you examine your function code and realize that the indentation is all wrong. There are also too many unnecessary comments. So you clean up your code and run the test again to confirm that you haven't accidentally made any errors. The test still passes, so everything is okay. That is the TDD approach in a nutshell, let's go over it one more time. In a scenario as a member of the development team, your task is to read the requirements for the software that you are writing. The requirements are passed to you by the project manager. So you get your first task for the day and start coding the TDD way. First you read the new requirement. Next you write a failing test, then you update your source code. So it resolves the requirement After that you run a test that passes Finally, you re factor your implementation. This process is usually explained in three words. Red, Green. Re factor, red represents the failing test. Green on the other hand, represents the passing test after you make updates to the source code.

###### Red Green Refactor
![RED GREEN REFACTOR](https://i.ibb.co/N2NCSjB/Screen-Shot-2022-10-30-at-09-11-01.png)

The refactor represents the final tweaks to the code that don't change implementation details, which can always be confirmed by running another subsequent test when implemented correctly. TDD brings huge benefits to an organization because it allows for automated testing in any platform projects grow bigger over time and become complex. Making sure that all the tests are passing is a strong signal that the current requirement and all the previous requirements for this piece of your app have been delivered successfully and that nothing is breaking. Test driven development has many advantages. Here are a few with TDD, you are **minimizing regressions** that is accidental bugs introduced to old code by **coding a new requirement and you also have proof** that your new implementation is not breaking other parts of the app.

You can **automate these tests** easily and thus keep verifying again and again that the system works as expected. You can test your implementations with various inputs and the tests become a specific kind of **documentation** for the new members of your team.
