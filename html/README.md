HTML
## CSS
### 特性
- 相同的属性会覆盖：后面的css属性覆盖前面的css属性
- 不同的属性都生成
- 选择器优先级：通配符<标签<类<id<行内样式<!important
    - 范围远大，优先级越低
### 选择器
- 标签选择器
```
p {
    color: #000;
}
```
- 类选择器
```
.container {
    width: 100%;
}
```
- id选择器
  ==同一个id选择器在一个页面只能用一次==
```
#header {
    background: #000;
}
```
- 通配符选择器
  通常在清楚默认样式的时候使用
```
* {
    box-sizing: border-box;
}
```
- 复合选择器
  定义：由两个或多个基础选择器，通过不同的方式组合而成。
  作用：更准确、更高效的选择目标元素
```
/*div里面的所有span颜色都会是#fff*/
div span{
    color: #fff;
}
/*div里面的只有儿子span颜色都会是#fff*/
div > span{
 color: #fff;
}

```
- 并集选择器
  逗号隔开选择器
```
div, span{
    background: #000;
}

```
- 交集选择器
  p标签下class熟悉是box的会改变颜色
```
p.box{
    background: #fff;
}

```
- 伪类选择器
  伪类表示元素状态，选择元素的样式。用:号表示
```
a:hover{
    color: #f00;
}

```
- 结构伪类选择器
    - :first-child 查找第一个元素
    - :last-child 查找最后一个元素
    - ntn-child(N) 查找第N个元素
```
li:first-child {
    background-color: #f00;
}

li:last-child {
    background-color: #0f0;
}

li:nth-child(3) {
    background-color: #00f;
}

```
### 显示模
#### 块级元素
- 独占一行
- 宽度默认是父级100%
- 添加宽度性生效
### 盒子模型
- overflow 元素溢出
    - hidden 溢出隐藏
    - scroll 溢出滚动，无论是否溢出都会出现滚动条
    - auth 溢出滚动，只有溢出才会出现滚动条
#### flex
设置方式：给父元素设置了display:flex，子元素可以自动挤压或拉伸
组成部分：
- 弹性盒子
- 弹性容器
- 主轴：默认水平方向
- 侧轴/交叉轴：默认在垂直方向
### 定位
作用：灵活的改变盒子在网页的位置

## 常见问题
1、浮动
- float浮动会导致布局脱标
- flex不会导致布局脱标
