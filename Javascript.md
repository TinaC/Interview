# Javascript

## JS 的基本类型，primitive type

- Boolean
- Number
- String
- Undefined
- Null
- Symbol (ES6)

## What is the difference between == and ===?

https://github.com/TinaC/Blog/blob/master/JavaScript/equlity.md

如果类型相同，== & === 是一样的
如果类型不同， === 直接返回 false, == 先执行类型转换(type conversions / coerce)再进行比较
coerce 规则见《You Don't Know JS》中册

---

## Event

### event bubble

event_propagation

https://github.com/TinaC/Blog/blob/master/JavaScript/event_propagation.md

### [Explain event delegation](Javascript/event-delegation.md) 事件委托

---

## [What is prototype chain, Explain how prototypal inheritance works](Javascript/prototype.md) 原型链 原型继承

写一个原型继承的 Sample

---

## Scope & this

### [Explain how `this` works in JavaScript](Javascript/this.md)

### [arrow function](Javascript/this.md)

### [What's the difference between .call and .apply?](Javascript/this.md)

### [Explain Function.prototype.bind.](Javascript/this.md)

### scope, lexical scope 词法作用域

`this`: Dynamic scope, run-time binding
`arrow function`: Lexical scope, author-time

---

## Event loop

## [What is a closure, and how/why would you use one?](Javascript/closure.md) 闭包
