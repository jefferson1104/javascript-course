# Storing data in arrays
JavaScript has a piece of functionality that allows you to store and rearrange sequenced collections of items. This is called an array.

I'll guide you through how to build an array and access its contents. I'll also demonstrate how JavaScript stores the contents of the array and indexes its values.

Let's say that you want to emulate a toy freight train using JavaScript. On this train, each carriage has a number painted on its site and is presented in sequence, starting **from 0**. Using JavaScript, you'll assign some cargo to each carriage. For the first one, let's input var carriage 0 equals **wheat**.
You can use the same approach to model your entire train. Let's say you do just that and end up with five variables of different values. You've just built a train with five carriages, each holding different cargo. Now let's make things interesting and introduce a second train. This one only has two carriages with the number 0 and 1 painted on the sides. Seems pretty simple, right? Well, you can't use the variable names carriage0 and carriage1 because they're already taken. You could use more descriptive names, such as train2carriage0 and a train2carriage1 but that feels a bit wordy. Another problem is that you need to signal that these variables are a collection belonging Train 2. But when written this way, JavaScript doesn't understand that. Luckily, we can fix this. To make JavaScript understand that we will group a sequence of variables in a collection, we use arrays. You can build an array using the array literal syntax, which is an opening square bracket followed by a closing one. The array is currently empty, but JavaScript now understands that we would provide a collection of items. Let's assign that collection to the Train 1 variable. Finally, let's add carriages to the train 1 array by typing in the item names with each separated by a comma. Now we have a train. But what happened to the carriage numbers? Not to worry. Behind the scenes, JavaScript gives each item a number starting from 0 that corresponds to its place in the sequence. You can then use these numbers to access each carriage. For example, typing train1 followed by 0, encased in brackets will access the value inside carriage 0, which is wheat in this case. To summarize, arrays help us achieve several things in JavaScript. Arrays signal that the assigned values all belong to a group. These values are ordered in a sequence and each one can be accessed through its index number in that sequence. In this video, you learned how to build an array in JavaScript. You also learned how JavaScript sequences array items using an index value.


Example: 
```js
var train1 = ["wheat", "barley", "potato", "salt", "rocks"];

console.log(train1[0]);
// Output: wheat

console.log(train1[1]);
// Output: barley

console.log(train1[2]);
// Output: potato

console.log(train1[3]);
// Output: salt

console.log(train1[4]);
// Output: rocks
```