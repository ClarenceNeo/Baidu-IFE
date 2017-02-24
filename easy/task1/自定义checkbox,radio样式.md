## 任务目的

1. 深入了解 html label 标签
2. 了解 CSS 边框、背景、伪元素、伪类（注意和伪元素区分）等属性的设置
3. 了解 CSS 中常见的雪碧图，并能自己制作使用雪碧图

## 任务描述

1. 参考 样例（[点击查看](![](http://oeryvxt85.bkt.clouddn.com/2017-02-24-99322cf8c3283e42.png))），实现页面开发，要求实现效果基本一致

## 任务注意事项

1. 尝试背景图和伪元素两种不同方式实现，对比两种方式各自的优缺点。
2. 注意测试不同情况，尤其是极端情况下的效果。

## 参考资料

1. [MDN label](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/label): 了解 html 中 label 的基本知识
2. [MDN background-position](https://developer.mozilla.org/en-US/docs/Web/CSS/background-position): 了解背景图片定位相关知识
3. [MDN :checked](https://developer.mozilla.org/en-US/docs/Web/CSS/:checked): 了解 input 的 `:checked` 伪类的基本知识以及应用场景
4. [MDN :before](https://developer.mozilla.org/en-US/docs/Web/CSS/::before):了解 input 的 `:before` 伪元素的基本知识
5. [MDN :after](https://developer.mozilla.org/en-US/docs/Web/CSS/::after):了解 input 的 `:after` 伪元素的基本知识

### 笔记

for元素：在同一个文件中，与指定的表单元素绑定

显式：

```
<label for="ex">abc</label>
<input type="text" id="ex">
```

隐式：

```
<label>abc<input type="text"></label>
```

在label标签和表单元素创建关联需要id属性，将表单数据发回服务器需要name属性。

思路：首先浏览器自带的input:checkbox的样式不能直接修改，但是提供的label标签带有for属性，当label标签被选中后，for所绑定的对应id的input也将被选中，所以可以利用这一点，来设置各种各样的自定义控件。

方法：隐藏input标签，为lable标签添加背景图片，来自定义样式，利用:checked伪类选择器来控制选中时背景图片位置的变化来达成样式的变化，利用:before或:after伪元素来添加提示文字（当然也可以利用伪元素来控制样式）。


