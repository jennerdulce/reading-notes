# Callstack and Debugging

## Javascript Call Stack
- the call stack is a mechanism for the interpreter(VS Code in our case)
  - to keep track of its place in a script, that calls multiple functions
  - what function is being ran
  - what functions are called from what functions
- Browser
  - single threaded interpreter
  - heap and single call stack
  - browser provides API, DOM, AJAX, Times
- Understanding the call stack will give clarity to how "function hierarchy and execution order" works in JS engine
- Call stack is used for function invocation
  - Single stack: functions execute is done 1 at a time from top-to-botto
  - call stack is SYNCRONOUS
- Understanding call stack is vital to asynchronous programing
- AsynJS
  - callback functions
  - event loops
  - task queue

- What is the call stack?
  - Last in, first out
  - teporarly store and manage function invocation calls
  - a function is added to the call stack and is only popped off the call stack when the function has completed all of the code in the function
  - ex: in a grocery store, you cannot be helped until the person in front of you has been helped
- stack overflow happend when the callstack is overloaded with infinite number of functions and will result in an error

### Summary
- starts with an empty call stack
- invoking functions add them to the stack
- once all of the code in a function is ran, remove the function from the call stack
1. single threaded: one thing at a time
2. synchronous
3. function invocation creates a stack that temporarily occupies memory
4. last in, first out

## Debugging
- errors:
  -reference, syntax, range
- always console.log() to find bugs
- can use the line `'debugger'` in any part of your code  
  - using this line will display a call stack in the terminal
- [object Object] means that the object was turned into a string and is no longer an object
- `console.table()` if used on an object with properties, will give you a visual table representation on the terminal
- `try .. catch(error)` sort of like a if else statement,
  - if you make an error, code will continue to run without problems
  ```
  try {
  // code block
  }
  
  catch(error){
  console.error(error);
  return default_value_you_choose
  }
  ```
