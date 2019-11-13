# CSS3 效果

- CSS3 效果
    - door-open 开门大吉源码
    - seamless-scrolling 无缝滚动源码

## css3 flex 布局

兼容性问题

- Android 
    - 2.3 开始支持旧版本的`display: -webkit-flex`
    - 4.4 开始支持标准版本的`display: flex`

- IOS 
    - 6.1 开始支持旧版本的 `display: -webkit-flex`
    - 7.1 开始支持标准版本的`display: flex`

- PC
    - `IE10`开始支持，但是`IE10` 的是`-ms`形式的。

兼容性的写法：

```css
    .box {
        /* 新版本语法：chrome 21+ */
        display: -webkit-flex; 
        /* 新版本语法：Opear 12.1,Firefox 22+ */
        display: flex; 
        /* 老版本语法：safari,Android browser,older Webkit browsers */
        display: -webkit-box;
        /* 老版本语法: Firefox (buggy) */
        display: -moz-box;
        /* 混合版本语法：IE10 */
        display: -ms-flexbox;
    }

    .flex1 {
        /* Chrome */
        -webkit-flex: 1; 
        /* IE10 */
        -ms-flex: 1;
        /* Opear 12.1,Firefox 20+ */
        flex: 1;
        /* IOS6, Safari 3.1-6 */
        -webkit-box-flex: 1;
        /* Firefox 19- */
        -moz-box-flex: 1;
    }
```

浏览器兼容的`flex` 语法：
```css
    .flex1 {
    -webkit-flex: 1;        /* Chrome */
    -ms-flex: 1             /* IE 10 */
    flex: 1;                /* NEW, Spec - Opera 12.1, Firefox 20+ */
    -webkit-box-flex: 1     /* OLD - iOS 6-, Safari 3.1-6 */
    -moz-box-flex: 1;       /* OLD - Firefox 19- */
}
.box{
 
    display: -webkit-flex;  /* 新版本语法: Chrome 21+ */
    display: flex;          /* 新版本语法: Opera 12.1, Firefox 22+ */
    display: -webkit-box;   /* 老版本语法: Safari, iOS, Android browser, older WebKit browsers. */
    display: -moz-box;      /* 老版本语法: Firefox (buggy) */
    display: -ms-flexbox;   /* 混合版本语法: IE 10 */
 
}

.flex1 {
    -webkit-flex: 1;        /* Chrome */
    -ms-flex: 1             /* IE 10 */
    flex: 1;                /* NEW, Spec - Opera 12.1, Firefox 20+ */
    -webkit-box-flex: 1     /* OLD - iOS 6-, Safari 3.1-6 */
    -moz-box-flex: 1;       /* OLD - Firefox 19- */
}
.box{
 
    display: -webkit-flex;  /* 新版本语法: Chrome 21+ */
    display: flex;          /* 新版本语法: Opera 12.1, Firefox 22+ */
    display: -webkit-box;   /* 老版本语法: Safari, iOS, Android browser, older WebKit browsers. */
    display: -moz-box;      /* 老版本语法: Firefox (buggy) */
    display: -ms-flexbox;   /* 混合版本语法: IE 10 */
 
}
/* 子元素-平均分栏 */
.flex1 {
  -webkit-box-flex: 1;      /* OLD - iOS 6-, Safari 3.1-6 */
  -moz-box-flex: 1;         /* OLD - Firefox 19- */
  width: 20%;               /* For old syntax, otherwise collapses. */
  -webkit-flex: 1;          /* Chrome */
  -ms-flex: 1;              /* IE 10 */
  flex: 1;                  /* NEW, Spec - Opera 12.1, Firefox 20+ */
}
/* 父元素-横向排列（主轴） */
.flex-h {
  display: box;              /* OLD - Android 4.4- */
  display: -webkit-box;      /* OLD - iOS 6-, Safari 3.1-6 */
  display: -moz-box;         /* OLD - Firefox 19- (buggy but mostly works) */
  display: -ms-flexbox;      /* TWEENER - IE 10 */
  display: -webkit-flex;     /* NEW - Chrome */
  display: flex;             /* NEW, Spec - Opera 12.1, Firefox 20+ */
  /* 09版 */
  -webkit-box-orient: horizontal;
  /* 12版 */
  -webkit-flex-direction: row;
  -moz-flex-direction: row;
  -ms-flex-direction: row;
  -o-flex-direction: row;
  flex-direction: row;
}
/* 父元素-横向换行 */
.flex-hw {
  /* 09版 */
  /*-webkit-box-lines: multiple;*/
  /* 12版 */
  -webkit-flex-wrap: wrap;
  -moz-flex-wrap: wrap;
  -ms-flex-wrap: wrap;
  -o-flex-wrap: wrap;
  flex-wrap: wrap;
}
/* 父元素-水平居中（主轴是横向才生效） */
.flex-hc {
  /* 09版 */
  -webkit-box-pack: center;
  /* 12版 */
  -webkit-justify-content: center;
  -moz-justify-content: center;
  -ms-justify-content: center;
  -o-justify-content: center;
  justify-content: center;
  /* 其它取值如下：
    align-items     主轴原点方向对齐
    flex-end        主轴延伸方向对齐
    space-between   等间距排列，首尾不留白
    space-around    等间距排列，首尾留白
   */
}
/* 父元素-纵向排列（主轴） */
.flex-v {
  display: box;              /* OLD - Android 4.4- */
  display: -webkit-box;      /* OLD - iOS 6-, Safari 3.1-6 */
  display: -moz-box;         /* OLD - Firefox 19- (buggy but mostly works) */
  display: -ms-flexbox;      /* TWEENER - IE 10 */
  display: -webkit-flex;     /* NEW - Chrome */
  display: flex;             /* NEW, Spec - Opera 12.1, Firefox 20+ */
  /* 09版 */
  -webkit-box-orient: vertical;
  /* 12版 */
  -webkit-flex-direction: column;
  -moz-flex-direction: column;
  -ms-flex-direction: column;
  -o-flex-direction: column;
  flex-direction: column;
}
/* 父元素-纵向换行 */
.flex-vw {
  /* 09版 */
  /*-webkit-box-lines: multiple;*/
  /* 12版 */
  -webkit-flex-wrap: wrap;
  -moz-flex-wrap: wrap;
  -ms-flex-wrap: wrap;
  -o-flex-wrap: wrap;
  flex-wrap: wrap;
}
/* 父元素-竖直居中（主轴是横向才生效） */
.flex-vc {
  /* 09版 */
  -webkit-box-align: center;
  /* 12版 */
  -webkit-align-items: center;
  -moz-align-items: center;
  -ms-align-items: center;
  -o-align-items: center;
  align-items: center;
}
/* 子元素-显示在从左向右（从上向下）第1个位置，用于改变源文档顺序显示 */
.flex-1 {
  -webkit-box-ordinal-group: 1;   /* OLD - iOS 6-, Safari 3.1-6 */
  -moz-box-ordinal-group: 1;      /* OLD - Firefox 19- */
  -ms-flex-order: 1;              /* TWEENER - IE 10 */
  -webkit-order: 1;               /* NEW - Chrome */
  order: 1;                       /* NEW, Spec - Opera 12.1, Firefox 20+ */
}
/* 子元素-显示在从左向右（从上向下）第2个位置，用于改变源文档顺序显示 */
.flex-2 {
  -webkit-box-ordinal-group: 2;   /* OLD - iOS 6-, Safari 3.1-6 */
  -moz-box-ordinal-group: 2;      /* OLD - Firefox 19- */
  -ms-flex-order: 2;              /* TWEENER - IE 10 */
  -webkit-order: 2;               /* NEW - Chrome */
  order: 2;                       /* NEW, Spec - Opera 12.1, Firefox 20+ */
}
```

## 移动端viewport 视口单位

1. 当把一个百分比的页面在移动设备浏览的时候，网页的宽度没有和设备宽度一致。
2. 移动设备的网页是基于什么？？？来计算宽度的？
3. 原因在移动设备中，浏览器和网页之间，还有一层虚拟的容器，这个容器叫 `viewport`
4. `viewport` 只有移动设备才有，而且主流设备当中的`viewport`默认宽度为980px，可以缩放

## 使用viewport 进行移动端的适配

标准化适配要求：
1. 网页的宽度和浏览器一致，网页的宽度和视口宽度一样，然后视口的宽度和浏览器一样（和设备的一样）
2. 保证网页内容的缩放比例和PC端保持一致，视口的缩放比是1:0；
3. 不允许用户自动缩放

去完成这个标准化的设置：
1. 怎么设置`viewport`
```css
<meta name="viewport" content="width=device-width,initial-scale="1.0",minimun-scale="1.0",user-scale="no"/>
```
2. 具体的功能怎么实现

属性 | 属性描述 | 值表示的含义
---------|----------|-------|
width | 设置视口的宽度 devive-width 表示当前设备的宽度| 
initial-scale | 设置视口的默认的缩放比 | 
user-scale | 设置视口是否允许用户自动缩放 | 0 表示否，1表示是，no表示不允许，yes表示允许
minium-scale | 最小允许缩放比
maximum-scale | 最大允许缩放比

## 垂直居中解决方案
1. 基于决定定位的解决方案（定宽+定高）

```css
main {
  position: absolute;
  top: 50%;
  left: 50%;
  /*18/2 = 9  */
  margin-left: -9em;
  /* 6/2 = 3 */
  margin-top: -3em;
  width: 18em;
  height: 6em;
}

```
这段代码本质上做了几件事情，先把这个元素的左上角放置在视口的正中心，然后利用负外边距把它向左、向上移动（移动距离等于其自身宽高的一半），从而把元素的正中心放置在视口的正中心。

同时还可以利用`calc()`函数
```css
main {
  position: absolute;
  top: calc(50% - 3em);
  left: calc(50% - 9em);
  width: 18em;
  height: 6em;
}
```

但是以上两种方法都是在定宽的定宽的情况下实现的，但是实际运用中，不定宽高的情况下是如何实现的？

答案来源于`css`变形属性，当我们在`translate()` 变形函数中使用百分比值时，而这正是我们所需要的

```css
main {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%,-50%);
}

```

2. 基于视口单位的解决方案

`vw`是与视口宽度相关的，与常人的直觉不符的是，`1vw` 实际上表示视口宽度的`1%`，而不是`100%`

```css
main {
  width: 18em;
  padding: 1em 1.5em;
  margin: 50vh auto 0;
  transform: translate(-50%);
}
```

3. 基于`Flexbox`的解决方案

```css
body {
  display: flex;
  min-height: 100vh;
  margin: 0;
}
main {
  margin: auto;
}

```
请注意，当我们使用`Flexbox` 时，`margin: auto` 不仅在水平方向上将元素居中，垂直方向上也是如此。

```css
main {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 18em;
  height: 18em;
}

```

## 特紧底部的页脚

1. 固定高度的解决方案

```html

<header>
  <h1>site name</h1>
</header>

<main>
  <p>
    数据类型的
  </p>
</main>

<footer>

</footer>
```

```css

main {
  min-height: calc(100vh - 2.5em - 7em);
}

```

2. flex解决方案

```css

body {
  display: flex;
  flex-flow: column;
  min-height: 100vh;
}

main {
  flex: 1;
}

```

## BFC(快级格式化上下文)

`BFC`是一个独立的渲染区域，只有`Block-level-box` 参与，它规定了内部的`Block-level-box`如何布局，并且与这个区域外面毫不相关。

白话文，孩子在家里愿意怎么折腾都行，但是出了家门，你就要乖乖的。

1. 元素的显示模式

> 元素有行内元素、快级元素、行内块元素

2. 哪些元素会具有`BFC`的条件

> 不是所有的元素模式都能产生`BFC`，`W3C`规范：`display` 属性为`block` 、`list-item` 、`table` 的元素，会产生`BFC`
3. 什么情况下可以让元素产生BFC
- `float` 属性不为`none`
- `position` 为`absolute` 或`fixed`
- `display` 为`inline-block` ，`table-cell` ，`table-caption` ，`flex`,`inline-flex`
- `overflow` 不为 `visible`
4. `BFC`元素所具有的特性
`BFC`布局规则特性：
- 在`BFC`中，盒子从顶端开始垂直地一个接一个地排列
- 盒子垂直方向的距离由`margin` 决定。属于同一个`BFC`的两个相邻盒子的`margin`会发生重叠
- 在`BFC`中，每一个盒子的左外边缘（margin-left）会触碰到容器的左边缘(border-left)（对于从右到左的格式来说，则触碰到右边缘）
5. `BFC`的主要用途
- 清除元素内部浮动
> 只要把父元素设为`BFC`就可以清理子元素的浮动了，最常见的用法就是在父元素是哪个设置`overflow: hidden`样式，对于`IE6`加上`zoom:1`就可以了。

主要用到了`BFC`的高度时，自然也会检测浮动的盒子高度。

- 解决外边距合并的问题
主要用到：
> 盒子垂直方向的距离由`margin`决定，属于同一个`BFC`的两个相邻盒子的`margin`会发生重叠。

属于同一个`BFC`的两个相邻盒子的`margin` 会发生重叠，那么我们创建不属于同一个`BFC`，就不会发生`margin` 重叠。

- 制作右侧自适应的盒子问题

主要用到：
> `BFC` 的区域不会与浮动盒子产生交集，而是紧贴着浮动边缘。

普通流体元素`BFC`后，为了和浮动元素不产生任何交集，顺着浮动边缘形成自己的封闭上下文。
6. `BFC`总结


## css 揭秘技巧

### 第一章

1. 半透明边框的实现方法

```css

div {
  border: 10px solid hsla(0, 0%, 100%, .5);
  background: skyblue;
  background-clip: padding-box; // 利用内边距的外延把背景裁剪掉
}

```
最终的效果：

![半透明边框实现效果](https://github.com/everast2015/css3/blob/master/css-scret-img/1-1.png)

2. 多重边框的解决方案

```css 
div {
  background: skyblue;
  box-shadow: 0 0 0 10px #655, 0 0 0 15px wheat;
  /* 利用box-shadow 可以设置多个投影的属性，可以设置页面的多重变量的问题 */
}
```

最终的效果：

![半透明边框实现效果](https://github.com/everast2015/css3/blob/master/css-scret-img/1-2.png)

另outline方案

两层边框的实现方案：

```css

div {
  background: skyblue;
  border: 10px solid wheat;
  outline: 5px solid green;
}
/* 最终的效果和box-shadow是一样的 */
```

4. 边框内圆角

```html

<div class="something-meaningful">
  <div>
    你的未来是怎样的，都是你说了算，自己的命运掌握在自己的手里
  </div>
</div>

.something-meaningful {
  background: #65;
  padding: .8em;
}

.something-meaningful div {
  background: tan;
  border-radius: .8em;
  padding: 1em;
}
```
![圆角实现的效果](https://github.com/everast2015/css3/blob/master/css-scret-img/1-4.png)

一个元素也可以达到这样的效果：
```css
div {
  background: wheat;
  border-radius: .8em;
  padding: 1em;
  box-shadow: 0 0 0 .6em #655;
  outline: .6em solid #655; 
  /* 这个属性的话，就是描述轮廓的，宽度，粗细，颜色值 */
}

```

最终的实现效果：

![一种效果实现内外圆角](https://github.com/everast2015/css3/blob/master/css-scret-img/1-4-1.png)

5. 条纹效果

```css
div {
  background: linear-gradient(#fb3, #58a);
}

```
我们看一下最终的效果：

![线性渐变可以实现条纹的效果](https://github.com/everast2015/css3/blob/master/css-scret-img/1-5.png)

两个色标拉近一些：

```css
div {
  background: linear-gradient(#fb3 20%, #58a 80%);
}

```
![线性渐变可以实现条纹的效果](https://github.com/everast2015/css3/blob/master/css-scret-img/1-5-1.png)

两个色标的值都是50%的时候，是什么效果：
如果都是50%的话，那就没有什么渐变的效果了，只有两块实色，各占据了background-image 一般的面积，本质上，我们创建了两条巨大的水平条纹

```css
div {
  background: linear-gradient(#fb3 50%, #58a 50%);
}

```
![线性渐变可以实现条纹的效果](https://github.com/everast2015/css3/blob/master/css-scret-img/1-5-2.png)


我们设置一个背景图像的大小:

```css
div {
  background: linear-gradient(#fb3 50%, #58a 50%);
  background-size: 100% 30px;
}

```

![线性渐变可以实现条纹的效果](https://github.com/everast2015/css3/blob/master/css-scret-img/1-5-3.png)

- 垂直条纹的实现













