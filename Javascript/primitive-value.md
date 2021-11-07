# Type

## Primitive Value

> All types except objects define immutable values (that is, values which can't be changed). For example (and unlike in C), Strings are immutable. We refer to values of these types as "primitive values".

- Boolean
- Number
- String
- Undefined
- Null
- Symbol (ES6) 2015
- BigInt (ES11) 2020

https://developer.mozilla.org/en-US/docs/Web/JavaScript/Data_structures

## Object

> In computer science, an object is a value in memory which is possibly referenced by an identifier.

Reference values are objects that are stored in the heap.
Reference value stored in the variable location is a pointer to a location in memory where the object is stored.

## typeof

```js
typeof undefined     === "undefined"; // true
typeof true          === "boolean";   // true
typeof 42            === "number";    // true
typeof "42"          === "string";    // true
typeof { life: 42 }  === "object";    // true

// added in ES6!
typeof Symbol()      === "symbol";    // true

typeof 2n ** 53n     === "bigint";    // true

typeof null          === "object";    // true

// 判断null, null is the only primitive value that is "falsy" (aka false-like) but that also returns "object" from the typeof check.
var a = null;
(!a && typeof a === "object"); // true

// Object(native or host and does implementent [[Call]])
// 标准规定了，实现了[[Call]]的object 返回function (Callable Object)
typeof new Function === "function"; // true
typeof new Function() === "function"; // true
typeof Object === "function"; // true

typeof [] === "object"; // true
// typeof wrapper object还是object
typeof new Array() === "object"; // true
typeof new String() === "object"; // true
```

typeof 相比 primitive type 就多了个 function
还有 null 是 object

标准：
https://262.ecma-international.org/5.1/#sec-11.4.3

https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/typeof#description
