# css最近问的越来越少了，只要会写常见的布局就ok，难点的答不出来也没事。相比移动端相关的会问题的比较多。

- 盒模型 [参考](https://www.jianshu.com/p/824eed8ce119)
  - 每个盒子由四个部分（或称区域）组成，其效用由它们各自的边界（Edge）所定义（原文：defined by their respective edges，可能意指容纳、包含、限制等）。与盒子的四个组成区域相对应，每个盒子有四个边界：内容边界 Content edge、内边距边界 Padding Edge、边框边界 Border Edge、外边框边界 Margin Edge。
  - 样式默认的方向的顺时针，上右下左
  - [盒模型完美解释](https://www.jianshu.com/p/aae29283f39e)
- positon的值，都是根据什么定位（注意下还有sticky）[参考](https://www.jianshu.com/p/a116022c6c99)
  - static  relative  absolute fixed 
  - fixed有兼容性的问题，ie6不支持
  - relative不会脱离文档流 absolute float会脱离文档流
  - 使用static 定位或无position定位的元素z-index属性是无效的
  - 将窗体自上而下分成一行行, 并在每行中按从左至右的顺序排放元素,即为文档流。
- 布局知识汇总 [参考](https://www.jianshu.com/p/f1657738b719)
  - 栅格布局的原理
  - 垂直居中布局 [参考](https://www.jianshu.com/p/d8db20f14e11)
  - 上中下布局，中间自适应 [参考](https://www.jianshu.com/p/30bc9751e3e8)
  - 左中右布局，中间自适应 [参考](https://www.jianshu.com/p/ffc6cbfa759b)
- 什么css可以减少重绘 [参考](https://www.jianshu.com/p/514809db1624)
  - 将多次修改样式合并为一次
  - 修改更为独立的节点
- 动画相关属性 [参考](https://www.jianshu.com/p/ffc44980d0f8)
  - transform: translate(x,y) rotate(100)
  - animation-duration, animatin-name
- 移动端适配方案（必考）[参考](https://www.jianshu.com/p/2c33921d5a68)
- 移动端适配1px的问题[参考](https://www.jianshu.com/p/d22ac00f3992)
- lineheight属性1.5和150%区别
  - 有单位时，子元素继承了父元素计算得出的行距；无单位时继承了系数，子元素会分别计算各自行距（推荐使用）。
```
  1） 当line-height:xxx %时：
body{ font-size:14px; line-height:150%; }
h1{ font-size:26px; }
实际是：
body{ line-height:21px; / 14px150%=21px / }
h1{ line-height:21px; } / 继承父元素计算出来的line-height ,21px */

2 ） 当line-height:x.x 时：
body{ font-size:14px; line-height:1.5; }
h1{ font-size:26px; }
实际是：
body{ line-height:21px; / 14px1.5=21px / }
h1{ line-height:39px; / 26px1.5=39px / }
```
- em和rem的区别 [参考](https://www.jianshu.com/p/da3844cedcf4)
  - rem 单位翻译为像素值是由 html 元素的字体大小决定的。 此字体大小会被浏览器中字体大小的设置影响，除非显式重写一个具体单位。
  - em 单位转为像素值，取决于他们使用的字体大小。 此字体大小受从父元素继承过来的字体大小，除非显式重写与一个具体单位。收到他所有祖先节点字体大小的影响
- [BFC(块级格式化上下文)](https://www.jianshu.com/p/66632298e355)
