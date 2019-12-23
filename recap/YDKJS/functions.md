# Functions

Function is a collection of statements that can be invoked one or more times, maybe provided some inputs, and may give back one or more outputs.

## Function Declaration & Function Expression
```js
// Function Declaration
function awesomeFunction(coolThings) {
  // ...
}

// Function Expression
let awesomeFunction = function(coolThings) {
  // ...
}
```

Function declaration appears as a statement by itself, not as an expression that's part of another statement.
The association between the identifier `awesomeFunction` and *the function value happens immediately during the compile phase of the code, before that code is executed.*

Function expression can be defined and assigned. *Function expression is not associated with its identifier until that statement during runtime.*
