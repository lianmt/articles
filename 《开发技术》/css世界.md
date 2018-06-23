CSS世界的诞生，就是为了图文信息展示服务的。

块级盒子、内联盒子（内在盒子、容器盒子）。块级盒子负责结构，内联盒子负责内容。
由外到内，display: inline-table; inline（内联） table （外联）

## 宽度
流动性，是一种margin/border/padding和content内容区域自动分配水平空间的机制。“无宽度，无图片，无浮动”。

“无宽度，借助流动性，采用宽度分离准则

![](https://upload-images.jianshu.io/upload_images/3317226-562a9ed4852c9c47.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

“包裹性”：

![](https://upload-images.jianshu.io/upload_images/3317226-542a2d7e295ecded.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

“首选最小宽度”：

 ![](https://upload-images.jianshu.io/upload_images/3317226-6e019257f44ab6eb.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

“最大宽度”：

![](https://upload-images.jianshu.io/upload_images/3317226-9b4c5f5534f66e43.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

设置了宽度，就形成了css盒子（块状），元素的流动性就丢失了：

![](https://upload-images.jianshu.io/upload_images/3317226-991e33ff96ecd003.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

“css流体布局下的宽度分离原则”

![](https://upload-images.jianshu.io/upload_images/3317226-0b8c0a31eb64bcd2.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

绝对定位支持隐式高度计算，充满父级高度

![](https://upload-images.jianshu.io/upload_images/3317226-f369b81474a4f03f.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

图片尺寸变化的本质是充满容器。
img无src属性时，浏览器不会请求资源，相当于span标签。
替换元素（img、video、textarea、iframe）和非替换元素的距离，就是src和content。

伪元素不算内容

![](https://upload-images.jianshu.io/upload_images/3317226-ee2559f5f817237e.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

## padding
padding、margin百分比值无论是水平方向还是垂直方向军事相对于宽度计算的。

内联元素默认的高度完全受font-size大小控制。

“三道杠”和双层圆点

![](https://upload-images.jianshu.io/upload_images/3317226-d289d61d24655870.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

## margin

![](https://upload-images.jianshu.io/upload_images/3317226-1990c13189cdef13.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

![](https://upload-images.jianshu.io/upload_images/3317226-eb155089d41578f3.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

margin + padding 实现等高布局

![](https://upload-images.jianshu.io/upload_images/3317226-4a3369596634cd87.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

## border

![](https://upload-images.jianshu.io/upload_images/3317226-8ae9c187339bb751.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

用border transparent扩大点击范围

元素边框高度总是和元素自身高度保持一致。
等高布局，用table-cell、margin + padding实现更兼容。

## 内联元素与流
























1
1
1
1
1
1
1
1
1
1
1
1
1
1
1
1
1
1
1
1
1
1
1
