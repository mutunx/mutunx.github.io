---
title: JavaScript 中 firstChild 和 firstElementChild 有什么区别
date: 2022-08-30
tags:
---

`firstChild` 获取第一个 `node` 节点不管什么类型
`firstElementChild` 只获取第一个 `element` 类型的节点

#### node 分为 element node / comment node / text node

```js
div = document.createElement('div');
> <div></div>
div.appendChild(document.createTextNode("hello"))
div.appendChild(document.createComment("hello"))
div.appendChild(document.createElement("hello"))
> <div>
    "hello"
    <!--hello-->
    <hello></hello>
  </div>
```