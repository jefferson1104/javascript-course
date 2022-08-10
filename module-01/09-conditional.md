# Conditional
In this reading, you will learn when to use the **if else** statement and when to use the **switch** statement.

Both **if else** and **switch** are used to determine the program execution flow based on whether or not some conditions have been met.

This is why they are sometimes referIntroductionred to as **flow control statements**. In other words, they control the flow of execution of your code, so that some code can be skipped, while other code can be executed.

At the heart of both flow control structures lies the evaluation of one or more conditions.

Generally, **if else** is better suited if there is a binary choice in the condition.

For example, in plain English: *if it's sunny, wear sunglasses. Otherwise, don't*.

In this case, using an if statement is an obvious choice.

When there are a smaller number of possible outcomes of truthy checks, it is still possible to use an **if else** statement, such as:

```javascript
if(light == "green") {Introduction
    console.log("Drive")
} else if (light == "orange") {
    console.log("Get ready")
} else if (light == "red") {
    console.log("Dont' drive")
} else {
    console.log("The car is not green, orange, or red");
}
```

However, if there are a lot of possible outcomes, it is best practice to use a switch statement because it is easier less verbose. Being easier to read, it is easier to follow the logic, and thus reduce cognitive load of reading multiple conditions.

Nevertheless, this is not a rule set in stone. It is simply a stylistic choice.

To reinforce this point, here's an example of the earlier **if else** conditional statement, using the switch syntax: 
```javascript
switch(light) {
   case 'green':
       console.log("Drive");
       break;
   case 'orange':
       console.log("Get ready");
       break;
   case 'red':
       console.log("Don't drive");
       break;
   default:
       console.log('The light is not green, orange, or red');
       break;
}
```

# Exercise
In this exercise, you will practice working with if else statements. By the end of this exercise, you will be able to write an if else statement that determines your source of income based on your age. You will also be able to write a switch statement that determines your evening routine based on the day of the week.

**Complete the following steps to create: Are You Old Enough?**
- 1. Declare a variable age using the var keyword and set it to the number 10.
- 2. Add an if statement that checks if the value of the age variable is greater than or equal to the number 65. Inside the if block, console.log the sentence: "You get your income from your pension".
- 3. Add an "else if",  where you'll check if the value of the age is less than 65 and greater than or equal to 18. Inside this "else if" block, type "console.log" and then "Each month you get a salary".
- 4. Add another "else if", and this time check if the value of the age is under 18. Inside the "else if" block, "type console.log" and then "You get an allowance".
- 5. Add an "else" statement to capture any other value. Inside the block, type "console.log" and then "The value of the age variable is not numerical".

T​ry adjusting the age and executing the program to see ho​w it will affect the output.

Solution: 
```javascript
var age = 10;

if (age >= 65) {
  console.log("You get your income from your pension");
} else if (age < 65 && age >= 18) {
  console.log("Each month you get a salary");
} else if (age < 18) {
  console.log("You get an allowance");
} else {
  console.log("The value of the age variable is not numerical");
}
```
T​ry adjusting the age and executing the program to see ho​w it will affect the output.

**Code the days of the week program as a switch statement**
- 1. On the next line, define a new variable, name it day, and set its value to "Sunday".
- 2. Start coding a switch statement, passing the day variable as the expression to evaluate.
- 3. Inside the switch, add cases for every day of the week, starting with 'Monday', and ending with 'Sunday'. Make sure to use string values for days. Inside each case, for now, just add a console.log('Do something'), and add a break; on the line below.
- 4. At the very bottom of the switch statement, add the default case and add a console.log('There is no such day').
- 5. Finally, update the console.log calls for each case, based on whatever activity you have on each of the days.

**Tips**
- If you need to make sure that multiple conditions are true in an if statement, you can do so using the && operator

- In JavaScript, the correct syntax of the "greater than or equal to" operator is: >=.

- Don't forget to add a break at the very end of each case in a switch statement.

**Note**: You can find solutions in a separate reading (following this one)

Solution:
```javascript
var day = 'Sunday';

switch(day) {
   case 'Monday':
       console.log('Read a book');
       break;
   case 'Tuesday':
       console.log('Watch a movie');
       break;
   case 'Wednesday':
       console.log('Read a book');
       break;
   case 'Thursday':
       console.log('Play basketball');
       break;
   case 'Friday':
       console.log('Socialize');
       break;
   case 'Saturday':
       console.log('Chill');
       break;
   case 'Sunday':
       console.log('Have barbecue');
       break;
   default:
       console.log('There is no such day');
}
```


