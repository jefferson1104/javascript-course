# Looping constructs

## For loop examples
```javascript
for (var i = 1; i <= 3; i++) {
  console.log(i);
}
console.log('Go');
```
```javascript
for (var i = 10; i > 0; i--) {
  console.log(i);
}
console.log('Happy New Year!');
```

## While loop examples
The while loop is quite similar to the for loop but they're not exactly the same. The first major difference is the counter value. With a while loop this is set before the loop and must be clearly defined. Let me demonstrate this now.
```javascript
var counter = 3;

while (counter > 0) {
  console.log(counter);
  counter = counter - 1;
}
```

# Exercises

### task 1
Write a "for" loop that will perform exactly the same repetitive code as this:
```javascript
console.log(1);
console.log(2);
console.log(3);
console.log(4);
console.log(5);
console.log('Counting completed!');
```

Solution:
```javascript
for (var i = 1; i <= 5; i++) {
  console.log(i);
}
console.log('Counting completed!');
```

### task 2
Write a "for" loop that will perform exactly the same repetitive code as this:
```javascript
console.log(5);
console.log(4);
console.log(3);
console.log(2);
console.log(1);
console.log('Countdown finished!');
```

Solution:
```javascript
for (var i = 5; i > 0; i--) {
  console.log(i);
}
console.log('Countdown finished!');
```

### task 3
Write a "while" loop that will perform exactly the same repetitive code as this:
```javascript
console.log(1);
console.log(2);
console.log(3);
console.log(4);
console.log(5);
console.log('Counting completed!');
```

Solution:
```javascript
var counter = 1;

while (counter < 6) {
  console.log(counter);
  counter++;
}
console.log('Counting completed!');
```

### task 4
Write a "while" loop that will perform exactly the same repetitive code as this:
```javascript
console.log(5);
console.log(4);
console.log(3);
console.log(2);
console.log(1);
console.log('Countdown finished!');
```

Solution:
```javascript
var countdown = 5;

while (countdown > 0) {
  console.log(countdown);
  countdown = countdown - 1;
}
console.log('Countdown finished!');
```

### task 5
Write a "while" loop that will perform exactly the same repetitive code as this:
```javascript
console.log(2018);
console.log(2019);
console.log(2020);
console.log(2021);
console.log(2022);
```

Solution:
```javascript
var year = 2018;
while (year < 2023) {
    console.log(year);
    year++;
};
```