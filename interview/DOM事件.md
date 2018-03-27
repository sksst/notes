### DOM事件的级别

DOM0 

```js
element.onclick=function(){}
```

DOM2

```
element.addEventListener('click', function(){}, false)
```

DOM3

```js
// 增加了一些事件类型
element.addEventListener('keyup', function(){}, false)
```

### DOM事件模型

捕获、冒泡



### DOM事件流

捕获 --> 目标阶段 --> 冒泡



### 描述DOM事件捕获的具体流程

window --> document --> html ... 目标元素



### Event对象的常见应用

```js
event.preventDefault()
event.stopPropagation()
event.stopImmediatePropagation()
event.currentTarget
event.target
```



### 自定义事件

```js
var eve = new Event('custome');
ev.addEventListener('custome', function(){
    console.log('custome');
});
ev.dispatchEvent(eve);
```



