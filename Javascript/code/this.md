# Scope & This

## What is a Temporal Dead Zone?

What's the result of this and why?

```js
x = 23;
var x;
```

> Uncaught SyntaxError: Identifier 'x' has already been declared

```js
`use strict`;
b = 23; // ReferenceError: b is not defined

var b;
```

必须是在全局对象下才会报错，
块作用域下不会报错:

```js
{
  `use strict`;
  b = 23; // No error
}
```

> First, strict mode makes it impossible to accidentally create global variables. In normal JavaScript mistyping a variable in an assignment creates a new property on the global object and continues to "work" (although future failure is possible: likely, in modern JavaScript). Assignments, which would accidentally create global variables, instead throw an error in strict mode:
> https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Strict_mode#converting_mistakes_into_errors

---

## Temporal Dead Zone 临时性死区

Temporal Dead Zone is a behaviour that occurs with variables declared using `let` and `const` keywords.

It is a behaviour where we try to access a variable before it is initialized.

Examples of temporal dead zone:

```js
x = 23; // Uncaught ReferenceError: Cannot access 'x' before initialization
let x;
```

```js
function anotherRandomFunc() {
  message = "Hello"; // Uncaught ReferenceError: Cannot access 'message' before initialization
  let message;
}
anotherRandomFunc(); //
```

In the code above, both in global scope and functional scope, we are trying to access variables which have not been declared yet. This is called the Temporal Dead Zone .
