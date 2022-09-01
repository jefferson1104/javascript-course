# Exercise: Error prevention

**Instructions**

**Task 1: Code a function declaration**
You need to code a function declaration named **addTwoNums**, which accepts numbers **a** and **b** and console logs **a + b**.

**Task 2: Invoke the addTwoNums function with a number and a string**
You need to invoke the **addTwoNums** using the following arguments: **5** and **"5"**.

**Task 3: Update the addTwoNums function with a try...catch block**
Add the try and catch blocks inside the function definition's body. For now, just make sure that the console log of **a + b** is inside the try block. Additionally, the **catch** block should catch an error named **err** and, inside the body of the **catch** block, you need to console log the **err** value.

**Task 4: If the passed-in arguments are not numbers, throw an error**
If either of the arguments passed to the **addTwoNums** are not numbers, you'll throw an error.

Specifically, code a conditional with the following logic:

- if the **typeof** the **a** parameter is not equal to **'number'**, throw a new **ReferenceError**. Inside the **ReferenceError**, pass a custom error message of **'the first argument is not a number'**.

- else if the **typeof** the **b** parameter is not equal to **'number'**, throw a new **ReferenceError**. Inside the **ReferenceError**, pass a custom error message of **'the second argument is not a number'**.

- else, console log **a + b** 

Once you've completed this task, all the code inside the **try** block will be inside these conditional statements.

**Task 5: Update the catch block**
Inside the catch block, update the code from **console.log(err)** to **console.log("Error!", err)**.

**Task 6: Invoke the addTwoNums function**
Invoke the **addTwoNums** function using **5** and **"5"** as arguments.

**Task 7: Add another console log under the addTwoNums function invocation**
Add another line of code that console logs the string **"It still works"**.

SOLUTION:
```javascript
function addTwoNums(a, b) {
  try {
    if (typeof(a)  != 'number') {
      throw new ReferenceError('the first argument is not a number');
    } else if (typeof(b) != 'number') {
      throw new ReferenceError('the second argument is not a number')
    } else {
      console.log(a + b)
    }
  } catch (error) {
    console.log("Error: ", error);
  }
}
  
addTwoNums(5, "5");
console.log("It still works");
```

# Exercise: Defensive programming
Defensive programming is all about assuming that all the arguments a function will receive are of the wrong type,  the wrong value or both.

In other words, you are assuming that things will go wrong and you are proactive in thinking about such scenarios before they happen, so as to make your function less likely to cause errors because of faulty inputs.

How would you then refactor the function given below with defensive programming in mind?

For this exercise, let's make sure that both of the arguments that are passed in satisfy the following criteria:

- The length of the **word** parameter cannot be less than **2**.

- The length of the **match** parameter must be **1**.

- The type of both the **word** and the **match** parameters must be string.

You will use the code below to complete your task:
```javascript
function letterFinder(word, match) {
    for(i = 0; i < word.length; i++) {
        if(word[i] == match) {
            console.log('Found the', match, 'at', i)
        } else {
            console.log('---No match found at', i)
        }
    }
}
```
Here are the tasks to complete:

1 - Just above the **for** loop in the **letterFinder** function definition, declare a variable named **condition1** and assign to it the following code: **typeof(word) == 'string' && word.length >= 2**.

2 - Declare a variable named **condition2** on the next line and assign to it and assign to it a check that makes sure that the type of **match** is a string AND that the length of the **match** variable is equal to **1**.

3 - Write an if statement on the next line that checks that **condition1** is **true**, and **condition2** is **true**

4 - Move the rest of the function's body into the if statement you wrote in the previous step.

5 - Code an "else" block after the "if" condition and console.log the following: **"Please pass correct arguments to the function."**.

6 - As a failing test, run the letterFinder function and pass it with any two numbers as arguments.

7 - As a passing test, run the **letterFinder** function and pass it with correct arguments, such as: **letterFinder("cat", "c")**.

SOLUTION:
```javascript
function letterFinder(word, match) {
    var condition1 = typeof(word) == 'string' && word.length >= 2;
    var condition2 = typeof(match) == 'string' && match.length == 1;

    if (condition1 && condition2) {
        for(i = 0; i < word.length; i++) {
            if(word[i] == match) {
                console.log('Found the', match, 'at', i)
            } else {
                console.log('---No match found at', i)
            }
        }
    } else {
        console.log("Please pass correct arguments to the function.")
    }
}


letterFinder(2, 3);
letterFinder('cat', 'c')
```


