# JavaScript Variables

## Introduction
In JavaScript, variables are used to store data values. You can declare a variable using the `var`, `let`, or `const` keyword. This README will cover the basics of variable declaration, initialization, and usage with examples and their outputs.

## Variable Declaration and Initialization

### Using `var`
The `var` keyword is used to declare a variable globally or locally to a function regardless of block scope.

```javascript
var x = 5;
console.log(x); // Output: 5
```
### using `let`
The `let` keyword declares a block-scoped variable, optionally initializing it to a value.

```javascript
let y = 10;
console.log(y); // Output: 10
```
### using `let`
The `let` keyword declares a block-scoped variable, optionally initalizing it to a value

```javascript

let y = 10;
console.log(y); // Output: 10

```
### Using const
The `const` keyword declares a block-scoped, read-only named constant.

```javascript
const z = 15;
console.log(z); // Output: 15
// z = 20; // This will throw an error because z is a constant
```
#### Variable Scope

### Global Scope
Variables declared outside any function are in the global scope.

```javascript
var globalVar = "I'm global";

function checkScope() {
  console.log(globalVar); // Output: I'm global
}
checkScope();
```
### Function Scope
Variables declared inside a function are in the function scope.

```javascript
function localScope() {
  var localVar = "I'm local";
  console.log(localVar); // Output: I'm local
}
localScope();
// console.log(localVar); // This will throw an error because localVar is not defined outside the function
```
### Block Scope
Variables declared with let or const inside a block (denoted by {}) have block scope.

```javascript
{
  let blockVar = "I'm block-scoped";
  console.log(blockVar); // Output: I'm block-scoped
}
// console.log(blockVar); // This will throw an error because blockVar is not defined outside the block
```
#### Variable Hoisting
JavaScript hoists declarations (not initializations) to the top of their scope.

### var Hoisting
```javascript

console.log(hoistedVar); // Output: undefined
var hoistedVar = "I'm hoisted";
```
### let and const Hoisting
Variables declared with let and const are hoisted but not initialized.

```javascript

// console.log(hoistedLet); // This will throw an error because hoistedLet is in the temporal dead zone
let hoistedLet = "I'm also hoisted";

// console.log(hoistedConst); // This will throw an error because hoistedConst is in the temporal dead zone
const hoistedConst = "I'm const hoisted";
```
##### Summary
<li>Use var for function-scoped variables (though let and const are generally preferred in modern JavaScript).
<li>Use let for block-scoped variables that may change.
<li>Use const for block-scoped variables that should not change.
<li>Be aware of variable hoisting and scope to avoid common pitfalls.

