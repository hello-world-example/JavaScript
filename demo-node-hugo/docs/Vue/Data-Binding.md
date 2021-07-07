# 数据双向绑定原理

> [Object.defineProperty(obj, prop, descriptor)](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Object/defineProperty)  可以在对象上定义新属性，或者修改现有属性

## 常规方式

### 页面

```html
<h1 id="title">Hello</h1>
<input type="text" id="a" />
```

### js

```js
var title = document.getElementById("title");
var input = document.getElementById("a"),
// 监听 input 输入事件，修改 h1 标签内容
input.oninput = function (e) {
    title.innerHTML = this.value;
};

// 修改 input 数据的时候，需要同时修改 h1 标签内容
input.value = '123';
title.innerHTML = input.value;
```

## “数据绑定“ 之后

数据绑定实际上是重写 数据对象 的 get/set 方法，修改其默认行为

```js
Object.defineProperty(input, 'val', { //这里必须定义一个新的属性名称，不可以用 value，否则会报错。
    get: function () {
        return this.value;
    },
    set: function (val) {
        this.value = val;
        title.innerHTML = val;
    }
});

// 这时候给一个对象赋值，会调用 set 方法，实际行为已经被改变
input.val = 'good';
```

## Read More

-  [数据双向绑定原理](https://www.cnblogs.com/lovebread/p/7875203.html)

-  [vue 的双向绑定原理及实现](https://www.cnblogs.com/canfoo/p/6891868.html)