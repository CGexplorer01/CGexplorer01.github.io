# []()【做着玩】用表达式在AE2018中实现简单plexus/线条连接效果  
原作者 百度贴吧:框六五二 [原地址](https://tieba.baidu.com/p/5701937588) 首发时间:2018-05-16 15:43  
最新获取时间:2021-04-26  
  
刚考完期中，又能闲一段时间了
![](/tb/area4/entry8_pic/0.jpg)
。于是翻了下ae官网用户手册，看到了个表达式可以创建路径，就想起来做这个效果。  
为什么我要说成ae2018呢，因为2018才可以用这个表达式，TM我还在2017上折腾了大半天![](/tb/area4/entry8_pic/1.jpg)，百度Google咋也找不到失败原因，最后发现竟然是新增功能![](/tb/area4/entry8_pic/2.jpg)。所以说用2018前的版本并不能通过这个方法实现，不过我问了一下，貌似有个叫motion v2的脚本中的一个功能可以在给定两点之间创建连接，原理一样，实现起来都很简单，有兴趣的可以试试![](/tb/area4/entry8_pic/3.jpg)。  

![](/tb/area4/entry8_pic/4.jpg)
  

二楼祭大鼻孔![](/tb/area4/entry8_pic/5.jpg)  

首先要说明的是，此方法纯属本人闲得**做着玩的，众所周知插件如plexus，脚本如cluster，都可以轻松实现这种效果。如果你跟我一样是个刚接触ae表达式并且有兴趣想知道怎么实现这种效果的，那么可以瞅瞅这里。  

![](/tb/area4/entry8_pic/6.jpg)
  

废话不多说![](/tb/area4/entry8_pic/7.jpg)  
  
  
  
  
首先我们有两种思路：  
1.      一堆线条发生长度与位置变化，让其中某些保持一端在一个点上  
2.      点的位置变化，然后每一点向其他点连线  
  
  
很明显,方法2要比1容易实现的多  
  
然后我们分析一下这个效果有哪些组成要素：  
1.      点（point）与位置（position）变化  
2.      线（line）随着两点间距离变化改变长度  
3.      线的长度影响描边宽度（stroke width）  
4.      …  
…(更多效果大家慢慢搞，都是相似的操作)  
  

第一步，撒点  
A.     虽然说起来是点，实际上是图层的位置属性，对于什么图层可以有几种较优的选择：  
  
1.空对象（null object） ：优势在于占内存较小，而且容易操纵位置  
2.形状层（shape layer） ：优势在于可以赋予端点任意形状  
当然你也可以用空对象父集到形状层。但操作起来比较麻烦。  
  
还有一个方法是通过效果—表达式控制—点控制（point control）/3D点控制 ，这个个人认为也是比较麻烦。  
  
B.点的位置变化  
  
  
如果你对点的变化有要求，可以手动对位置K帧，若结合运动追踪有很好的效果。  
如果你只想得到一个动态的效果，那么可以对位置添加表达式。这时可以有两种选择：  
  
1.      wiggle(freq,amp)  
2.      noise(seed)    [注意不是random()，因为random返回的随机值之间没有关联]  
  
两种都可以，这里我用wiggle，因为更容易控制，而且可以更改某一帧的位置。如果你  
用noise，可以写成如：  
position=[(1+noise(time/32))*(1280/2), (1+noise(time/28))*(720/2)]  
【这里我工程用的720p，可以根据需求适当修改，也可以用thisComp.width,thisComp.height获取，下同】  
  
用wiggle写就是position=[wiggle(0.3 , 888)[0],wiggle(0.25 , 666)[1]]  
  
  
在这里最好把创建的空对象或者形状层单独用一个合成来存放，以便后续的更改，命名可以设为“Nulls”  

![](/tb/area4/entry8_pic/8.jpg)
  
  

第二步：在点之间创建路径  
  
这里同样用单独一个合成存放，命名为“Lines”  
  
在“Lines”合成的中右键新建一个形状层改名为Line 1，左侧小箭头展开，点击“添加（add）”—“路径(path）“，然后继续“添加（add）”—“描边（stroke）”，给描边宽度一点参数比如6。  

![](/tb/area4/entry8_pic/9.jpg)
  
  
  
  
  
  
接下来就是最核心的一步，展开刚创建的路径，alt+左键点旁边的秒表添加表达式：  
lis=[]  
for(i=0;i<comp("Nulls").numLayers;i++){  
for(j=i+1;j<comp("Nulls").numLayers;j++){  
lis.push([i+1,j+1])  
}  
}  
//对Nulls中每相连两点的index生成一个列表  
  
p=lis[index-1]  
a=comp("Nulls").layer(p[0]).transform.position-[640,360]  
b=comp("Nulls").layer(p[1]).transform.position-[640,360]  
createPath([a,b])  
  
添加后可能会报错，这可能因为在“Nulls”图层中你只创建了一个空对象或形状层，可以按ctrl+D复制，这里可以先复制到6份  
  
这时面前出现了一道排列组合题，n个点之间两两相接，共有多少条线？  
答案是Cn2个，若n=6,则有C6 2=6*5/（2*1）=15条线，若n=10,则有10*9/（2*1）=45  
  
  
  
  
那么，因为我们的Nulls图层中有6个图层，回到“Lines”合成中，复制“Line 1”到15份，点击预览，如果前面都做对的话，你就能看到基本的效果已经出来啦  

![](/tb/area4/entry8_pic/10.jpg)
  
  
  

没人吗
![](/tb/area4/entry8_pic/11.jpg)
  

第三步：为线条添加描边宽度变化  
  
这里引入一个函数：  
linear(value,olimit1,olimit2,limit1,limit2)  
功能是将value在(olimit1,olimit2)范围内的值对应到（limit1,limit2）上，比如  
linear（6，0，10，0，100），返回的值就是60，  
linear（6，0，10，100，0），返回的值就是40.  
  
  
我们用这个函数，通过两点之间距离值返回透明度的值，于是在stroke width下我们可以写：  
  
  
len=length(content("Path1").path.points()[0],content("Path 1").path.points()[1])  
linear(len,0,comp("MAIN").layer("parameter").effect("MaxD")("Slider"),8,0)  
  
  
于是我们将描边宽度对应到点之间的距离上，当点之间距离为0时，描宽为8，当距离为MaxD（这个是滑块控制，在下面说明）时，描宽为0.  
可以改进的是，linear正如字面意义上是线性的意思，如果我们把linear改为ease，其参数不变，就可以得到缓入缓出的较为流畅的动画。也就是：  
  
  
len=length(content("Path1").path.points()[0],content("Path 1").path.points()[1])  
ease(len,0,comp("MAIN").layer("parameter").effect("MaxD")("Slider"),8,0)  

下面说明如何通过滑块较为便捷的控制表达式中的一些参数  
  
  
我们新建一个合成，命名为“MAIN”，将上面两个合成“Nulls”，“Lines”拖到里面，然后右键新建一个调整图层（Adjustment Layer）改名为parameter，添加效果—表达式控制—滑块（slider），选择滑块按回车键改名为MaxD，即最大距离，然后在  
ease(len,0,▲,8,0)  
将三角换成  
comp("MAIN").layer("parameter").effect("MaxD")("Slider")  
【中文版ae需注意双引号内名称是否能对应上，comp即为合成的意思，括号内为名称，layer即图层，effect即效果，slider即滑块，此后不做赘述】  
  
同理，也可以添加多个滑块效果分别控制描宽的最大宽度，wiggle在x，y上摆动的频率与幅度等等。比如在空对象的位置属性写  
x=wiggle(comp("MAIN").layer("parameter").effect("wiggle_xfreq")("Slider"),comp("MAIN").layer("parameter").effect("wiggle_xamp")("Slider"))[0]  
y=wiggle(comp("MAIN").layer("parameter").effect("wiggle_yfreq")("Slider"),comp("MAIN").layer("parameter").effect("wiggle_yamp")("Slider"))[1]  
position=[x,y]  

![](/tb/area4/entry8_pic/12.jpg)
  

如果你觉得点太少。可以多复制几份空对象，但不要忘记“Lines”合成中的形状层同样需要增加，有n个空对象就得有Cn2个形状层。  
  
其实还可以实现更多效果，比如每三个点生成一个三角形然后根据三角形面积返回透明度值等等，这些都可以用表达式实现。  
  
  
当然，这样实现的效果速度会非常慢，所以权当无聊做瞎折腾罢。  

