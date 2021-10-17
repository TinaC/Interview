# let

```js
function func1() {
  setTimeout(() => {
    console.log(x);
    console.log(y);
  }, 3000);

  var x = 2;
  let y = 12;
}

func1();
```

> 2
> 12

Since, even though `let` variables are not hoisted, due to async nature of javascript, the complete function code runs before the `setTimeout` function. Therefore, it has access to both x and y.

先执行 x, y 的定义，再执行 setTimeout 的回调函数 / Event loop

https://www.interviewbit.com/javascript-interview-questions/#coding-problems

---

```js
function func2() {
  for (var i = 0; i < 3; i++) {
    setTimeout(() => console.log(i), 2000);
  }
}

func2();
```

> 3
> 3
> 3

three times since variable declared with `var` keyword does not have block scope.
Also, inside the for loop, the variable `i` is incremented first and then checked.

```js
function func2() {
  for (let i = 0; i < 3; i++) {
    setTimeout(() => console.log(i), 2000);
  }
}

func2();
```

> 0
> 1
> 2

`let` creates a variable declaration for each loop which is block level declaration. So basically it creates a scope within { }.
每个 loop 有属于自己的块作用域，保存了每个 loop 独有的 i

https://stackoverflow.com/questions/762011/whats-the-difference-between-using-let-and-var
