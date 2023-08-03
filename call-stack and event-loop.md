This repository contains a simple JavaScript code snippet that demonstrates the concept of the call stack, event loop, and synchronous execution in JavaScript. The code provided showcases the order of execution of function calls and regular code statements.

## Code Explanation

The provided code consists of the following parts:

```javascript
console.log("Hello World!");
logger();
console.log(3);

function logger() {
  console.log(1);
  console.log(2);
}
```

1. `console.log("Hello World!");`: This line prints the message "Hello World!" to the console.

2. `logger();`: Here, the function `logger()` is called. When this happens, the `logger()` function is pushed onto the call stack.

### Call Stack

The call stack is a data structure in JavaScript that keeps track of function calls. When a function is called, it is pushed onto the call stack. When a function finishes executing, it is removed from the call stack.

In our code, the `console.log("Hello World!");` statement is the first to execute, and it is added to the call stack. Next, the `logger()` function is called, and it is also added to the call stack. When the `logger()` function finishes executing (after printing 1 and 2), it is removed from the call stack. Finally, the `console.log(3);` statement is executed and added to the call stack, followed by its removal after printing 3.

### Event Loop

JavaScript is a single-threaded language, which means it can only execute one piece of code at a time. However, it can handle asynchronous operations using the event loop. The event loop continuously checks if there are any asynchronous tasks waiting to be executed, and if so, it offloads those tasks to be executed outside the main thread. This allows non-blocking behavior in JavaScript.

In our code, there are no asynchronous tasks, so the event loop remains idle, and the code executes synchronously, line by line.

The chronological order of the execution is as follows:

1. "Hello World!" is printed.
2. `logger()` function is called and executed.
3. The numbers 1 and 2 are printed.
4. `console.log(3);` is executed, and the number 3 is printed.

---

Feel free to further customize the README if needed and add any other relevant information you may want to include. Once done, you can upload the README to your GitHub repository, and it will be visible on the repository's landing page.
