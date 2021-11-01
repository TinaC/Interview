# New features

https://juejin.cn/post/6844903811622912014#heading-45
https://juejin.cn/post/6968269593206849572#heading-10

[tc39 Finished Proposals](https://github.com/tc39/proposals/blob/master/finished-proposals.md)

## 2021 ES12

https://dev.to/brayanarrieta/new-javascript-features-ecmascript-2021-with-examples-3hfm

* Numeric separators

```js
// A billion
const amount = 1_000_000_000;

// Hundreds of millions     
const amount = 1_475_938.38;

// 6234500 cents (62345 dollars)
const amount = 62345_00;

// 1,734,500
const amount = 1_734_500; 

// 20^30000
const amount = 2e30_000;
```

* String replaceAll

```js
// Before
const message = 'hello+this+is+a+message';
const messageWithSpace = message.replace(/\+/g, ' ');

const message = 'hello+this+is+a+message';
const messageWithSpace = message.replaceAll('+', ' ')

// hello this is a message
```


Logical assignment operator
And & Equals (&&=)
OR & Equals (||=)
Nullish Coalescing & Equals (??=)
Promise.any
Private class methods
Private Getters and setters
WeakRef
Finalizers

## 2020 ES11

https://developers.amadeus.com/blog/new-javascript-features-es2020-examples

* import()
* flat() and flatMap()
* Nullish Coalescing Operator

* Optional Chaining Operator  

console.log(passenger?.profile?.name);

* Private classes variables  

* Promise.allSettled()  

* Object.fromEntries()  

* BigInt()  