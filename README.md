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
```

### 开门大吉源码
[door-open](https://github.com/yjn2015/CSS3)

1. 门关闭时的效果

![门关闭时的效果](https://github.com/yjn2015/CSS3/blob/master/door-open/door-close.png)

2. 门打开时的效果

![门打开时的效果](https://github.com/yjn2015/CSS3/blob/master/door-open/door-open.png)


