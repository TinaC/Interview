# Float

The float CSS property places an element on the left or right side of its container, allowing text and inline elements to wrap around it.

The element is removed from the normal flow of the page, though still remaining a part of the flow (in contrast to absolute positioning `position: absolute;`).
挪出了正常的页面文本流，但还是文本流的一部分（还会预留位置）

> absolute
> The element is removed from the normal document flow, and no space is created for the element in the page layout. It is positioned relative to its closest positioned ancestor, if any; otherwise, it is placed relative to the initial containing block. Its final position is determined by the values of top, right, bottom, and left.
> 被挪出了正常的文本流，并且不会给它预留位置

A floating element is one where the computed value of float is not none.

```css
float: none;
float: left;
float: right;
```

## How floated elements are positioned

As mentioned above, when an element is floated, it is taken out of the normal flow of the document (though still remaining part of it).
It is shifted to the left, or right, until it touches the edge of its containing box, or another floated element.

## Reference

https://developer.mozilla.org/en-US/docs/Web/CSS/float

---

## clear float

> The clear CSS property sets whether an element must be moved below (cleared) floating elements that precede it. The clear property applies to floating and non-floating elements.
> 把元素放在它之前的 float 元素的后面，而不是并排放

https://developer.mozilla.org/en-US/docs/Web/CSS/clear
