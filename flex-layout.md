# flex布局
```
步骤：
1. 父级元素添加flex; display:flex;
2. 子盒子添加份数; flex：1;
```
## flex属性
### 最小和最大宽度
目的在于保护盒子不至于变形
1. 最小宽度 min-width
2. 最大宽度 max-width
### flex-direction设置主轴方向（默认水平方向）
flex-direction：column; 从上向下排列
### justify-content 水平对齐
设置子盒子在横轴方向上的对齐方式
### align-items 垂直对齐
设置子盒子在纵轴方向上的对齐方式
### flex-wrap控制是否换行
1. nowrap不换行
2. wrap换行
### align-content堆栈（由flex-wrap产生的独立行）对齐
```
align-items是针对一行的垂直对齐
align-content是针对多行的垂直对齐
```
使用条件：
1. 父元素设置display:flex
2. 排列方式为横向排列flex-direction:row
3. 设置换行flex-wrap:wrap
### flex-flow
flex-flow是flex-direction、flex-wrap的简写形式
```
flex-flow:排列方向 换不换行
```
### order控制子盒子的排列顺序
用CSS来控制盒子的排列顺序（默认值是0），数字越小越排在前面
