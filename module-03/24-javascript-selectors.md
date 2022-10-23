# JavaScript Selectors
One of the most powerful features of JavaScript is **DOM** manipulation. For example, you can click on a button and change the color of some text or even display a pop up message. Essentially, you're dynamically updating the **HTML** content in real time. To do this, you must be able to locate the objects in your html document that you want to manipulate.

I'll guide you through how to use selectors in JavaScript to quickly find specific objects in a document. JavaScript selectors work with the document object which you can access by typing the keyword `document`. This returns the webpage stored in the browser's memory known as the document object model or DOM. Let's start locating specific elements inside the document object using the query selector method.



For example, I know this page contains two HTML paragraph elements, to access the first one I typed document.queryselector. Then in single quotes inside of the parentheses, I typed the letter `p`, when I press enter to run the command, it returns the first `p` element.
```js
  document.querySelector('p');
```

This method can be used with other html elements, such as the anchor tag. If I run the same command with the letter `a`, I get back the first anchor element on the page. 
```js
  document.querySelector('a');
```

There is a very similarly named JavaScript selector that allows me to get all the matches from a web page. It's the query selector all method, to demonstrate this, I type `document.querySelectorAll`. Inside the parentheses, I passed the `p` letter as a string and indeed I get back a result that shows that there are two paragraph tags on this page.
```js
  document.querySelectorAll('a');
```

Another useful JavaScript selector is `getElementById` which can find objects in the dawn that match a specified html ID attributes. For example, let's say we want to find something on this page with the idea of heading, I typed `document.getElementById`  and then the string heading in parentheses, I press enter and notice that an `h1`, element is returned assigned with the html ID attribute value of heading. 
```js
  document.getElementById('heading');
```

Next, let's use a similar method that returns an element based on a specified class name rather than ID. We can do this by calling `document.getElementsByClassName`. I typed `document.getElementsByClassName` and then the string txt and parentheses.
```js
  document.getElementsByClassName('txt');
```

Print screen example:
![example image](https://i.ibb.co/HpRLwJP/Screen-Shot-2022-10-23-at-12-26-17.png)

You learned how to use JavaScript selectors to speed up the process of finding specific objects in a document.