Go through the code below and write down the process of making decision about looking for the variable. Also write the output of the code below.

Example:

```js
function hello() {
  var username = 'Arya';
}
console.log(useranme); // output
```

In above code we are looking for the variable named `usename`. There is no variable named `username` in the global scope. The variable is inside the function named `hello` and we can't access the variable defined inside a function from outside.

The above code will throw an error `Reference Error username is not defined`.

2. Go through the code below and write down the process of making decision about looking for the variable. Also write the output of the code below.

```js
{
  const username = 'Arya';
}
console.log(useranme); // output
```
In above code we are looking for the variable named `username`. There is no variable named `username` in the global scope. The variable is inside the  scope and we can't access the variable defined inside a  scope from outside.

The above code will throw an error `Reference Error usernanme is not defined`.

3. Go through the code below and write down the process of making decision about looking for the variable. Also write the output of the code below.

```js
if (true) {
  let username = 'Arya';
}
console.log(username); // output
```
In above code we are looking for the variable named `username`. There is no variable named `username` in the global scope. let creates a scope  The variable is inside the block scope and we can't access the variable defined inside a block scope from outside.

The above code will throw an error `Reference Error usernanme is not defined`.


4. Go through the code below and write down the process of making decision about looking for the variable. Also write the output of the code below.

```js
if (true) {
  var username = 'Arya';
}
console.log(username); // Arya
```
actually var doesnt create a scope in the block scope hence it act has variable declared in global scope 


The above code will show ' Arya'

5. Go through the code below and write down the process of making decision about looking for the variable. Also write the output of the code below.

```js
let username = 'John';
if (true) {
  var username = 'Arya';
}
console.log(username); // output
```
here let creates block scope but var doesnt create hence the variable name will declared same both it shows an error
The above code will throw an error `SyntaxError Error usernanme has already been declared `.

6. Go through the code below and write down the process of making decision about looking for the variable. Also write the output of the code below.

```js
let username = 'John';
if (true) {
  let username = 'Arya';
}
console.log(useranme); // John
```
in these code let creates block scope but first one  `username` will be the global scope hence the another one  `username` act as block scope the console prints john as output



7. Go through the code below and write down the process of making decision about looking for the variable. Also write the output of the code below.

```js
let username = 'John';
function sayHello() {
  let username = 'Arya';
}
sayHello();
console.log(useranme); // John

```
in these code let creates block scope but first one `username` will be the global scope hence the another one  `username` act as block scope the console prints john as output function sayHello doesnt play impact in it becauses the function execution context gets deleted after the execution

8. Go through the code below and write down the process of making decision about looking for the variable. Also write the output of the code below.

```js
for (var i = 0; i < 10; i++) {
  console.log(i, 'First'); // output
}
console.log(i, 'Second'); // 
//  0 'First'
//  1 'First'
//  2 'First'
//  3 'First'
//  4 'First'
//  5 'First'
//  6 'First'
//  7 'First'
//  8 'First'
//  9 'First'
//  10 'Second'
```
In above code the var doesn't creates the scopes it goes through the condition checks the condition and iterate aover it until the condition become false .

9. Go through the code below and write down the process of making decision about looking for the variable. Also write the output of the code below.

```js
for (let i = 0; i < 10; i++) {
  console.log(i, 'First'); // 
  //  0 'First'
//  1 'First'
//  2 'First'
//  3 'First'
//  4 'First'
//  5 'First'
//  6 'First'
//  7 'First'
//  8 'First'
//  9 'First'
}
console.log(i, 'Second'); // reference error i is not defined.
```
In above code the let creates the block scopes and works the given condition and also iterate over the condition until the condition becomes false  after that it shows an error like i is not defined