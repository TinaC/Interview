# Interview

- [General](./General.md)
- [HTML](./HTML.md)
- [CSS](./CSS.md)
- [SASS](./SASS.md)

---

- [HTTP](./HTTP.md)
- [Security]

---

- [Javascript](./Javascript.md)
- [Bootstrap]
- [jQuery](./jQuery.md)
- [React](./React.md)
- [Typescript]

---

- [Webpack]

- [Git](./Git.md)

---

## Reference

https://github.com/h5bp/Front-end-Developer-Interview-Questions/blob/main/src/questions/general-questions.md

https://www.interviewbit.com/java-interview-questions/

https://juejin.cn/post/7007991848308310024?utm_source=gold_browser_extension#heading-2

https://frontendinterviewhandbook.com/javascript-questions/

## Literal Inference

```js
declare function handleRequest(url: string, method: "GET" | "POST"): void;

const req = { url: "https://example.com", method: "GET" };

// 因为这中间是可能插入代码的，比如 `req.method = "GUESS"`, 所以ts认为req.methods的类型是string, 而不是"GET"

handleRequest(req.url, req.method);
// Argument of type 'string' is not assignable to parameter of type '"GET" | "POST"'.
```

expression evaluation 表达式求值
evaluate: 评估，代码求值

In the above example, `req.method` is inferred to be string, not "GET".
Because code can be evaluated 求值,执行 between the creation of `req` and the call of `handleRequest` which could assign a new string like "GUESS" to `req.method`, TypeScript considers this code to have an error.

---

https://www.typescriptlang.org/docs/handbook/2/functions.html#push-type-parameters-down

这俩谁更好

```
function firstElement1<Type>(arr: Type[]) {
  return arr[0];
}
 
function firstElement2<Type extends any[]>(arr: Type) {
  return arr[0];
}
 
// a: number (good)
const a = firstElement1([1, 2, 3]);
// b: any (bad)
const b = firstElement2([1, 2, 3]);
```