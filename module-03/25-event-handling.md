# Event handling
Let's say you are using a webpage on your computer and you click a button, or you tap the like icon on a friend's picture on your phone. In JavaScript, the button click and the like icon tap are examples of user triggered events. Events are happening all the time. You can use JavaScript code to listen for these events. You can even choose the parts of the page on which you are listening for events. In JavaScript, the function that handles captured events is known as the **event handler**. 

### Example
Let me demonstrate how to listen foreign event by using the add **event listener method**.

```js
const target = document.querySelector('body');

function handleClick() {
  console.log('clicked the body');
}

target.addEventListener('click', handleClick);
```

![example this code](https://i.ibb.co/KqWd2cn/Screen-Shot-2022-10-26-at-21-36-09.png)

### Explaining: 
One of the easiest ways to listen for an event is to use the add **event listener method**. You can do that on a given HTML element. For example, suppose I want to listen to the **click event** on the **body** of this example website. First, I need to get a reference to the **body element** where we want to listen to this event.

In the **console** of the browser developer tools, I type `document.queryselector`, and then the name of the element inside of the parenthesis. For this example, its **body**, and I enclose it with single quotes. Next, I want to assign the body object to a variable. I type const target equals to assign the body object to the `target` variable. I've named this variable `target` because it's the target of our click event. 
```js
const target = document.querySelector('body');
```

Now I can create a function that would be run when this target is clicked. I type function `handleClick`, and then in the function **body**, I **console log** the string, **clicked the body**.
```js
function handleClick() {
  console.log('clicked the body');
}
```

The next step is to run the `addEventListener` method on the target element. I type `target.addEventListener()`. Then inside the parenthesis, I pass it two arguments. The first is the event type `click` as a string value, and the second is my `handleClick` function.
```js
target.addEventListener('click', handleClick);
```

Okay, so my code is now ready. Let me test it by clicking the webpage. Success. Notice that the text is output to the console. 

### Other example
In addition to the addEventListener method, an alternative way to listen for events is by using HTML event attributes.

Let me first write a second click handler function named handleClick2. Once again, I console log a string inside the function body. This time it will output the phrase clicked the heading.
```js
function handleClick2() {
  console.log('clicked the heading');
}
```

In HTML
```html
<h1 onClick="handleClick2()">Example Domian</h1>
```

![example 02](https://i.ibb.co/dm41m5W/Screen-Shot-2022-10-26-at-21-54-58.png)