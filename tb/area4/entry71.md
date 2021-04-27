# []()[教程]疯狂甩脂瘦身字  
原作者 百度贴吧:我是新来的额 [原地址](https://tieba.baidu.com/p/1896868557) 首发时间:2012-10-02 17:57  
最新获取时间:2021-04-26  
  
好吧，这个特效的创意来自于一个疯狂甩脂瘦身机的电视广告，我们要实现的效果大概就是文字在不停的甩啊甩，然后边甩边掉渣。  

![](/tb/area4/entry71_pic/0.jpg)
  
  
  

我们从文字层开始制作  
新建一个文字层，打上你要的文字，不过请注意，为了摇摆效果的实现，一个文字层我们只能写一个字。  
然后加入特效:CC-滚珠操作组（CC Ball Action）  
这个特效会把图层转换成点阵的样式，调节参数grid spacing(网格间距) = 8；ball size(滚珠尺寸) = 34 ------- 参数适用于1080P分辨率。  
之后加入特效:find edges(查找边缘)  
调节为invert(反向)  
加入特效:glow(辉光)  

然后的问题是如何让文字扭来扭去  
最开始我打算使用mesh warp(网格扭曲)，但是操作的时候比较麻烦，于是我果断的放弃了。  
换成了另外一个扭曲特效：CC Bend it，如果你用的是中文版，那么你可以会找到一个不尴不尬的名字：CC-弯曲它（好像也有译作CC-弯曲器）。  
调节参数：bend(扭曲数量)打上一系列关键帧，从-50 到50 到 -50 到 50....  
或者你也可以写一个表达式来控制，比如Math.sin(time*5)*50，不过我在这里采用了关键帧的方式。  
start(扭曲起点)-放置于文字底部  
end(扭曲终点)-放于文字顶部  
  


![](/tb/area4/entry71_pic/1.jpg)
  
  
  

我在做的时候希望文字看起来像是只有边缘部分在掉渣，不是整个文字都充当发射器，而且对于文字的底部，从底部甩出来的粒子也应该不会有过大的速度（因为底部几乎就是不动的），所以我没有直接用刚刚做好的文字充当发射层，而是做了一些加工操作：  
将文字层复制两层，这里我们把他们起名叫做copy1 copy2  
将这两层预合成，我们把这个预合成起名叫for particular，进入预合成  
关闭copy1,copy2上的所有特效，仅保留bend it  
将copy1图层向前拉动一帧，将copy1作为copy2的luma inverted matte（反转亮度蒙版）  
在copy2上加入特效：ramp(渐变)，调节参数为文字上部是纯白色，底部是纯灰色（R:127 G:127 B:127）【这里的操作是为了调节粒子速度而设计的，之后会用到】  

![](/tb/area4/entry71_pic/2.jpg)
  
  
  

退回到默认的合成组 Comp1  
新建固态层  
在固态层上添加特效:particular  
调节属性：  
-------Emitter-------  
particles/sec(发射量):25000  
emitter type = layer  
direction = directional  
direction spread = 17  
X rotation = 表达式控制：time * 500  
Y rotation = 关键帧控制：（0）~（90）~（0）~（-90）~（0）~（90）~....  
velocity = 570  
velocity distribution = 1  
layer emitter:  
layer = for particular  
layer sampling = particle birth time  
layer RGB usage = Lightness - velocity  
-------particle-------  
particle type = glow sphere  
sphere feather = 0  
size = 6  
size random = 100  
-------physics-------  
physics model = bounce  
gravity = 420  
-------Aux system------  
emit = at bounce event  
emit probability = 46  
particles/collision = 68  
Life = 0.5  
velocity = 434  
size = 3  
gravity = 250  
randomness:  
life = 100  
size = 100  
--------rendering------  
motion blur:  
motion blur = on  
![](/tb/area4/entry71_pic/3.jpg)我知道你们都很熟了，就不帮你们翻译了  
  


![](/tb/area4/entry71_pic/4.jpg)
  
  
  

复制当前固态层  
调节副本层粒子属性  
-------Emitter-------  
particles/sec(发射量):55000  
-------particle-------  
particle type = textured polygon（因为还没有做粒子，所以有一些参数调不了）  
size = 23  
size random = 49  
-------Aux system------  
emit = continously  
emit probability = 11  
particles/collision = 263  
Life = 0.5  
type = sphere  
velocity = 0  
size = 2  
opacity over life = 第二个  
gravity = 250  
randomness:  
life = 100  
size = 0  
添加特效-4色渐变  
参数调节如图
![](/tb/area4/entry71_pic/5.jpg)
  
  
  


![](/tb/area4/entry71_pic/6.jpg)
  
新建合成组（100*100，持续5帧），在合成组内完成这样的效果，第一帧画一个正方形，第二帧画三角形，然后五边形，五角星，圆形...当然你画点别的我也不介意。  
画完了之后将这个合成作为第二个粒子层的粒子，选择random - still frame模式，具体的参数调节见14L的图  

![](/tb/area4/entry71_pic/7.jpg)你还可以将粒子的旋转属性也做调整，让他们转着圈飞出来。  

复制当前粒子层  
在新的一层上更改属性如下  

![](/tb/area4/entry71_pic/8.jpg)
  
  
  

![](/tb/area4/entry71_pic/9.jpg)然后基本制作就完成了  
不过我貌似忘了说要建一个固态层当做地板...![](/tb/area4/entry71_pic/10.jpg)不过我相信你们已经发现了~  
之后新建调节层调色，新建摄像机调节动画，就可以渲染输出了。  

<原文此处有视频，建议到原地址观看>  
<原文视频来源: http://www.tudou.com/programs/view/BnCkFZ2UAi8/>
  
  
  

