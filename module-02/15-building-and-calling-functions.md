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

1. the starting loop counter value as a temporary variable `i` 

2. the exit condition (the maximum value of the loop counter variable `i`, above which the loop no longer runs) 

3. how to update the value of `i` after each loop

Here's the information I'll use in this function declaration: 1. The loop's starting counter will be `0`. The reason for setting it to zero is due to the fact that arrays are also counted from zero. 

This means that I'll have a one-to-one mapping of the current value of the i variable at any given time, corresponding to the same index position of any item in the `arr` array 2.

The for loop's exit condition is when the value of `i` is equal or greater than `arr.length`. 

Since the `arr.length` counts the number of items in the array from one, and the array items are indexed from zero, this effectively means that as soon as `i` is equal to `arr.length`, the loop will finish and any other code after it will be run. 

This practically means that the exit condition for this for loop will be `i < arr.length` returning `false`. 

In other words, as long as `i < arr.length` is true, this for loop will continue to run. 3. To make sure that none of the items in the `arr` array are skipped, I have to increase the value of `i` by `1` after each loop.

Now that I know exactly how my for loop should behave, I can add it to my `listArrayItems()` function:
```javascript
function listArrayItems(arr) {
    for (var i = 0; i < arr.length; i++) {
        // ... code pending here ...
    }
}
```
Now all that I have left to decide is how I want to output each item from the received `arr` array.

It can be as simple as console logging the array item index of the current value of `i`:
```javascript
function listArrayItems(arr) {
    for (var i = 0; i < arr.length; i++) {
        console.log(arr[i])
    }
}
```

If I now invoke the `listArrayItems` function, I can, for example, give it the following array of colors:  
```javascript
var colors = ['red', 'orange', 'yellow', 'green', 'blue', 'purple', 'pink'];
listArrayItems(colors);
```

The output will be:  
```bash
red
orange
yellow
green
blue
purple
pink
```

I can update the output any way I like. For example, here are my `arr` items with a number in front of each item:  
```javascript
function listArrayItems(arr) {
    for (var i = 0; i < arr.length; i++) {
        console.log(i, arr[i])
    }
}

var colors = ['red', 'orange', 'yellow', 'green', 'blue', 'purple', 'pink'];

listArrayItems(colors);
```

Now the output of the above code will be as follows:  
```bash
0 'red'
1 'orange'
2 'yellow'
3 'green'
4 'blue'
5 'purple'
6 'pink'
```

To start the count from one instead of zero, I can update my function declaration as follows:  
```javascript
function listArrayItems(arr) {
    for (var i = 0; i < arr.length; i++) {
        console.log(i+1, arr[i])
    }
}
```

Invoking the above, updated, function declaration on my `colors` array, will now result in the following output:  
```bash
1 'red'
2 'orange'
3 'yellow'
4 'green'
5 'blue'
6 'purple'
7 'pink'
```

I can even add one or more conditions, such as:  
```javascript
function listArrayItems(arr) {
    for (var i = 0; i < arr.length; i++) {
        if (arr[i] == 'red') {
            console.log(i*100, "tomato!")
        } else {
            console.log(i*100, arr[i])
        }
    }
}
```

Now I'm adding control flow right inside my function, based on whether a specific array member matches a specific value - in this case the string `"red"`.

Invoking my newest updated version of the `listArrayItems` function on the `colors` array will now result in the following output:
```bash
0 'tomato!'
100 'orange'
200 'yellow'
300 'green'
400 'blue'
500 'purple'
600 'pink'
```
