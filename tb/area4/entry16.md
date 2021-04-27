# []()【慢更】关于动画制作在MAD中的运用  
原作者 百度贴吧:冰凝咏叹调 [原地址](https://tieba.baidu.com/p/4817119755) 首发时间:2016-10-11 10:45  
最新获取时间:2021-04-26  
  
以下说明几点：  
1.达到同种效果的方法或许很多，但是我这里只做一种  
2.不讲调色，调色很少用  
3.只说说这将近一年来在工作上学习到的东西，分享出来，给大家学习  
4.慢更，所以，记得只看楼主  

1.涟漪的制作  
（1）新建400*400的合成，建立2个圆制作原形单元动画。  
效果图：  

![](/tb/area4/entry16_pic/0.jpg)
  
参数图：  

![](/tb/area4/entry16_pic/1.jpg)
  
  
（2）回到原合成 ，粒子批量生产  
效果图：  

![](/tb/area4/entry16_pic/2.jpg)
  
  
参数图：  

![](/tb/area4/entry16_pic/3.jpg)
  

![](/tb/area4/entry16_pic/4.jpg)
  

![](/tb/area4/entry16_pic/5.jpg)
  
  
单元为刚刚做的涟漪的合成。  
（3）画面扭曲先将粒子和单元预合成一下 调整图层——置换图来实现  
效果图：  

![](/tb/area4/entry16_pic/6.jpg)
  
  
参数：  

![](/tb/area4/entry16_pic/7.jpg)
  
  
具体参数可以按照需求调整  

2.雨的制作  
  
虽然有个插件（CC rain）可以一键生成，但是我感觉并不好看，所以还是用噪波（分形杂色）制作。  
  
最终效果图：  

![](/tb/area4/entry16_pic/8.jpg)
  
  
（1）第一层分形  
参数：  

![](/tb/area4/entry16_pic/9.jpg)
  
这里偏移要快点（具体看需求）： 我是3秒钟，-3000到10000  
  
（2）第二层分形，这里的2个分形都是加在同一层中  

![](/tb/area4/entry16_pic/10.jpg)
  
偏移和大小都不动，演化表达式：time*360，注意混合模式相乘  
  
（3）快速模糊与发光调节  

![](/tb/area4/entry16_pic/11.jpg)
  
  
  
  
这两个主要是调节柔度与亮度  
图层的叠加模式为颜色减淡或者叠加，并且打开3D层，调节透视  
  
PS：一般来说做一层是不对，至少要做2层，一层远景（雨滴小且密），一层近景（上面的所做的）， 所以有耐心的小伙伴，应该将人物和背景分开，拉开远近关系。  

（4）环形速度线的制作  
最前面的分形步骤一样，在建立完分形之后，加一个极坐标  

![](/tb/area4/entry16_pic/12.jpg)
  
就变成这样  

![](/tb/area4/entry16_pic/13.jpg)
  
然后我们放大，铺满屏幕  

![](/tb/area4/entry16_pic/14.jpg)
  
  
然后预合成，这部很关键。。。。  

![](/tb/area4/entry16_pic/15.jpg)
  
再画个圆形遮罩 ，这里的遮罩一定要羽化。  

![](/tb/area4/entry16_pic/16.jpg)
  
  
接着调整颜色，对比度，亮度  

![](/tb/area4/entry16_pic/17.jpg)
  
  
  
  
再将这两个预合成  
放大移动位置，焦点对准  

![](/tb/area4/entry16_pic/18.jpg)
  
  
最后调整下：  

![](/tb/area4/entry16_pic/19.jpg)
  

PS：现在有些动画的速度线添加了一些效果，比如 美术社和舞武器等等  

![](/tb/area4/entry16_pic/20.jpg)

![](/tb/area4/entry16_pic/21.jpg)
  
  
  
只需要对速度线添加画笔描边和毛边就可以做出差不多的效果：  

![](/tb/area4/entry16_pic/22.jpg)
  
  
参数一样，并不是什么固定参数，只是参考，特别注意，做这个粗糙速度线，一定要提高分形的对比度  

![](/tb/area4/entry16_pic/23.jpg)
  
  
速度线就说到这  

5.背光的制作  
文字说我也说不清，直接上图。  

![](/tb/area4/entry16_pic/24.jpg)
  
就是要做这样的效果。。。。。。  
  
（1）首先我们先随便构建一个画面  

![](/tb/area4/entry16_pic/25.jpg)
  
（2）给画面润色下，人物光的渐变，地面阴影，地面光线等等。。。。  

![](/tb/area4/entry16_pic/26.jpg)
  
巴拉巴拉。。。。。  
  
（3）背光透过光的制作  
  
首先预合成再添加一个白色背景  

![](/tb/area4/entry16_pic/27.jpg)
  
  
然后，是关键点，全部的最关键的地方  
  
复制一遍刚刚的合成，填充——选择背景颜色——反转，添加快速模糊（2015.3可以直接高斯模糊）重复边缘像素  
参数图：  

![](/tb/area4/entry16_pic/28.jpg)
  
  
模糊度控制透过光的大小  
  
效果图：  

![](/tb/area4/entry16_pic/29.jpg)
  
然后调节下曲线，因为背光所以暗点。  

![](/tb/area4/entry16_pic/30.jpg)
  
额，好像也没啥差别，具体看大家。。。  
  
（4）滤镜  
为了让光线更加柔和......  
  
原图：  

![](/tb/area4/entry16_pic/31.jpg)
  
  
  
滤镜后：  

![](/tb/area4/entry16_pic/32.jpg)
  

![](/tb/area4/entry16_pic/33.jpg)
  
滤镜参数：  
DF1：快速模糊 5  透明度50%        变亮  
DF2：快速模糊80  透明度30%       变亮  
  
都为原来的合成复制  

入射体积光的制作  
  
（1）新建 一层，添加分形杂色  

![](/tb/area4/entry16_pic/34.jpg)
  
  
演化：time*30  
缩放和旋转调整到适合的位置  

![](/tb/area4/entry16_pic/35.jpg)
  
  
新建纯色，亮度蒙版，给分形添加颜色  

![](/tb/area4/entry16_pic/36.jpg)
  
  

![](/tb/area4/entry16_pic/37.jpg)
  
  
  
（2）给这2层预合成一下  
添加快速模糊，发光，曲线调下颜色，叠加模式为相加，不透明度为80%  
开3D层调整下透视  

![](/tb/area4/entry16_pic/38.jpg)
  

![](/tb/area4/entry16_pic/39.jpg)
  

![](/tb/area4/entry16_pic/40.jpg)
  
  
画个遮罩  

![](/tb/area4/entry16_pic/41.jpg)
  
  

![](/tb/area4/entry16_pic/42.jpg)
  
  
就完成了  
  
然后随便添加点粒子用来做灰尘什么的。  

最后滤镜：  

![](/tb/area4/entry16_pic/43.jpg)
  
  
  
DF1：
![](/tb/area4/entry16_pic/44.jpg)
  
  
DF2：快速模糊35  
DF3：双向模糊 半径 30 阈值 120  
  
叠加模式和透明度和上面一样  
  

![](/tb/area4/entry16_pic/45.jpg)
  

毛刺现象  
RE0.第4集 16:30左右  

![](/tb/area4/entry16_pic/46.jpg)
  
  
  
我们按动画的来做  
  
（1）新建一个层，加入分形杂色  
记得类型选择块  
  

![](/tb/area4/entry16_pic/47.jpg)
  
关键帧为：time*3000 （可以多弄几层，加强一下）
![](/tb/area4/entry16_pic/48.jpg)
  
  
(2)将刚刚的分形预合成一下，记得选第二个  

![](/tb/area4/entry16_pic/49.jpg)
  
  
（3）添加调整图层，加入置换图  

![](/tb/area4/entry16_pic/50.jpg)
  
  
就好了：  
  

![](/tb/area4/entry16_pic/51.jpg)
  

玛德，贴吧的gif有毒  

![](/tb/area4/entry16_pic/52.jpg)
  

夜晚水面效果制作  
  
本篇比较长，比较乱，耐心看-  -  
  
  
原图：  
  

![](/tb/area4/entry16_pic/53.jpg)
  
  
  
准备工作：  
（1）一开始，先色调补正下，毕竟原本的图是白天……  
色调补正：  
  

![](/tb/area4/entry16_pic/54.jpg)
  
  
  

![](/tb/area4/entry16_pic/55.jpg)
  
  
用了纯色和曲线去调整，纯色提供一个冷色调，曲线提供明暗部调整  
  
（2）水面的思路就是利用分形来制作波纹反光和扭曲效果，所以先制作一个分形素材。  
第一层参数：  
  

![](/tb/area4/entry16_pic/56.jpg)
  

![](/tb/area4/entry16_pic/57.jpg)
  
  
第二层参数：  
把第一层复制一下，然后调整一下。  
  

![](/tb/area4/entry16_pic/58.jpg)
  

![](/tb/area4/entry16_pic/59.jpg)
  
  
第二层亮度蒙版  
  

![](/tb/area4/entry16_pic/60.jpg)
  
  
关键帧说明：  
第一层和第二层要错开，但是起始点要不同，我的起始点（第一帧）为上图所示。最后一帧下图所示。  
  

![](/tb/area4/entry16_pic/61.jpg)
  
  
效果图：  
  

![](/tb/area4/entry16_pic/62.jpg)
  
  
  
  
  

滤镜：  
最后一步，为上面的合成制作滤镜。  

![](/tb/area4/entry16_pic/63.jpg)
  
  
  
  
DF1：快速模糊10  
DF2：快速模糊45  
透过光源：建立一个纯色，打个遮罩，羽化500  

![](/tb/area4/entry16_pic/64.jpg)
  
  
  
色调补正：  
  
往蓝色调就对了。。。  

![](/tb/area4/entry16_pic/65.jpg)
  
  
发现暗角不够，再压一次。。。。  

![](/tb/area4/entry16_pic/66.jpg)
  
  
  
最后效果图：  

![](/tb/area4/entry16_pic/67.jpg)
  
  
  

![](/tb/area4/entry16_pic/68.jpg)
  
  
再吐槽一下，辣鸡贴吧，gif限制得要那么小  
  
  

嗨呀，今天没时间了。。。只能明天来写了，不过做完了倒是  

![](/tb/area4/entry16_pic/69.jpg)
  

海面环境的构建  
还是比较长，所以耐心看……  
原图：  

![](/tb/area4/entry16_pic/70.jpg)
  
  
  
效果图：  

![](/tb/area4/entry16_pic/71.jpg)
  
  

![](/tb/area4/entry16_pic/72.jpg)
  
  
  
  
分成3个部分：天空的构建，海面的构建以及整体的合成  

天空的构建  
  
（1）新建一个纯色，添加梯度渐变，做天空的颜色  

![](/tb/area4/entry16_pic/73.jpg)
  
  

![](/tb/area4/entry16_pic/74.jpg)
  
  
  
  
渐变颜色为：上面的是43B0EE   下面的B4F7FB  
  
（2）新建纯色，添加分形杂色和快速模糊制作云层  

![](/tb/area4/entry16_pic/75.jpg)
  
  
关键帧（3S）：湍流是（640,360）——（640,500）   演化是time*50  
  
快速模糊 模糊度为15  
  
两层分形的图层的叠加模式改为屏幕  
  
（3）复制一层刚刚第二步做的云，把演化改为time*150，快速模糊的模糊度改为83  
  
  
（4）回到外面合成（720P的），把刚刚的天空合成加进去，打开3d层，X轴旋转77°，位置为（637.7,109.8,330.8），自己觉得好看的位置就行。再添加线性擦除。  

![](/tb/area4/entry16_pic/76.jpg)
  
  
  
  

![](/tb/area4/entry16_pic/77.jpg)
  
  
效果图：  

![](/tb/area4/entry16_pic/78.jpg)
  

整体合成  
  
（1）可以看出中间有条黑线。  
给最下面添加一个纯色，颜色为D9EFFF  

![](/tb/area4/entry16_pic/79.jpg)
  
  
  
（2）再添加一个纯色，EEF8FF，画个遮罩（羽化300），图层模式为相加，做远处亮光  

![](/tb/area4/entry16_pic/80.jpg)
  
  
添加一个调整图层，加入高斯模糊，模糊度为1000，遮罩和上面一样，羽化改为30  

![](/tb/area4/entry16_pic/81.jpg)
  
  
  
（3）对人物进行简单处理。  
打个阴影，调个曲线。 打开3d层，调整下透视。  

![](/tb/area4/entry16_pic/82.jpg)
  

![](/tb/area4/entry16_pic/83.jpg)
  
  
  
（4）添加光和彩虹，这个按个人喜好……我是用of做的  

![](/tb/area4/entry16_pic/84.jpg)
  

滤镜添加  
  

![](/tb/area4/entry16_pic/85.jpg)
  
  
不透明度和叠加模式  
  
DF1  快速模糊5  
DF2  快速模糊40  
T光  就是眼睛高光和文乃头上发卡的反光  

![](/tb/area4/entry16_pic/86.jpg)
  
  
透射光  颜色A8E7FF 遮罩羽化800  

![](/tb/area4/entry16_pic/87.jpg)
  
  
  
蓝色补正  

![](/tb/area4/entry16_pic/88.jpg)
  
  
  
镜头模糊  

![](/tb/area4/entry16_pic/89.jpg)
  
  
就是提升焦点，给周围一圈模糊，一点点就好  
  
就完成了  

第9期太长了，所以我把工程放出来给大家  
http://pan.baidu.com/s/1slKoBgh  

  
10.LED屏幕效果  
  
  
原图：  

![](/tb/area4/entry16_pic/90.jpg)
  
  
  
效果图：  
  
  

![](/tb/area4/entry16_pic/91.jpg)
  
  
（1）将项目改为32bpc，这点挺重要的  

![](/tb/area4/entry16_pic/92.jpg)
  
  
增加对光的信息采集  
  
（2）对图片简单的调整  
做个动画什么的  

![](/tb/area4/entry16_pic/93.jpg)
  
  

![](/tb/area4/entry16_pic/94.jpg)
  
  
图片一定要比较暗，要不然做完之后会超级亮。  
  
（3）对合成添加CC滚珠（cc ball action）和发光  

![](/tb/area4/entry16_pic/95.jpg)
  
  
就会得到这样的图：  

![](/tb/area4/entry16_pic/96.jpg)
  

  
(5)复制一下合成  
更改下特效参数  

![](/tb/area4/entry16_pic/97.jpg)
  
  
再添加out of focus  

![](/tb/area4/entry16_pic/98.jpg)
  
  
  
将图层模式改为线性光，透明度为30%  

![](/tb/area4/entry16_pic/99.jpg)
  
  
  
（6）光线的制作  
新建一个纯色，添加cc spotlight  

![](/tb/area4/entry16_pic/100.jpg)
  
  
  
  
  
图层模式改为相加  

![](/tb/area4/entry16_pic/101.jpg)
  
  
  
完成  
  

![](/tb/area4/entry16_pic/102.jpg)
  

周末不更![](/tb/area4/entry16_pic/103.jpg)  

![](/tb/area4/entry16_pic/104.jpg)想我没，我又来更了  

3.pl粒子的制作  
  
（1）新建一层，添加pl粒子，添加基本体，透明度调为100%（旧版本和这个可能有点不一样，不过差不多啦）  

![](/tb/area4/entry16_pic/105.jpg)
  
  
  
（2）然后我们发现点太小了，点开点属性的面板。  

![](/tb/area4/entry16_pic/106.jpg)
  

![](/tb/area4/entry16_pic/107.jpg)
  
  
  
（3）pl粒子制作的优点  
①你可以在effect里面添加noise  

![](/tb/area4/entry16_pic/108.jpg)
  
  
由整变乱  
  
②添加线  

![](/tb/area4/entry16_pic/109.jpg)
  

![](/tb/area4/entry16_pic/110.jpg)
  
  
通过改变最大距离得到一些网格图案  
  
③添加三角形得到一些效果比较酷的图案  

![](/tb/area4/entry16_pic/111.jpg)
  
  
  
等等等等  
  
  
  
4.最简便的做法，添加蓝宝石。。。。。  

![](/tb/area4/entry16_pic/112.jpg)
  
  
这三个都可以做，不过我比较不推荐这么做，因为局限性比较大，而且我也不熟，就不多讲了……  
  
  
5. 可以简单处理下，新房风_(:з)∠)_  

![](/tb/area4/entry16_pic/113.jpg)
  

近期更不了了，不过不是不更了，就是晚点再来，要研究和整理点东西，下期大概是滤镜的使用规律  

1）首先，我们拿一张图过来（先感谢Miv4t国际版第一的图）  
原图：  

![](/tb/area4/entry16_pic/114.jpg)
  
  
  
分析：原图背景是暗调，所以我们可以把这个当做是带有火光的夜晚，突出火光，然后散射以为弱光所以较低。  
加完散射光之后：  

![](/tb/area4/entry16_pic/115.jpg)
  
  

![](/tb/area4/entry16_pic/116.jpg)
  
  
  
  
DF1：快速模糊5  小边缘散光  
DF2：快速模糊30  大边缘柔和散光  
  
人物整体变亮并且突现出光晕的效果。  
  
之后为了突现火光环境，增加一个暖色补正  

![](/tb/area4/entry16_pic/117.jpg)
  
  

![](/tb/area4/entry16_pic/118.jpg)
  
  
  
  
  
  
火光的夜晚的一般就是这样的步骤，当然还有打光的那个步骤，但是因为是插画所以就不再补充光线。  

（2）第一步你可能看不出什么感觉，所以这里就再说一些。  
比如我们给saber加一个圣光效果。  

![](/tb/area4/entry16_pic/119.jpg)
  
  
先用固态层+遮罩做一个这样的图形  

![](/tb/area4/entry16_pic/120.jpg)
  
  
将模式改为柔光  

![](/tb/area4/entry16_pic/121.jpg)
  
  
  
  
复制一层，改下大小和羽化值  

![](/tb/area4/entry16_pic/122.jpg)
  

![](/tb/area4/entry16_pic/123.jpg)
  
  
  
  
  
  
将刚刚复制那层模式改为叠加。调整一下透明度就可以得到这样的图。  
  
所以滤镜的具体使用并不全是按照环境决定，有时候也会根据所需效果为主体去调整。  

最后是滤片：  
滤片一般就是使用固态层，叠加模式改为颜色，进而改变整体色调。  

![](/tb/area4/entry16_pic/124.jpg)
  
  
记得调整透明度  

![](/tb/area4/entry16_pic/125.jpg)
  

![](/tb/area4/entry16_pic/126.jpg)
  
  
  
  
  
这是冷暖2种滤片可以发现差异非常大，也会直接破坏（覆盖）原有色调，所以非必要其实少用，如果你发现画面无法融合，这是一个好方法。  
  

![](/tb/area4/entry16_pic/127.jpg)
  
  
  
当然你可以添加渐变来做出薄暮的效果，比如k就用到了很多这种效果，不过k的叠加模式颜色，而是叠加或者其他  

![](/tb/area4/entry16_pic/128.jpg)
  

接着就是明暗的补正：  
明暗补正一般通过色阶和曲线来实现，不过色阶，我一般比较不用，所以在这里就讲讲曲线。  

![](/tb/area4/entry16_pic/129.jpg)
  
  
  
  
曲线的调整趋势，一般就是这样，选择中间直线线上的点往左上走就是变亮，往右下走就是变暗，线上的点分布是：左下——右上是暗部——亮部。  
  
  
  
  
  
  
  
  
  

![](/tb/area4/entry16_pic/130.jpg)
  

![](/tb/area4/entry16_pic/131.jpg)
  
  
S型曲线：加高对比度，因为可控性比直接调整对比度高，所以我一直用这个调整对比度。  
  

![](/tb/area4/entry16_pic/132.jpg)
  

![](/tb/area4/entry16_pic/133.jpg)
  
  
加亮曲线：有时候大家做mad做到那种治愈，唯美什么的可以使用这种有奇效。  

![](/tb/area4/entry16_pic/134.jpg)

![](/tb/area4/entry16_pic/135.jpg)
  
  
加暗曲线：我一般都不用，如果画面太亮又做比较压抑效果的可以用这个。  

前面那图我们做了圣光效果，所以这里尝试用滤镜做一下模糊高亮效果：  

![](/tb/area4/entry16_pic/136.jpg)
  
  

![](/tb/area4/entry16_pic/137.jpg)
  
  
DF1：快速模糊5  
DF2：快速模糊65  

![](/tb/area4/entry16_pic/138.jpg)
  
  
曲线不要太过就行，按感觉走  
  
接着我们来总结一下滤镜的流程顺序：  
  
1.散光（DF），画面整体的扩散效果，利用散光效果达到整体融合。方法都为复制原图像添加模糊调整透明度。  
2.颜色补正（色相），利用色相将一些画面中不太如意颜色调整色相和饱和度亮度。  
3.滤片（纯色——颜色），改变整体的色调。  
4.明暗补正（曲线），亮部暗部的调整以及对比度的高低。  
  
做完这些一般滤镜就完成了，还有一些其他的按照需要调整，比如：曝光度啊，曲线的RGB等等。  
  
这里整理列举一些常见环境的滤镜参数：  
因为颜色补正和明暗补正是根据具体画面来做的，所以不全部列入归纳  
  

![](/tb/area4/entry16_pic/139.jpg)
  

周末不更，诶嘿嘿  

原图  

![](/tb/area4/entry16_pic/140.jpg)
  

14.火焰环境的构建  
这次一样比较长，耐心一步步来。  
原图：  

![](/tb/area4/entry16_pic/141.jpg)
  
  
最终效果：  

![](/tb/area4/entry16_pic/142.jpg)
  

![](/tb/area4/entry16_pic/143.jpg)
  
  
因为太长了，所以后续的什么滤镜就没做了……  
  
  
1.火焰的制作  
主要思路就是粒子，额，粒子- -  
  
（1）火焰基础部分的制作  
新建一纯色，添加p粒子，改了挺多属性的，所以要对好。  

![](/tb/area4/entry16_pic/144.jpg)
  

![](/tb/area4/entry16_pic/145.jpg)
  

![](/tb/area4/entry16_pic/146.jpg)
  
  
  
  
生命期颜色：左FF6100   右F34400  
物理学：  

![](/tb/area4/entry16_pic/147.jpg)
  
  

![](/tb/area4/entry16_pic/148.jpg)
  
  
  
效果图：  

![](/tb/area4/entry16_pic/149.jpg)
  
  
  
然后加入定向模糊，模糊长度为15  

![](/tb/area4/entry16_pic/150.jpg)
  
  
  
  
  
  
  

（2）内焰的制作  
把刚才制作的基础复制一份，将粒子大小调到10  
  
（3）火焰蒸汽的制作  
新建一个纯色，添加分形  

![](/tb/area4/entry16_pic/151.jpg)
  
  
对偏移和演化添加动画关键帧，这个随意。。。  
  
添加色阶调节  

![](/tb/area4/entry16_pic/152.jpg)
  
  
  
添加发光  

![](/tb/area4/entry16_pic/153.jpg)
  
  
湍流置换的演化打上动画关键帧，数值随意  

![](/tb/area4/entry16_pic/154.jpg)
  
  
画遮罩，羽化值随意（70左右吧）  
  
将图层模式改为屏幕。  

![](/tb/area4/entry16_pic/155.jpg)
  
  
  
  
（4）余烬（火星）的制作  
也是用粒子制作，新建纯色，添加p粒子。  

![](/tb/area4/entry16_pic/156.jpg)
  
  

![](/tb/area4/entry16_pic/157.jpg)
  
  

![](/tb/area4/entry16_pic/158.jpg)
  
  
  

![](/tb/area4/entry16_pic/159.jpg)
  
  
  
  
  
  
4层的位置  

![](/tb/area4/entry16_pic/160.jpg)
  

（5）整体调整  
将4层预合成，添加曲线，调整颜色  

![](/tb/area4/entry16_pic/161.jpg)
  

![](/tb/area4/entry16_pic/162.jpg)
  
  
  
  
  
  
  
2.添加环境光  

![](/tb/area4/entry16_pic/163.jpg)
  
  
添加一个橙色，屏幕，透明度5%  
  
将环境光1复制，透明度改为30%，画遮罩  

![](/tb/area4/entry16_pic/164.jpg)
  
  
  
透明度写上表达式：wiggle(5,8)  
  

第16期，这次是简易的动画摄影制作  
  
上班的最后一天就写一篇比较完整给大家学习作为新年礼物吧_(:з)∠)_  
首先我拿的素材是日文教材的（工程已经帮大家翻译完了），所以大家最好还是去下载一下，我会把素材和工程都放出来。  
  
原图：  

![](/tb/area4/entry16_pic/165.jpg)
  
  
  
效果图：  

![](/tb/area4/entry16_pic/166.jpg)
  

1.合成，这里要对着摄影表排帧和按照设计稿调整构图，有兴趣的可以去了解下。  

![](/tb/area4/entry16_pic/167.jpg)
  
  
这镜动画的摄影表。吧AE的时间轴顺时针旋转90度再水平翻转就是这样的图像。  
  
  
  
  
新建合成，命名为1.合成  
  
①更改颜色  
冲击特效填充为红色，剑光为蓝色渐变  
冲击特效  
添加色相（记得彩色化，当然你直接填充也可以），发光和定向模糊  

![](/tb/area4/entry16_pic/168.jpg)
  

![](/tb/area4/entry16_pic/169.jpg)
  

![](/tb/area4/entry16_pic/170.jpg)
  
  
  
  
  
然后发现不够冲击力所以我们复制一层  
发光和色相不变，把定向模糊改为CC light burst  

![](/tb/area4/entry16_pic/171.jpg)
  
  
图层模式改为相加  

![](/tb/area4/entry16_pic/172.jpg)
  
  
  
注：冲击的破片就是C层也是这么做  

剑光  
剑光为渐变蓝色，所以我们添加蓝色和黑色的渐变（具体颜色数值这期都不给了，记得下工程自己做一遍啊）。  

![](/tb/area4/entry16_pic/173.jpg)
  
  
因为动画的关系，所以渐变的2个点要按照动画去K帧，MAD中如果做形状层刀光我也是这么做的（不知道有啥不用K的方法么- -）。  

![](/tb/area4/entry16_pic/174.jpg)
  
  
再添加发光和模糊，让它亮起来  
  
  

![](/tb/area4/entry16_pic/175.jpg)
  

![](/tb/area4/entry16_pic/176.jpg)
  
  
  
  
  
更改图层模式为相加，然后和接触的物体（冲击波）预览一遍  
  

![](/tb/area4/entry16_pic/177.jpg)
  
  
发现因为叠加模式的关系，所以叠一起的时候，刀光会变得很淡，不清晰，所以接触的这几帧我们复制一层  

![](/tb/area4/entry16_pic/178.jpg)
  
  
  

②速度感模糊的制作  
先把人物的高光色和正常色排好。  
人在挥剑的时候会产生速度模糊，所以我们通过定向模糊来制作  
添加一层调整图层，添加定向模糊  

![](/tb/area4/entry16_pic/179.jpg)
  
  
  
  
  
  
绘画遮罩，只对手臂和剑绘制  

![](/tb/area4/entry16_pic/180.jpg)
  
  
  
添加前：  
  
  

![](/tb/area4/entry16_pic/181.jpg)
  
  
  
添加后  

![](/tb/area4/entry16_pic/182.jpg)
  
  
  
然后下一帧添加剑的速度模糊  

![](/tb/area4/entry16_pic/183.jpg)
  
  
  
记得遮罩和模糊方向  

![](/tb/area4/entry16_pic/184.jpg)
  
  
  
这些都是要K帧………..  

③环境光  
冲击波所产生的环境光效  
新建形状层，添加红黑渐变  

![](/tb/area4/entry16_pic/185.jpg)
  
  
模式为相加  

![](/tb/area4/entry16_pic/186.jpg)
  
  
因为撞击的时候突出画面，所以光效要加强。  
  
所以我们在撞击处加上渐变  

![](/tb/area4/entry16_pic/187.jpg)
  

![](/tb/area4/entry16_pic/188.jpg)
  

![](/tb/area4/entry16_pic/189.jpg)
  
  
  
  
  
  
  
2层的叠加模式看上图。  

④人物阴影斜光  
突出撞击，所以在人物的阴影面加上放射状的投影。  
复制一层人物高光色，添加CC light burst  

![](/tb/area4/entry16_pic/190.jpg)
  

![](/tb/area4/entry16_pic/191.jpg)
  
  
  
  
  
按照摄影表的要求终于合成这一步完成了。  

17.这次是做下极光的效果  
  
  
主要运用的是shine,分形澡波和形状层  
因为我这里的shine出了点问题，开了3D没反应，所以做起来有点奇怪，就当抛砖引玉了。  
原本要做这样的  

![](/tb/area4/entry16_pic/192.jpg)
  
  
最后变成这样了  

![](/tb/area4/entry16_pic/193.jpg)
  
  
  
1.基础的制作  
先用形状层画一个圆  

![](/tb/area4/entry16_pic/194.jpg)
  
打开3d层，然后调整位置  

![](/tb/area4/entry16_pic/195.jpg)
  

![](/tb/area4/entry16_pic/196.jpg)
  
  

分形制作  
新建固态层，添加分形杂色，  

![](/tb/area4/entry16_pic/197.jpg)
  
演化表达式：time*150  

![](/tb/area4/entry16_pic/198.jpg)
  
将分形这层的这个地方点开（有点像PS的剪切蒙版，向下Alpha蒙版）  
  

![](/tb/area4/entry16_pic/199.jpg)
  
就能得到这样一个斑点圈  
  
星星的分形也是一样  

![](/tb/area4/entry16_pic/200.jpg)
  
  
之后预合成一下，星星和圆圈要分开  

![](/tb/area4/entry16_pic/201.jpg)
  
  
  
2.动态的制作  
因为shine出了问题，所以不能开3D灯光，就不能让星星旋转，只能做绘画动画了  
  

![](/tb/area4/entry16_pic/202.jpg)
  
对形状层添加修建路径，然后 内容——修建路径——对开始或者结束K帧  
  

忘了加GIF了....  

![](/tb/area4/entry16_pic/203.jpg)
  

线条提取&水墨遮罩  
这期其实可以算是番外了，因为动画制作的时候不会用这用提取线条。不过竟然目的是做mad，就一起写出来。  
提取线条的主要思路就是利用卡通特效选择边缘再调整数值实现。  
这里的例子是：线条展现——黑白上色——最后变为彩色  

![](/tb/area4/entry16_pic/204.jpg)
  

![](/tb/area4/entry16_pic/205.jpg)
  
  
  
  
  
  
  
线稿提取：  
添加图片，给图片预合成下命名为线稿提取（这样就以后替换图片方便），添加卡通特效  

![](/tb/area4/entry16_pic/206.jpg)
  
  
记得渲染选择边缘，主要调节边缘中的阈值和柔和度  
  
再将添加完特效的合成预合成下，记得选择第二个  

![](/tb/area4/entry16_pic/207.jpg)
  
  
然后合成的叠加模式选择相乘  
  

![](/tb/area4/entry16_pic/208.jpg)
  
  

![](/tb/area4/entry16_pic/209.jpg)
  
  
  
  
  
下面的纸张纹理，大家随便搜搜都有不一定要这样的纹理，根据需求而定。  


![](/tb/area4/entry16_pic/210.jpg)
  

黑白填充  
这步同样是添加卡通特效，把刚刚的图片合成再拿过来，添加卡通特效  

![](/tb/area4/entry16_pic/211.jpg)
  
  
这里主要把细节半径关到0，边缘增强调到100，边缘黑色阶调高就会让线变成色块。  
  

![](/tb/area4/entry16_pic/212.jpg)
  
  
  
之后和上一部分一样，预合成，模式调为相乘  

![](/tb/area4/entry16_pic/213.jpg)
  
  
  
最后就是彩色。。。。  
额。不用调  
  

然后就是遮罩  
遮罩我用的是拆模板之后的素材。  
  

![](/tb/area4/entry16_pic/214.jpg)
  

![](/tb/area4/entry16_pic/215.jpg)
  
  
  
  
  
一些水墨的什么的，所以大家平时要记得素材的积累。  
  
将素材作为素材，三层都遮罩设置一下  

![](/tb/area4/entry16_pic/216.jpg)
  
  
  
  
  
再排序一下就能得到很好的转场效果  

![](/tb/area4/entry16_pic/217.jpg)
  
最后再调色一下，就得到这样的效果。  

![](/tb/area4/entry16_pic/218.jpg)
  
因为呢，这次也没啥复杂的东西，所以也就不放工程了。  


![](/tb/area4/entry16_pic/219.jpg)
  

再建立一个半径为30的球体，放进去就完成了  

![](/tb/area4/entry16_pic/220.jpg)
  
  
  
  
  
  
  
（5）尾部  
如果你前面都搞懂的话，最后的尾部就很快  
  
新建立方体，调整位置，然后对称，选择XY轴，完成。  
  

![](/tb/area4/entry16_pic/221.jpg)
  
  

![](/tb/area4/entry16_pic/222.jpg)
  
  
  
  
  
  
  
（6）材质  
看最终图就2个材质，一个是主体偏白材质，一个是中间球体黑色材质。  
新建2个材质。  
  
  

![](/tb/area4/entry16_pic/223.jpg)
  
  

![](/tb/area4/entry16_pic/224.jpg)
  

分别赋予材质  

![](/tb/area4/entry16_pic/225.jpg)
  
  
CTRL+R 预览一下  

![](/tb/area4/entry16_pic/226.jpg)
  
  
  
  
  
2.场景的构建  
  

![](/tb/area4/entry16_pic/227.jpg)
  
  
场景都是简单的几何体拼凑而成，就讲一个中间很多立方体排列怎么做的。  
  
新建立方体，然后调整大小  

![](/tb/area4/entry16_pic/228.jpg)
  
  
添加阵列方块，把立方体设为方块的子级  

![](/tb/area4/entry16_pic/229.jpg)
  
  
  
  

3.粒子发射  
运动物理后面的小方块漂浮主要是靠粒子发射  

![](/tb/area4/entry16_pic/230.jpg)
  
  
  
首先我们先创建发射器。上方菜单模拟——粒子——发射器  

![](/tb/area4/entry16_pic/231.jpg)
  
  
  
  
  
  
新建立方体，把立方体设为发射器的子级  

![](/tb/area4/entry16_pic/232.jpg)
  
  
  
点击发射器，在粒子选单中，勾选显示对象  

![](/tb/area4/entry16_pic/233.jpg)
  

给粒子的填充对象（立方体）添加材质，调整粒子参数和发射器大小，把发射器绑到运动物体上（设为子级）。是不是很像p粒子的操作啊，对，没错，就是这样的操作。  
  
  

![](/tb/area4/entry16_pic/234.jpg)
  
  

![](/tb/area4/entry16_pic/235.jpg)
  
  

![](/tb/area4/entry16_pic/236.jpg)
  
  
  
  
  
物体样条运动和摄像机运动比较复杂，下次有空再说吧。  
  
  

4.背景&全局光  
新建天空，地面，背景。把地面设为背景的子级  
  

![](/tb/area4/entry16_pic/237.jpg)
  
  

![](/tb/area4/entry16_pic/238.jpg)
  
  
  
  
  
  
  
  
  
右键，给地面和天空添加合成标签  

![](/tb/area4/entry16_pic/239.jpg)
  
  
  
标签里勾上合成背景  

![](/tb/area4/entry16_pic/240.jpg)
  
  
点击下图的渲染设置，点击效果——全局光照  
  
  

![](/tb/area4/entry16_pic/241.jpg)
  
  

![](/tb/area4/entry16_pic/242.jpg)
  

把渲染调到物理渲染器  

![](/tb/area4/entry16_pic/243.jpg)
  
  
  
  
CTRL+R预览  

![](/tb/area4/entry16_pic/244.jpg)
  
  
  
  
当然C4D还可以做物理反弹什么的，比ae的牛顿插件好。  
  

![](/tb/area4/entry16_pic/245.jpg)
  
  
  

![](/tb/area4/entry16_pic/246.jpg)
  
  
  
  
  
  
  
  
最后，你需要输出序列帧，然后导入ae做效果，这个也好长啊，大家可以百度的_(:з)∠)_  

然后你还可以导入mmd这么玩，瞎几把玩，GTA等着你23333333  
  
  

![](/tb/area4/entry16_pic/247.jpg)
  
  

![](/tb/area4/entry16_pic/248.jpg)
  
  
  
  
  
工程下载：  
链接：http://pan.baidu.com/s/1pKJ9zcf  

@宫永or丰音  

![](/tb/area4/entry16_pic/249.jpg)
  
  
这种吗  

应该是第20期了吧，写了这个系列也半年多了，玛徳，物哀一下……  
最近一直在工作，到现在也还没找到，所以一直没空更，抽空感觉更更。  
  
湍流置换(Turbulent Displace )对于形状层的应用  
  
这次主要就制作下REC 13话ED中的效果和动画人物特殊边缘（做的也不是很像就是）  

![](/tb/area4/entry16_pic/250.jpg)
  

![](/tb/area4/entry16_pic/251.jpg)
  
  
  
  
1.REC 13话ED  
  
（1）新建一个描边圆的形状层  

![](/tb/area4/entry16_pic/252.jpg)
  
  
（2）添加湍流置换(Turbulent Displace )效果，数量100 大小 100 复杂度 6，并对演化添加表达式：time*50。  

![](/tb/area4/entry16_pic/253.jpg)
  

![](/tb/area4/entry16_pic/254.jpg)
  
  
（3）对形状层的描边宽度和比例k帧。  
描边宽度：20到0  
比例：0到你想要的大小  
然后关键帧F9，或者调下曲线  

![](/tb/area4/entry16_pic/255.jpg)
  

![](/tb/area4/entry16_pic/256.jpg)
  

![](/tb/area4/entry16_pic/257.jpg)
  
  
（4）发光润色，如下图，中间的发光是默认  

![](/tb/area4/entry16_pic/258.jpg)
  

（5）直线，其实一样的，就是把圆的比例改成为修建路径去k帧，并且修改一下湍流置换的值。  

![](/tb/area4/entry16_pic/259.jpg)
  

![](/tb/area4/entry16_pic/260.jpg)
  
  
  
  
  
2.动画人物特殊边缘（爱酱）  
（1）导入图片，然后扣下图，预合成一下  

![](/tb/area4/entry16_pic/261.jpg)
  
  
（2）复制合成，添加Distance Gradation，就是描边，没有这个插件的，我会放在后面的工程下载里，到时候大家弄一下就好了。参数如下图。  

![](/tb/area4/entry16_pic/262.jpg)
  

![](/tb/area4/entry16_pic/263.jpg)
  
  
（3）对描边添加2个湍流置换。并且偏移K帧往上移动就行（速度自己定下吧），演化表达式：time*100  

![](/tb/area4/entry16_pic/264.jpg)
  

![](/tb/area4/entry16_pic/265.jpg)
  
  
  
(4)添加CC Vector Blur让它有点模糊变化  

![](/tb/area4/entry16_pic/266.jpg)
  
  

![](/tb/area4/entry16_pic/267.jpg)
  

（5）添加快速模糊，投影与发光，润色一下  

![](/tb/area4/entry16_pic/268.jpg)
  

![](/tb/area4/entry16_pic/269.jpg)
  
（6）然后我们发现发光的不够，需要增加一点扩散光  
复制一层刚刚做的边缘，快速模糊改为60，发光的发光半径改为95，叠加模式改为相加，不透明度改为78%。  

![](/tb/area4/entry16_pic/270.jpg)
  
  
（7）对爱酱进行点调色。  
对源层添加曲线和曝光度。  

![](/tb/area4/entry16_pic/271.jpg)
  

![](/tb/area4/entry16_pic/272.jpg)
  
  
（8）复制一层刚刚添加特效的爱酱，删除曝光度，添加色光与快速模糊  
色光的输出循环使用预设火焰，然后叠加模式改为变暗，调整不透明度为46%  

![](/tb/area4/entry16_pic/273.jpg)

![](/tb/area4/entry16_pic/274.jpg)
  
  
  
  

21.saber的运用  
  
  
这期是对上期（20期）的一个补充，就是另外的做法，因为那个实在太麻烦了，而且插件也好冷，所以这个21就用saber来做，简短的讲解下思路。（电脑终于好了XD  
这次用到的插件：saber，UnMult  
爱酱：
![](/tb/area4/entry16_pic/275.jpg)
  
原图：
![](/tb/area4/entry16_pic/276.jpg)
  
完成图：
![](/tb/area4/entry16_pic/277.jpg)
  
说明：在MAD中可以用于GAL提取的立绘运用，如果是抠图的话可以跳过前面几步，直接上saber。  
（1）这次用到的素材和上次一样都是大平摄影书的素材。将人物前后（因为色调所以它画了2层）合成一个合成。  
  

![](/tb/area4/entry16_pic/278.jpg)
  
  
（2）这步非常关键，可以说全部的核心，就是利用ae自带功能生成mask，如果你是动抠的话就已经有mask了，可以跳过这部分。  
选择图层——自动轨迹，英文版位置如下。  
  
  
  
  

![](/tb/area4/entry16_pic/279.jpg)
  
  
将时长选择工作区，勾上生产新层。  

![](/tb/area4/entry16_pic/280.jpg)
  
  
  
  
  
  
  
然后我们就会得到这样一个层  

![](/tb/area4/entry16_pic/281.jpg)
  

（3）对刚才自动轨迹生成的层添加saber，你会发现出现一条激光，没有啥效果  

![](/tb/area4/entry16_pic/282.jpg)
  
展开自定义主体，主体类型选择遮罩图层，渲染设置选择遮罩核心。  

![](/tb/area4/entry16_pic/283.jpg)
  
  
接着调整预设，选择你喜欢的预设。并且对主体大小K帧。把saber层移动到人物层下面。  

![](/tb/area4/entry16_pic/284.jpg)
  
  
（4）打开所有层，你会发现背景被黑色遮住了。对saber层添加UnMult（去黑）。  

![](/tb/area4/entry16_pic/285.jpg)
  
  
完成。  

![](/tb/area4/entry16_pic/286.jpg)
  
  
  
（5）其他  
Saber选项中选择启用遮罩，你会得到简单的双重曝光（好像是叫这个）wwww  

![](/tb/area4/entry16_pic/287.jpg)
  
  
选择遮罩辉光或者遮罩核心，调整下参数……  

![](/tb/area4/entry16_pic/288.jpg)
  

![](/tb/area4/entry16_pic/289.jpg)
  
  
总结下，就是利用自动轨迹生成边缘mask，然后添加saber，利用saber生成光效，再用UnMult去黑。  
  
工程文件里有saber插件。  
  
下载地址： 链接：http://pan.baidu.com/s/1boIb30j 密码：n3pf  

22.宝石的制作  
  
  
看了3集宝石之国，现在对一堆宝石非常关注23333.然后有天动画摄影群的小伙伴发了个PS制作宝石的奇技淫巧，就想着来用AE试试。  
（感谢大触分享）  

![](/tb/area4/entry16_pic/290.jpg)
  
  
  
  
宝石的制作  
  
用到的主要还是分形杂色（Fractal Noise），色调方面直接用曲线（Curves）（Curves）  

![](/tb/area4/entry16_pic/291.jpg)
  

![](/tb/area4/entry16_pic/292.jpg)
  
  
  
  
  
  
粒子（Particular）批量之后：  

![](/tb/area4/entry16_pic/293.jpg)
  
  

1.宝石的反射面制作（表面）  
  
新建固态层（Solid），黑色的- -  
  
新建固态层（Solid），添加分形杂色（Fractal Noise），设置如下  

![](/tb/area4/entry16_pic/294.jpg)
  
之后得到这样的一个分形杂色（Fractal Noise）  

![](/tb/area4/entry16_pic/295.jpg)
  
  
  
  
完成后，再添加一个 单元格图案（Cell Pattern）。  
图案那里选择晶格化（Crystallize）  

![](/tb/area4/entry16_pic/296.jpg)
  
  

![](/tb/area4/entry16_pic/297.jpg)
  
这里不用马赛克的原因是，马赛克(Mosaic)是规则的矩形，并不能制造宝石表面的多边形与随机效果。  
  
对这层进行Y轴缩放（快捷键S）  
记得把前面的锁定高宽比去掉（就是红色圈地方的锁链）  

![](/tb/area4/entry16_pic/298.jpg)
  

![](/tb/area4/entry16_pic/299.jpg)
  
将图层混合模式改为线性减淡(Linear Dodge)，并且复制一层，对复制后的一层添加方框模糊（Box Blur），模式改为颜色(Color)，调整不透明度（Opacity）。  

![](/tb/area4/entry16_pic/300.jpg)
  
  
到这，表面就完成了。  
这时候你可能看不出来有宝石表面的那样的反射，你可以试试加个底色预览下。  
  

2.宝石内部纹路的制作  
新建固态层（Solid），添加分形杂色（Fractal Noise）  

![](/tb/area4/entry16_pic/301.jpg)
  
  
添加色阶（Levels）与快速模糊（Fast Blur）调整  

![](/tb/area4/entry16_pic/302.jpg)
  
  
图层不透明度（Opacity）改为52%，模式改为屏幕（Screen）  
  
弄完之后你得到的画面应该是这样的。  

![](/tb/area4/entry16_pic/303.jpg)
  
  
复制一层 ，调整色阶（Levels）（2），并且修改不透明度（Opacity）  

![](/tb/area4/entry16_pic/304.jpg)
  

![](/tb/area4/entry16_pic/305.jpg)
  
  

![](/tb/area4/entry16_pic/306.jpg)
  
  
  
到这里内部纹路差不多就完成了，为了凸显立体复杂形，所以再添加一个细微的，运动幅度大的分形纹路。  
  
新建一层，添加分形杂色（Fractal Noise）  

![](/tb/area4/entry16_pic/307.jpg)
  
  
一样，添加色阶（Levels）调整，不过这里最后添加的是矢量模糊（CC Vector Blur）。  

![](/tb/area4/entry16_pic/308.jpg)
  
层不透明度（Opacity）调为48%，模式调为屏幕（Screen）。  

![](/tb/area4/entry16_pic/309.jpg)
  
  

3.色调  
显示全部层  

![](/tb/area4/entry16_pic/310.jpg)
  

![](/tb/area4/entry16_pic/311.jpg)
  
是不是感觉很像了。  
把这些层预合成下，命名为宝石。  
再随便画一个遮罩（Mask），像宝石就行  

![](/tb/area4/entry16_pic/312.jpg)
  
对合成添加色阶（Levels）  

![](/tb/area4/entry16_pic/313.jpg)
  
让物体更透亮一点。  

![](/tb/area4/entry16_pic/314.jpg)
  
  
添加曲线（Curves）调整颜色（我这里是把绿色往下拉就会变成紫色，想要其他颜色的话，大家可以随意玩）  

![](/tb/area4/entry16_pic/315.jpg)
  

![](/tb/area4/entry16_pic/316.jpg)
  
  
最后，是否要发光（Glow），就看各位的需求了，这是发光后的。我就不贴发光数据了  

![](/tb/area4/entry16_pic/317.jpg)
  
  
※动态：通过CC light sweep和里面分形的演化K帧来实现。  

![](/tb/area4/entry16_pic/318.jpg)
  
  
  
4.扩展：粒子复制  

![](/tb/area4/entry16_pic/319.jpg)
  
这个想做的人应该都会的，不会小伙伴就去补补粒子课吧_(:з)∠)_  
  

