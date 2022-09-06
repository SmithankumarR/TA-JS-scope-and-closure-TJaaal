Find the output of the code snippets below:

```js
console.log(numA + numB); // NAN
var numA = 21,
  numB = 30;
```
first after the declaration phase console will be executed hence both values are undefined results with NAN

Find the output of the code snippets below:

```js
console.log(numA + numB); // numA is not defined
let numA = 21,
  numB = 30;
```
while execution phase it checks the argumets are decalred or not hence it results with error numA is not defined

Find the output of the code snippets below:

```js
let numA = 21,
  numB = 30;
console.log(numA + numB); // 51
```
after decalration phase the both variables got created and assigned with the specified values and excute them with the output value of 51

Find the output of the code snippets below:

```js
console.log(sayHello()); // Hello
function sayHello() {
  console.log("Hey");
}
function sayHello() {
  console.log("Hello");
}
```
after the decalration phase the function named `sayHello` which displays the console log of hey and again override with the lastest console statememt and while excution phase it checks lastest statement and prints the value Hello

Find the output of the code snippets below:

```js
let username = "Tyrion";
sayHello(); // Tyrion
function sayHello() {
  console.log(username);
}
```
while the decalration phase the variable created using let has no value and next at the time of execution phase value will be assigned to that variable and excute the function sayHello and prints the value of the username

Find the output of the code snippets below:

```js
sayHello(); // username is not defined
let username = "Tyrion";
function sayHello() {
  console.log(username);
}
```

while the decalration phase the variable created using let has no value and next at the time of execution phase function call will happen hence it displays the error of username is not defined



Find the output of the code snippets below:

```js
let username = "Tyrion";
sayHello(); // sayHello is not defined

let sayHello = () => {
  console.log(username);
};
```
while declaration phase the username has no value but  at the time of the execution phase here the function call searches for the function but there is no function it will be function expression hence it shows an error like sayHello is not defined

Find the output of the code snippets below:

```js
sayHello(); // sayHello is not defined
let username = "Tyrion";
let sayHello = () => {
  console.log(username);
};
```
while declaration phase the username has no value  but at the time of the execution phase here the function call searches for the function but there is no function it will be function expression hence it shows an error like sayHello is not defined

Find the output of the code snippets below:

```js
sayHello(); // sayHello is not defined
var username = "Tyrion";
let sayHello = () => {
  console.log(username);
};
```
while declaration phase the username has undefined but at the time of the execution phase here the function call searches for the function but there is no function it will be function expression hence it shows an error like sayHello is not defined

Find the output of the code snippets below:

```js
var username = "Tyrion";
sayHello(); // sayHello is not defined
let sayHello = () => {
  console.log(username);
};
```
while declaration phase the username has undefined but at the time of the execution phase here the function call searches for the function but there is no function it will be function expression hence it shows an error like sayHello is not defined

Find the output of the code snippets below:

```js
var username = "Tyrion";
let sayHello = () => {
  console.log(username);
  var username = "John";
};
sayHello(); // undefined
```
while the decalration while the variable `username` will be undifinied but the at the time of execution phase it has the another varible declared with undefined value hence at that time function wil be called  the output will be the undefined.

Find the output of the code snippets below:

```js
var username = "Tyrion";
let sayHello = () => {
  var username = "John";
  console.log(username);
};
sayHello(); // John
```
while the decalration while the variable `username` will be undifinied but the at the time of execution phase it has the another varible declared with `John` value hence at that time function wil be called  the output will be the `John`.

Find the output of the code snippets below:

```js
var username = "Tyrion";
let sayHello = () => {
  console.log(username);
  let username = "John";
};
sayHello(); // OUTPUT
```
while the decalration while the variable `username` will be undifinied but the at the time of execution phase it has the another varible declared with `Tyrion` value hence at that time function wil be called  the output will be the error saying like can't access the username before intialization.
