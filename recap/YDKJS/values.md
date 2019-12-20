# Values in JS
Values are data. Values come in two forms in JS: primitive and object.

## Primitive values
1. Strings
2. Numbers
3. Booleans
4. null
5. undefined
6. Symbols

## Objects
1. Functions - special type (sub-type) of object.
2. Arrays - special type (sub-type) of object that's comprised of an ordered and numerically indexed list of data.
3. Objects - unordered, keyed collection of any various values.

## Values Type Determination -- typeof
```js
typeof 21;                    // "number"
typeof 'hello';               // "string"
typeof true;                  // "boolean"
typeof undefined;             // "undefined"
typeof null;                  // "object" -- JS bug!
typeof {name: 'John'};        // "object"
typeof [1, 2, 3]              // "object"
typeof function Hello() {};   // "function"
```

