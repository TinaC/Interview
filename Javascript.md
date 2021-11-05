# Javascript

[Introduce some new features about ECMAScript](./Javascript/new-feature.md)

---

## Type

[JS 的基本类型，primitive type](./Javascript/primitive-value.md)

[为什么叫 primitive type, 和 object 的区别是?](./Javascript/primitive-value.md)

[如何判断这些基本类型，typeof](./Javascript/primitive-value.md)

[typeof 是 object 的有哪几种类型，分别如何判断](./Javascript/primitive-value.md)

```js
Array.isArray([1, 2, 3]); // true

if (variable === null) Number.isNaN(NaN); // true
```

---

[What is the difference between == and ===?](https://github.com/TinaC/Blog/blob/master/JavaScript/equlity.md)

如果类型相同，== & === 是一样的
如果类型不同， === 直接返回 false, == 先执行类型转换(type conversions / coerce)再进行比较
coerce 规则见《You Don't Know JS》中册

---

## Event

[event propagation 传播, event bubble](https://github.com/TinaC/Blog/blob/master/JavaScript/event_propagation.md)

[Explain event delegation](Javascript/event-delegation.md) 事件委托

写一个事件委托的例子

stopPropagation will prevent any parent handlers from being executed.

stopImmediatePropagation will prevent any parent handlers and also any other handlers from executing

https://stackoverflow.com/questions/5299740/stoppropagation-vs-stopimmediatepropagation

---

## Prototype

[instanceof 的目的](./Javascript/primitive-value.md)

> The instanceof operator tests to see if the prototype property of a constructor appears anywhere in the prototype chain of an object. The return value is a boolean value.

查找原型链

```js
// defining constructors
function C() {}
function D() {}

let o = new C();

// true, because: Object.getPrototypeOf(o) === C.prototype
// C(构造函数)的原型属性存在于o的原型链上
o instanceof C;

// false, because D.prototype is nowhere in o's prototype chain
o instanceof D;
```

```js
var myArray = [1, 2, 3];
myArray instanceof Array; // true
myArray instanceof Object; // true
// instanceof fails to work for literal values (because literals are not Objects)
3 instanceof Number; // false
"abc" instanceof String; // false
true instanceof Boolean; // false
```

原型链

[What is prototype chain, Explain how prototypal inheritance works](Javascript/prototype.md) 原型链 原型继承

写一个原型继承的 Sample

---

## Scope & this

[Explain how `this` works in JavaScript](Javascript/this.md)

[arrow function](Javascript/this.md)

[What's the difference between .call() and .apply()?](Javascript/this.md)

[Explain Function.prototype.bind()](Javascript/this.md)

scope, lexical scope 词法作用域

`this`: Dynamic scope, run-time binding
`arrow function`: Lexical scope, author-time

[Coding Problems, Temporal Dead Zone](Javascript/code/this.md)

[Coding Problems, var, let 和 const 的区别](Javascript/code/let.md)

---

## Event loop

[macrotask, microtask](https://github.com/TinaC/Blog/blob/master/JavaScript/event_loop.md)

[Coding Problems, async setTimeout](Javascript/code/async.md)

[What is a closure, and how/why would you use one?](Javascript/closure.md) 闭包

---

## Live coding

https://www.freecodecamp.org/news/3-questions-to-watch-out-for-in-a-javascript-interview-725012834ccb/

[Make this work `duplicate([1, 2, 3, 4, 5]); // [1,2,3,4,5,1,2,3,4,5]`](Javascript/code/array.md)

[Write a event delegation](Javascript/event-delegation.md)
