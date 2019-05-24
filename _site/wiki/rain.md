# 雨水/Rain
**输入效果名： 雨 或 rain**  
                 
[参考教程地址](https://www.bilibili.com/read/cv869584) 教程作者：冰叹 （bilibili.com）  

![](/demo/rain_demo.gif)  
_示例图片。原图来自《辉夜大小姐想让我告白》漫画111话，用[style2paints](https://github.com/lllyasviel/style2paints)上色而成。_

自动生成一个带有雨水效果的图层，雨水主要由分形杂色而不是CC Rainfall实现。其中有使用模糊特效，如果AE版本的整数部分大于13（即从版本14开始），则默认使用新版的高斯模糊，否则则使用旧版的快速模糊，两种版本产生的效果会有所不同。建议像原教程所说的，生成两层雨水并调整参数。