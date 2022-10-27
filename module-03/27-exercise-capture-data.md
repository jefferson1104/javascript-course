# Exercise: Capture Data

### Description
The aim of this exercise is to access the content of an element, specifically to use a button click to replace text.

### Task 1: The example.com website
Open the example.com website in your browser. Open the developer tools and focus on the Console tab.

### Task 2: Get h1 into a variable
Use the `document.querySelector()` method to query the `h1` element on the page and assign it to the variable named `h1`.

### Task 3: Code an array
Declare a new variable, name it `arr`, and save the following array into it:

```json
[
    'Example Domain',
    'First Click',
    'Second Click',
    'Third Click'
]
```

### Task 4: Write a click-handling function
Write a new function declaration, named `handleClicks`. It should not accept any parameters.

Inside of it, code a `switch` statement, and pass a single parameter to it, `h1.innerText`.

The body of the switch statement should have a total of 4 cases (the fourth being the default case).

The first case should start with `case arr[0]:`. It should set the `h1.innerText` to `arr[1]`. In other words, it should assign the value of `arr[1]` to the `h1.innerText` property. The next line should have only the `break` keyword.

The second case should start with case `arr[1]`:. It should set the `h1.innerText` to `arr[2]`. In other words, it should assign the value of `arr[2]` to the `h1.innerText` property. The next line should have only the `break` keyword.

The third case should start with case `arr[2]`:. It should set the `h1.innerText` to `arr[3]`. In other words, it should assign the value of `arr[3]` to the `h1.innerText` property. The next line should have only the `break` keyword.

The default case should set the value of the h1.innerText property to arr[0].

### Task 5: Add an event listener
You've created an `h1` variable in Task 2. Now, use that variable to run the `addEventListener()` method on it. Pass two arguments to the `addEventListener()` method: `'click'` and `handleClicks`.

# Solution

### Task 1 solution: The example.com website
Open your favorite browser and navigate to https://example.com/.

Next open its developer tools using either the F12 key, or right-clicking onto the page and selecting the contextual menu's Inspect command, or by pressing CTRL SHIFT I or COMMAND SHIFT I.

Next, click on the Console tab to open it in a dedicated tab, or press the ESC key to have the console open while any tab is in focus.
![open devtools](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/RnsUC_7NRI27FAv-zQSNaA_0b84f6a9402149439f90d7918fe98de1_example.com-dev-tools.png?expiry=1667001600000&hmac=ArZjb4niai227WW0pLEmneDdAjEh1dUCIX6gqAvmuHo)

### Task 2 solution: Get h1 into a variable
```js
var h1 = document.querySelector('h1')
```

### Task 3 solution: Code an array
```js
var arr = [
    'Example Domain',
    'First Click',
    'Second Click',
    'Third Click'
]
```

### Task 4 solution: Write a click-handling function
```js
function handleClicks() {
    switch(h1.innerText) {
        case arr[0]:
            h1.innerText = arr[1]
            break
        case arr[1]:
            h1.innerText = arr[2]
            break
        case arr[2]:
            h1.innerText = arr[3]
            break
        default:
            h1.innerText = arr[0]
    }
}
```

### Task 5 solution: Add an event listener
```js
h1.addEventListener('click', handleClicks);
```

An example of the solution being run in the browser:

[video example](https://d3c33hcgiwev3.cloudfront.net/PCWG5YEXTuulhuWBFz7roA.processed/full/360p/index.mp4?Expires=1667001600&Signature=P53utQZ08SlI~Cy3kAlijd63~TbtXQfLvh7PWkZa43WYeJRlgRu2jw6RMSFDNRBmiimnYp8OjJa6kDnVL0nx5IEvih2IiuwJAYsXkiK5GXDW0PW8znJqNg0dW1WGeLLkf8VmEIcbQlrCXmR1fPIqaFmiSlgWftpNHf392Vyw9KU_&Key-Pair-Id=APKAJLTNE6QMUY6HBC5A)