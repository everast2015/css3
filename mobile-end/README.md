# 移动端

## 流式布局的概念

流式布局也就是百分比布局

## 移动web标准适配方案推导

1. 网页宽度必须和浏览器宽度一致
2. 默认显示的缩放比例和PC端保持一致
3. 不允许用户自行缩放网页

屏幕的像素和页面的尺寸的单位

什么是屏幕的像素（物理像素）

> 物理像素是设备显示屏的最小显示颗粒的大小

px 实际的网页的尺寸大小

## 移动端1px的解决的方案

为什么会出现移动端1px的问题？

主要的原因就是有些屏幕看起来会很粗的

1. `border-image`

```
   .border_1px{
          border-bottom: 1px solid #000;
        }
        @media only screen and (-webkit-min-device-pixel-ratio:2){
            .border_1px{
                border-bottom: none;
                border-width: 0 0 1px 0;
                border-image: url(../img/1pxline.png) 0 0 2 0 stretch;
            }
        }
```
## 移动web 浏览器的现状

移动web浏览器的注意事项：

1. 可以使用`jquery` 但是不建议。
2. `jquery` 做了很多桌面浏览器的兼容问题，但是移动端没有`IE`浏览器
3. 主流的浏览器，谷歌，火狐（2016年停止了维护和更新）`safari` 浏览器，百度，360
4. 内核基本上都是`webkit` 或者 `blink` 兼容`--webkit`
5. 使用一个`html api` 或者说使用一个叫做 `zepto.js` （基于高版本的浏览器开发的）


## 移动端reset重置样式

为所有的元素，设置为盒子模型，主要的目的就是为了防止内容的溢出，出现窗口不适配的问题。

```css
    *,
    *::before,
    *::after {
        margin: 0;
        padding: 0;
        box-sizing: border-box;

        /* 清除移动端点击高亮的效果 */
        -webkit-tap-hightlight-color: transparent;
    }
```
