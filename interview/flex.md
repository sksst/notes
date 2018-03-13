Flex 是 Flexible Box 的缩写，意为"弹性布局"，用来为盒状模型提供最大的灵活性。

## 容器的属性

- `flex-direction`：主轴的方向。
- `flex-wrap` ：换行规则。
- `flex-flow` ：`flex-direction`属性和`flex-wrap`属性的简写形式。
- `justify-content` : 项目在主轴上的对齐方式。
- `align-items` : 项目在交叉轴上的对齐方式。
- `align-content` : 多根轴线的对齐方式（一根轴线，该属性不起作用）。



## 项目的属性

- `order` : 定义项目的排列顺序。数值越小，排列越靠前，默认为0。
- `flex-grow` : 定义项目的放大比例，默认为`0`，即如果存在剩余空间，也不放大。
- `flex-shrink` : 定义了项目的缩小比例，默认为1，即如果空间不足，该项目将缩小。
- `flex-basis` : 定义了在分配多余空间之前，项目占据的主轴空间。
- `flex` : `flex-grow`, `flex-shrink` 和 `flex-basis`的简写，默认值为`0 1 auto`。后两个属性可选。
- `align-self`  : 允许单个项目有与其他项目不一样的对齐方式，可覆盖`align-items`属性。





参考资料：

- [Flex 布局教程：语法篇](http://www.ruanyifeng.com/blog/2015/07/flex-grammar.html?^%$)
- [Flex 布局教程：实例篇](http://www.ruanyifeng.com/blog/2015/07/flex-examples.html)

