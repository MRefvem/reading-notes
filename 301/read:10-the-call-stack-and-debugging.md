# Read:10 - The Call Stack and Debugging

## Understanding the JavaScript call stack
[www.freecodecamp.org](https://www.freecodecamp.org/news/understanding-the-javascript-call-stack-861e41ae61d4/)

The JavaScript engine, is a single-threaded interpreter comprising of a heap and a single call stack. The call stack is primarily used for function invocation (call). Since the call stack is single, functions execution, is done one at a time, from top to bottom. The stack is synchronous.

Asynchronous JavaScript is when you have a callback function, an event loop or a task queue. The callback function is acted upon by the call stack udring execution after the call back function has been pushed to the stack by the event loop.

The call stack is a data structure that uses the Last In, First Out (LIFO) principle to temporarily store and manage function invocation.