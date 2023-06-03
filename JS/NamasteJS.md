# Namaste JavaScript

- [Namaste JavaScript](#namaste-javascript)
  - [How JavaScript Works \& Execution Context](#how-javascript-works--execution-context)
  - [How JavaScript Code is executed? \& Call Stack](#how-javascript-code-is-executed--call-stack)
    - [Call Stack](#call-stack)
  - [Hoisting in JavaScript (variables \& functions)](#hoisting-in-javascript-variables--functions)

## How JavaScript Works & Execution Context

- Everything in JavaScript happens inside an `Execution Context`
- Execution Context is divided into 2 Parts:

    |Memory|Code|
    |:---|:---|
    |It is also known as Variable Environment.|It is also known as Thread of Execution|
    |Here variables are divided into Key : Value pairs e.g a : 10, fn : {...}| Here code is evaluated line by line.|

- JavaScript is a `Synchronous` `Single threaded` language.
  - Synchronous: It can perform only one command at a time.
  - Single threaded: It can perform command only in a particular sequence. Once the previous command is completed.

---

## How JavaScript Code is executed? & Call Stack

```javascript
var n = 2;

functon square (num){
    var ans = num * num
    return ans;
}

var sq2 = square(n);
```

- When code is executed, JavaScript Gloabal Execution Context is created.
- Execution context is created in two phase :

  |Phase 1 : Memory creation phase|Phase 2 : Code execution phase|
  |:---|:---|
  |JS allocates memory to variables and function.|In this phase, JS goes through the whole code and assigns actual values|
  |It stores the undefined to variables. e.g: n = undefined , sq2 = undefined.| e.g: n=2, wherever function is called/invoked function execution context is created|
  |And in functions, it stores the whole code of function as a value. e.g: square{...} |This function execution context behaves like the global execution context.|

  - Arguments are the values given while calling the function
  - Parameters are the values given inside the ( ) while defining the function.
  - After whole code is executed Global Execution context is removed.

### Call Stack

- It manages creation and deletion of all the `execution context` including Global execution context
- All the function execution context are put over the Global execution context as soon as they appear in code. This forms a stack which is called call stack.
- Once the code is executed, the call stack gets empty.
- It maintains the order of execution of execution contexts.
- Call stack is also known as:
  - Execution Context Stack
  - Program Stack
  - Control Stack
  - Runtime Stack
  - Machine Stack

---

## Hoisting in JavaScript (variables & functions)
