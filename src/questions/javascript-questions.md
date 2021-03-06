---
title: JavaScript Questions
layout: layouts/page.njk
permalink: /questions/javascript-questions/index.html
---

- **Explain event delegation.**  
  If we have a lot of elements handled in a similar way, then instead of assigning a handler to each of them – we put a single handler on their common ancestor. When using event delegation pattern, listening for events on multiple elements requires just one event listener.  
  //could add more here  

- **Explain how `this` works in JavaScript.**

  - In a method, `this` refers to the owner object.
  - When used alone, `this` refers to the global object. In a browser window. the global object is `[object Window]`
  - In a function, `this` refers to the global object because the owner of the function is the default binding for `this`.
  - In a function, in strict mode, `this` is undefined.
  - In HTML event handlers, `this` refers to the element that received the event.
  - Methods like call(), and apply() can refer `this` to any object.

- **Can you give an example of one of the ways that working with `this` has changed in ES6?**

  - Anonymous function passed as argument gets its this value from the function who is executing it. In non-strict mode, if `this` is undefined, then it falls back to `window`.
  - fat arrow function in ES6 is, `this` inside fat arrow function points to whatever the value of `this` inside upper function is. Hence value of `this` inside arrow function is lexically scoped.

- **Explain how prototypal inheritance works.**  
  Everything in Javascript is an `object`. Even when creating a `Class` is an `Object` via an `Object Literal` or `Constructor Function`. This is how Javascript does class-based programming as to other traditional Object-Oriented Programming languages where they use the keyword `class` and `inheritance`.  

  So, the core idea of Prototypal Inheritance is that an object can point to another object and inherit all its properties. The main purpose is to allow multiple instances of an object to share common properties, hence, the Singleton Pattern.  

- **What's the difference between a variable that is: `null`, `undefined` or `undeclared`?**
  - `undefined` is a variable that has been declared but no value exists and is a type of itself `undefined`.
  - `null` is a value of a variable and is a type of object.
  - `undeclared` variables is a variable that has been declared without `var` keyword
  - `undeclared` variables don’t even exist. `undefined` variables exist, but don’t have anything assigned to them. `null` variables exist and have null assigned to them

- **How would you go about checking for any of these states?**
  - We use `console.log()`; and `type of` to check if a variable is `undefined` or `null`. `type of` can also be used to tell the difference between `undefined` and `undeclared`
- What is a closure, and how/why would you use one?
- What language constructions do you use for iterating over object properties and array items?
- Can you describe the main difference between the `Array.forEach()` loop and `Array.map()` methods and why you would pick one versus the other?

- **What's a typical use case for anonymous functions?**  
  Since Anonymous Functions are function expressions rather than the regular function declaration which are statements. Function expressions are more flexible. We can assign functions to variables, object properties, pass them as arguments to other functions, and even write a simple one line code enclosed in an anonymous functions.  

  Example:  
  `var squaredArray = inputArray.map(function(x) { return x * x; });`  
  With ES6 syntax this becomes even more concise.  
  `var squaredArray = inputArray.map(x => x * x);`  
  Another typical example would be an anonymous function used by popular frameworks used as `IIFE` (Immediate Invoked Function Expression).  
  `(function() { })();`
- **Can you describe the main difference between the `Array.forEach()` loop and `Array.map()` methods and why you would pick one versus the other?**
  **Definition**
  The `map` method receives a function as a parameter. Then it applies it on each element and returns an entirely new array populated with the results of calling the provided function.

  Like `map` , the `forEach()` method receives a function as an argument and executes it once for each array element. However, instead of returning a new array like map, it returns `undefined`.

  **1.The returning value**
  The first difference between `map()` and `forEach()` is the returning value. The `forEach()` method returns `undefined` and `map()` returns a new array with the transformed elements. Even if they do the same job, the returning value remains different.

  **2. Ability to chain other methods**
  The second difference between these array methods is the fact that `map()` is chainable. This means that you can attach `reduce()`, `sort()`, `filter()` and so on after performing a `map()` method on an array.

  That's something you can't do with `forEach()` because, as you might guess, it returns `undefined`.

  **3. Mutability**
  In general, the word "mutate" means change, alternate, modify or transform. And in the JavaScript world it has the same meaning.
  The `map()` method returns an entirely new array with transformed elements and the same amount of data. In the case of `forEach()`, even if it returns `undefined`, it will mutate the original array with the callback.

  Therefore, we see clearly that `map()` relies on immutability and `forEach()` is a mutator method.



- What's a typical use case for anonymous functions?
- What's the difference between host objects and native objects?
- Explain the difference between: `function Person(){}`, `var person = Person()`, and `var person = new Person()`?
- Explain the differences on the usage of `foo` between `function foo() {}` and `var foo = function() {}`
- Can you explain what `Function.call` and `Function.apply` do? What's the notable difference between the two?
- Explain `Function.prototype.bind`.
- What's the difference between feature detection, feature inference, and using the UA string?
- Explain "hoisting".
- Describe event bubbling.
- Describe event capturing.
- What's the difference between an "attribute" and a "property"?
- What are the pros and cons of extending built-in JavaScript objects?
- **What is the difference between `==` and `===`?**
  - `==` in JavaScript is used for comparing two variables, but it ignores the datatype of variable. `===` is used for comparing two variables, but this operator also checks datatype and compares two values.
- Explain the same-origin policy with regards to JavaScript.
- Why is it called a Ternary operator, what does the word "Ternary" indicate?
- What is strict mode? What are some of the advantages/disadvantages of using it?
- What are some of the advantages/disadvantages of writing JavaScript code in a language that compiles to JavaScript?
- What tools and techniques do you use debugging JavaScript code?
- Explain the difference between mutable and immutable objects.
  - What is an example of an immutable object in JavaScript?
  - What are the pros and cons of immutability?
  - How can you achieve immutability in your own code?
- Explain the difference between synchronous and asynchronous functions.
- What is event loop?
  - What is the difference between call stack and task queue?
- What are the differences between variables created using `let`, `var` or `const`?
- What are the differences between ES6 class and ES5 function constructors?
- Can you offer a use case for the new arrow `=>` function syntax? How does this new syntax differ from other functions?
- What advantage is there for using the arrow syntax for a method in a constructor?
- What is the definition of a higher-order function?
- Can you give an example for destructuring an object or an array?
- Can you give an example of generating a string with ES6 Template Literals?
- Can you give an example of a curry function and why this syntax offers an advantage?
- What are the benefits of using `spread syntax` and how is it different from `rest syntax`?
- How can you share code between files?
- Why you might want to create static class members?
- What is the difference between `while` and `do-while` loops in JavaScript?
- What is a promise? Where and how would you use promise?

## Coding questions

- Make this work:

```javascript
duplicate([1, 2, 3, 4, 5]); // [1,2,3,4,5,1,2,3,4,5]
```

- Create a for loop that iterates up to `100` while outputting **"fizz"** at multiples of `3`, **"buzz"** at multiples of `5` and **"fizzbuzz"** at multiples of `3` and `5`
- What will be returned by each of these?

```javascript
console.log("hello" || "world");
console.log("foo" && "bar");
```

- Write an immediately invoked function expression (IIFE)
