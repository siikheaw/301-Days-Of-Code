# How we organize in JS

Two major patterns for organizing code (data and behavior) : **classes** and **modules**.

## Classes
A class in a program is a definition of a **"type"** of custom data structure that includes both data and behaviors that operate on that data.
Classes define how such a data structure works, but classes are not themselves concrete values. To get a concrete value that you can use in the program, a class must be instantiated (with the `new` keyword) one or more times.

### Class Inheritance
`extends`
`super`

Both inherited and overriden methods can have the same name and co-exist is called *polymorphism*.

Inheritance is a powerful tool for organizing data/behavior in separate logical units (classes), but allowing the child class to cooperate with the parent by accessing/using its behavior and data.

## Modules
Modules has the same goal as the class pattern, to group data and behavior together into logical units. Modules can *include* or *access* the data and behaviors of other modules.

Modules was an important and common pattern that was leveraged in countless JS programs, even without a dedicated syntax.

The key hallmarks of a classic module are an outer function (that runs at least once), which returns an "instance" of the module with one or more functions exposed that can operate on the module instance's internal (hidden) data.

Because a module of this form is just a function, and calling it produces an "instance" of the module, another description for these functions is "module factories".

The class form stores methods and data on an object instance, which must be accessed with the this. prefix. With modules, the methods and data are accessed as identifier variables in scope, without any this. prefix.

With class, the "API" of an instance is implicit in the class definition -- also, all data and methods are public. With the module factory function, you explicitly create and return an object with any publicly exposed methods, and any data or other unreferenced methods remain private inside the factory function.

### ES Modules
