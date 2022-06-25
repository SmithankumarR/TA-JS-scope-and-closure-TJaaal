1. Convert the function below into different forms of function expression.

```js
function percentage(marks, total) {
  return (marks * 100) / total;
}


let percentage = ((marks,total) => (marks * 100 / total)) ;


```

2. Write Function Declaration or Function Expression next to the function.

```js
function percentage(marks, total) {
  return (marks * 100) / total;
}
// Your answer
let percentage = ((marks,total) => (marks * 100 / total)) ;

```

```js
let percentage = function (marks, total) {
  return (marks * 100) / total;
};
```

```js
let percentage = function (marks, total) {
  return (marks * 100) / total;
};
```

```js
let percentage = (marks, total) => {
  return (marks * 100) / total;
};
```

```js
let percentage = (marks, total) => (marks * 100) / total;
```

3. Why is a function definition an expression in JavaScript? Give one example of function expression.
ans --- 
A function definition expression defines a JavaScript function, and the value of such an expression is the newly defined function. In a sense, a function definition expression is a “function literal” in the same way that an object initializer is an “object literal.” A function definition expression typically consists of the keyword function followed by a comma-separated list of zero or more identifiers (the parameter names) in parentheses and a block of JavaScript code (the function body) in curly braces. 
```js
let isOdd = ((num) => num % 3 === 0);

4. Why is a function call an expression in JavaScript?

 
A function call expression is used to execute a specified function with the provided arguments. If the function being called is overloaded, the compiler will attempt to match the argument types with the function parameter types. If there are no matching function declarations, a compile-time error will be raised.
 ```js
//  First overload
int plus(int a, int b) {
    return a + b;
}
//  Second overload
int plus(int a, int b, int c) {
    return a + b + c;
}
 
Console.log(plus(1, 1));    // Calls first overload. Result: 2
Console.log(plus(1, 1, 1)); // Calls second overload. Result: 3
```
5. Write VALID and INVALID next to each example below with the reason.

```js
function add(a, b) {
  return a + b;
}

let five = add(2, 3); // valid
five = add; // invalid
five = five(10, 11); // valid
five = function () {
  return 'Hello';
}; // invalid
```

6. What is the difference between function definition and function call? Explain with an example.

function definition : is used to define the set of rules or tasks that need to be performed by defineing a name with required parameters.

function call : is used to call the defined function with the arguments given as value for the parameters defined in the function which helps to perform the task.
```js
function age(num){
  if(num >= 18){
    return `you are an Adult`;
  }
  else {
    return `you are still a child`;
  }
}  // function defination

age(24);  // function call
```
7. What is the similarities between function definition and function call?
function definationis used to build or perform the tasks.
function call is the complete the given tasks

8. Is the code below valid or invalid. Explain with reason.

```js
function hello() {
  console.log('Hello World!');
}

hello.user = 'Sam'; // valid 
```

9. What is higher order function explain with an example.

 A function that accepts other functions as arguments is called a higher-order function, which contains the logic for when the callback function gets executed. 

while calling a function we just need to refernce the name of the function 
``` js
const numbers = [1, 2, 3, 4, 5];

function addOne(array) {
  for (let i = 0; i < array.length; i++) {
    console.log(array[i] + 1);
  }
}

addOne(numbers);
```
10. Explain what is callback function. Why you can pass a function inside a function?
A callback function is a function that is passed as an argument to another function, to be “called back” at a later time. A function that accepts other functions as arguments is called a higher-order function, which contains the logic for when the callback function gets executed.

```js
 function createQuote(quote, callback){ 
  var myQuote = "Like I always say, " + quote;
  callback(myQuote); // 2
}

function logQuote(quote){
  console.log(quote);
}

createQuote("eat your vegetables!", logQuote); 
createQuote("eat your vegetables!", function(quote){ 
  console.log(quote); 
});
```