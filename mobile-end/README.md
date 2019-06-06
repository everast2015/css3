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



