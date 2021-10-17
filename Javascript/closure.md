# Closure

A closure is the combination of a function and the lexical environment within which that function was declared. The word "lexical" refers to the fact that lexical scoping uses the location where a variable is declared within the source code to determine where that variable is available. Closures are functions that have access to the outer (enclosing) function's variables—scope chain even after the outer function has returned.

Why would you use one?

- Data privacy / emulating private methods with closures. Commonly used in the module pattern.
- Partial applications or currying.

References#
https://developer.mozilla.org/en-US/docs/Web/JavaScript/Closures
https://medium.com/javascript-scene/master-the-javascript-interview-what-is-a-closure-b2f0d2152b36
