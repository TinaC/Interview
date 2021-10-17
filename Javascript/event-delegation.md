# Event delegation

Event delegation is a technique involving adding event listeners to a parent element instead of adding them to the descendant elements. The listener will fire whenever the event is triggered on the descendant elements due to event bubbling up the DOM. The benefits of this technique are:

Memory footprint goes down because only one single handler is needed on the parent element, rather than having to attach event handlers on each descendant.
There is no need to unbind the handler from elements that are removed and to bind the event for new elements.

利用事件冒泡和事件捕捉，可以实现更优秀的事件处理模式：事件委托

如果有很多元素需要同样的事件处理，与其分配给每个元素 handler，不如给它的祖先元素一个统一单个 handler。当点击子元素，事件会冒泡到它的祖先元素，然后利用 event.target 来判断如何处理。

父元素捕获后代元素的事件，后代元素将它们的事件冒泡到父元素

典型的例子设置 event 到`<ul>`, 而不是`<li>`. (但是现在都用模板，数据绑定，不会复制粘贴`<li>`来分配 handler 了吧)

优点:

1. 节约内存, 不用重复创建多个 event handler
2. 不用 copy & paste 绑定 event handler, 当频繁添加删除子元素的时候，不需要再操作 handlers
3. 对于动态生成的元素，不用再 rebind handler
4. 如果子元素之间的 handler 不相同，更应该把整体的 handler 逻辑写在父元素，避免出错

https://frontendinterviewhandbook.com/javascript-questions/#explain-event-delegation
https://codeburst.io/the-simple-rules-to-this-in-javascript-35d97f31bde3
https://stackoverflow.com/a/3127440/1751946
