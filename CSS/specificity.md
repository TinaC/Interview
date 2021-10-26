# Specificity

> Specificity CSS 优先级，越具体越优先

递增:

- inherent CSS 继承过来的
- Universal selector (\*), combinators (+, >, ~, ' ') and negation pseudo-class (`:not()`) 没有优先级，有等于没有
- Type selectors (e.g., `h1`) and pseudo-elements (e.g., `::before`).
- Class selectors (e.g., `.example`), attributes selectors (e.g., `[type="radio"]`) and pseudo-classes (e.g., `:hover`).
- ID selectors (e.g., `#example`).
- inline style attribute
- !important

相同优先级的 rule, 后加载的覆盖前面的

## 继承 parents 的 rule, 优先级最低

```css
/* 这个优先级高 */
* {
  color: blue;
}

/* Inherited from div */
div {
  color: red;
}
```

## :not()

虽然:not()本身是不算入优先级的，但是里面的 rule 是算的，所以不要写太长了

```css
/* 这个优先级高 */
input:not([type="text"]):not([type="checkbox"]):not([type="radio"]) {
  color: blue;
}

body.robus-ui input[type="submit"] {
  color: red;
}
```

## Reference

https://developer.mozilla.org/en-US/docs/Web/CSS/Specificity#Selector_Types
https://developer.mozilla.org/en-US/docs/Web/CSS/Specificity
https://developer.mozilla.org/en-US/docs/Learn/CSS/Introduction_to_CSS/Cascade_and_inheritance
