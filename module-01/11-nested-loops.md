# Nested loops

### Examples
```javascript
// Week  1 day1
// Week  1 day2
// Week  1 day3
// Week  1 day4
// Week  1 day5
// Week  2 day1
// Week  2 day2
// Week  2 day3
// Week  2 day4
// Week  2 day5

for (var i = 1; i <= 2; i++) {
  for (var j = 1; j <= 5; j++) {
    console.log("Week ", + i + " day" + j);
  }
}
```

Other example
```javascript
for (var year = 2023; year < 2025; year++) {
  console.log(year);
  for (var month = 6; month < 9; month++) {
    console.log(".......", month);
  }
}
```

Other example
```javascript
for (var firstNum = 0; firstNum < 2; firstNum++) {
  for (var secondNum = 0; secondNum < 10; secondNum++) {
    console.log(firstNum + ", " + secondNum);
  }
}
```

Other example
```javascript
for (var firstNum = 0; firstNum < 2; firstNum++) {
  for (var secondNum = 0; secondNum < 10; secondNum++) {
    console.log(firstNum + " times " + secondNum + " equals " + firstNum * secondNum);
  }
}
```