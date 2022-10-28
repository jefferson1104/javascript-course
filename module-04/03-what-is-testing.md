# What is testing?
When you're building something, you want to make sure it works, and you make sure that something works by testing it. It's the same with JavaScript code. You need to make sure that your JavaScript code works before you launch it. 

In this explanation, I'll show you how web developers test their JavaScript code. By the end of this explanation, you'll be able to:

- Identify why developers test their code
- Explain the red-gren-refactor cycle
- Differentiate between manual and automated testing
- Demonstrate an understanding of unit testing

###### How do web developers test their code?
Let's find out by coding a custom `concatStrings` function. For example, I can create a `concatStrings` function to join any two strings that I give it. In this case, I want the function to join `string A` and `string B` that are received as arguments, and return the result.
```js
function concatStrings(strA, strB) {
  return strA + strB;
}
```

For example, I could write `concatStrings` `a, b, c` and then `d, e, f` and the returned result would be `abcdef`. When the function receives number `1` and `2`, it returns a `3` as a number instead of a string of one and two together i.e, `1, 2`.
```js
concatStrings("abc","def");
// Result: "abcdef"

concatStrings(1,2);
// Result: 3 <--- oops!

concatStrings("world","wide");
// Result: "worldwide"

concatStrings("123","456");
// Result: "123456"
```

There are many custom testing frameworks available in JavaScript. One of the strengths of such frameworks is that I don't have to use comments to describe my expectations. The test syntax itself becomes expectation documenting. When I write tests, those tests are a better alternative to comments in my source code because they specify what expectations my source code is trying to satisfy. Tests are also callable, meaning I can execute tests to check if expectations are met.

As I demonstrated earlier, I could execute the `concatStrings` function with the first argument being the string `abc`, and the second argument, the string `def`. I would then expect the function to return `abcdef`, when I call it.

To write this as an expectation in some testing frameworks such as **JEST**, I can use the function that has the name expect. I then pass the call to the concatStrings function with the specific arguments. Then I add that to the function, which is another testing function, and I pass it the value of what I'm expecting this code to produce. I'm essentially stating that I expect the calling `concatStrings` with `abc` and `def`, will return the value `abcdef`.
```js
expect(concatStrings("abc", "def")).toBe("abcdef"); // passed
expect(concatStrings("123", "456")).toBe("123456"); // passed
```

Testing in JavaScript lets me verify that the function is behaving in the way I intended. Testing code in this way ensures three things. **Conciseness** as it's straightforward and to the point, since there are only two function calls to explain what is the expected result. **Clarity**, because you know exactly what arguments you're providing, and repeatability, as you can run it again and again with the same arguments each time. Now, I could run multiple function calls using this syntax. For example, I could have expected `concatStrings` `123` and `456` as arguments, and then the function to be with the argument `123456`, and in each instance, the expectations will be correct, and the code will behave as expected. In testing terminology, you would say that your tests are passing. But I'm only halfway there because it's still possible from my code to fail an expectation.

For example, if I run the expect method and pass it an invocation of the `concatStrings` function with numbers `1` and `2` as arguments, my expectation of `12` being the results will fail. This is because when I use the plus operator with two values of the number type, it performs the mathematical operation of addition, instead of joining the two numbers together to form the number `12`, like it would form abcdef.
```js
expect(concatStrings(1, 2)).toBe(12); 
// not passed, error because result is 3, because use number not string
```

If a test fails, then it's a sign that I need to write the code in such a way that it passes its test. Once my test passes, I need to improve both the app's code and the test code, but without changing the behavior of either. This is known as refactoring. Refactoring is the process in which I write my feature code so that it runs more efficiently or that it's easier to read and thus easier to understand for other programmers on the team. This is done without affecting the results that the code produces. The only obvious change should be perhaps the test itself taking less time to run because I've optimized my source code. You want to always write your code in a way that meets all expectations. It's most likely that some of your tests will be red and some of them will be green. Red tests are a guide as to how you need to improve your code to cater for unmet expectations. As you continue to refine your code in response to red tests, it becomes a cyclical activity. This is often described as the **red-green-refactor cycle**. This cycle is the basis of the **test-driven development** or **TDD** approach to programming.

Let me explain the **TDD** approach. First, you write a failing test, then you write your source code so that the previously failing test now passes. Finally, you optimize your source code without changing its results. There are many advantages of having code that tests other code. For example, you can run it as many times as you want. You can run the testing code automatically. The tests can be repeated without significant cost in time or effort. To sum up, testing is how you verify the expectations you have regarding the behavior of your code.
