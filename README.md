## 移动端适配方案


### 概念
- 单位英寸像素数（Pixel Per Inch，PPI）

现实世界的一英寸内像素数，决定了屏幕的显示质量

- dpr

`dpr` 是 `devicePixelRatio` 的简写，也就是`屏幕分辩比(设备像素比率)`


- 分辨率（Resolution）

屏幕区域的宽高所占像素数

- 完美视口

`<meta name="viewport" content="initial-scale=1.0,width=device-width,user-scalable=0,maximum-scale=1.0"/>`

- scale

`scale` 是屏幕拉伸比。也就是视口上的 `initial-scale` , `maximum-sacle` 等属性。

- 基准

以前是 iPhone 4 的 `320*480`， 现在更多的是 iPhone 6 的 `375*667`。

### 三种适配方案（推荐方案 2 ）

1. 固定宽度

固定宽度, `js` 动态修改 `viewport` 。

固定 640px 的宽度，viewport 640px 定宽，设计稿也是按照 640px 切。

缺点：让浏览器去缩放, 既然是缩放，那么就会失真，这是由于浏览器的自身渲染导致的。

优点：简单，粗暴，和pc页面一样的写，全是绝对定位。

2. rem

[flexible](https://github.com/amfe/lib-flexible)

3. flex