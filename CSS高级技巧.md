# CSS高级技巧

## CSS界面用户样式
### 鼠标样式 cursor
1. text 默认文本样式
2. pointer 小手
3. default 小白
4. move 移动
### 轮廓outline
```
应用场景：
outline:0(outline:none) 取消input的轮廓线
```
### 防止拖拽文本域resize
resize:none
## vertical-align 垂直居中
![1](D:\Document\image\1.png)

vertical-align: baseline || top || middle || bottom

应用场景：
1. 实现行内块元素（图片、表单）和内容居中对齐
2. 去除图片底侧空白缝隙
* 将图片转为块级元素
* 使用vertaical-align:top
## 溢出的文字隐藏
### 英文换行 word-break
### 中文换行 white-space
### text-overflow文字溢出
1. text-overflow:clip 简单的裁剪，不显示省略标记
2. text-overflow:ellipsis 文本溢出时显示省略标记
* 首先强制一行内显示（white-space:nowrap）
* 然后和overflow配合使用（overflow:hidden）
* 最后text-overflow:ellipsis

## CSS精灵技术（sprite）小妖精 雪碧
### 精灵技术本质
CSS精灵技术本质上是一种处理网页背景图片的方式，将一个页面涉及到的所有图像集中到一张大图中去
## 字体图标（iconfont）
```
可以做和图片一样的事，例如改变透明度、旋转度
本质还是文字，可以改变颜色、大小等
体积小，携带信息没有削减
几乎支持所有的浏览器
移动端设备的必备良药
```
下载之后的使用步骤：

1. 声明字体
2. 给盒子使用字体
3. 盒子里面添加结构
## 滑动门
### 核心技术
核心技术就是利用CSS精灵和盒子padding撑开宽度，以便适应不同字数的导航栏

滑动门的布局如下所示:
```
<li>
    <a href="#">
        <span>导航栏内容</span>
    </a>
</li>
```
总结：
1. a设置背景左侧，padding-left撑开合适宽度
2. span设置背景右侧，padding-right撑开合适宽度，剩下由文字继续撑开宽度
3. a包含span是因为导航是可以点击的

## before和after伪元素
```
类选择器、伪类选择器就是选取对象
伪元素选择器本质上是插入一个行内元素（标签、盒子），伪元素是不占位置的
```
## CSS过渡（transition）(CSS3)
过渡：从一种状态变为另一种状态的过程
```
谁做动画谁做过渡
```
语法：
```
transition: 过渡的属性 花费时间 运动曲线 何时开始；
transition写在div中，而不是写在hover中
写在div中有返回效果，写在hover中没有返回效果
```

| 属性 | 描述 |
| ---- | ---- |
| transition-property   | 定义应用过渡的CSS属性名称 |
| transition-duration  | 定义过渡效果花费的时间，默认是0 |
| transition-timing-function  | 定义过渡效果的时间曲线，默认是“ease" |
| transition-delay | 规定过渡效果何时开始，默认是0 |
## 2D变形(CSS3)transform
2D变形可以实现元素的位移、旋转、倾斜和缩放，甚至支持矩阵方式
1. 移动translate(x,y)
```
translate(x,y)  水平方向和垂直方向同时移动
translateX(x)  仅水平方向移动
translateY(y)  仅垂直方向移动
```
2. 缩放scale(x,y)
scale(x,y)  水平方向和垂直方向同时缩放
scaleX(x)  仅水平方向缩放
scaleY(y)  仅垂直方向缩放
3. 旋转rotate(deg)
可以对元素进行旋转，正值为顺时针，负值为逆时针
4. transform-origin 设置旋转中心点
transform-origin:left
transform-origin:20px 20px;
5. 倾斜skew(xdeg,ydeg)
```
x为正值，向左倾斜；x为负值，向右倾斜
y为正值，向上亲给；y为负值，向下倾斜
```
## 3D变形
```
透视是眼睛到屏幕的距离,透视只是一种展示形式，有3d效果
translateZ是物体到屏幕的距离   近大远小
```
## 动画 animation
```
语法格式：（这里引用动画）
animation:动画名称 动画时间 运动曲线 何时开始 播放次数 是否反方向；
```
```
定义动画：
@keyframes 动画名称{
    from{开始位置}
    to{结束位置}
}
```
```
animation-iteration-count:infinite; 无限循环播放
animation-play-state:paused; 暂停动画
```