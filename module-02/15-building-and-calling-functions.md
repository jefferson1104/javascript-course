# Building and calling functions
In this reading, you will learn how to build and call a function. The purpose of this reading is to provide you with an example of function declaration (build) and function invocation (call). In the next lesson you will be writing the code.

By the end of this reading you should be able to:

- Code simple functions that can accept an array and iterate through it

Let's start with giving our function declaration a name:
```javascript
function listArrayItems(arr) {
    // ... code to be added ...
}
```
So, I've declared a **listArrayItems** function, and I've set it up to accept a single parameter, `arr` - which stands for an array.

Now, I'll need to code a for loop to loop over an array.

As covered in previous lessons in this course, a for loop needs the following information: 

1. the starting loop counter value as a temporary variable i 

2. the exit condition (the maximum value of the loop counter variable i, above which the loop no longer runs) 

3. how to update the value of i after each loop