# BFC(块级格式化上下文)
BFC(Block formatting context)
BFC是一个独立的渲染区域，只有Block-level参与，规定内部的Block-level Box如何布局，和区域外的内容无关
## 元素的显示属性
display的属性值有很多 display:block inline none
## 具有BFC条件的元素
dispaly: block list-item table（布局中的常用元素）

宽度、高度、padding border margin
## 什么情况可以让元素产生BFC
```
元素添加如下属性就可以触发BFC
float的属性值不为none
position的值为absolute或者fixed
display为inline-block table-cell table-caption flex inline-flex
overflow不为visible
```
### BFC具有的特性
1. 在BFC中，盒子从顶端垂直排列
2. 盒子垂直方向的距离由margin决定，属于同一BFC盒子的两个相邻盒子的margin值会发生重叠
3. 每个盒子的做外边缘（margin-left）会触碰到容器的左边缘（border-left）
4. BFC的区域不会和浮动盒子产生交集，而是紧贴浮动边缘
5. 计算BFC高度时会自动检测浮动的盒子高度
### BFC的用途
1. 清除元素内部浮动

常用overflow: hidden

主要用到上面的第5条特性，计算BFC高度的时候自然检测浮动盒子的高度

2. 解决外边距合并问题

主要用到第2条特性，让外边距重叠的盒子不属于同一个BFC

3. 制作右侧自适应的盒子

主要用到第3条特性






