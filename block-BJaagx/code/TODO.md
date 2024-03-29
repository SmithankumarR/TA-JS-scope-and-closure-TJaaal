
1. Which all function is Higher order function and which one is a callback function in the code given below.

```js
let marks = [34, 45, 56, 76];
function multiplyArrayByN(arr, cb) {
  let finalArr = [];
  for (let elm of arr) {
    finalArr.push(cb(elm));
  }
  return finalArr;
}
function addFive(n) {
  return n + 5;
}
function multiplyBy5(n) {
  return n * 5;
}
let numbersAddedFive = multiplyArrayByN(marks, addFive);
let numbersMultipliedBy5 = multiplyArrayByN(marks, multiplyBy5);
```
as we already know that the HOF will always receives the call back function as the parameters so in the above code snippet function named `multiplyArrayByN` recives arr and cb as aruguments at the declaration phase and another function named `addFive` and `multiplyBy5` will be an call back function.


2. Create the execution context diagram of the above code snippet
![](../code/img/pic1.jpg);

3. Write a higher order function that accepts a number and a operation function (callback function). Call the callback function passing the number as argument and return the returned value.

```js
function operation(n, opFn) {
 return opFn(n);
}

// TEST
let  numbersDividedByFive = console.log(
  operation(21, function (n) {
    return n / 10;
  })
);
// Output: 2.1
let  numbersMultiplyAndDividedByFive = console.log(
  operation(10, function (n) {
    return (n * n) / 5;
  })
);
// Output: 20
```

4. Write a higher order function that accepts a string and a operation function (callback function). Call the callback function passing the string as argument and return the returned value.

```js
function operation(str, opFn) {
  return opFn(str);
}
// TEST
let uppercaseString =console.log(
  operation("Learning to fly", function (text) {
    return text.toUpperCase();
  })
);
// Output: "LEARNING TO FLY"
let splittedString = console.log(
  operation("Higher Order Fucntion", function (text) {
    return text.split(" ");
  })
);
// Output: ["Higher","Order","Function"]
```
