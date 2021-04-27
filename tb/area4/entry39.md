# []()【表渣脚本】分型图一键生成器  
原作者 百度贴吧:人间之表 [原地址](https://tieba.baidu.com/p/3144926094) 首发时间:2014-07-04 18:48  
最新获取时间:2021-04-26  
  

![](/tb/area4/entry39_pic/0.jpg)
  

![](/tb/area4/entry39_pic/1.jpg)

![](/tb/area4/entry39_pic/2.jpg)
  

![](/tb/area4/entry39_pic/3.jpg)
  

![](/tb/area4/entry39_pic/4.jpg)
  

![](/tb/area4/entry39_pic/5.jpg)
  

![](/tb/area4/entry39_pic/6.jpg)
  

![](/tb/area4/entry39_pic/7.jpg)
  

![](/tb/area4/entry39_pic/8.jpg)
  

![](/tb/area4/entry39_pic/9.jpg)
  

![](/tb/area4/entry39_pic/10.jpg)
  

![](/tb/area4/entry39_pic/11.jpg)
  

![](/tb/area4/entry39_pic/12.jpg)
  
  
链接：http://pan.baidu.com/s/1hqGGbWg密码：xlp9  
  
  
下面上使用方法  


![](/tb/area4/entry39_pic/13.jpg)
←关于分型我就不怎么讲了，大概就是这个意思2333  
  
  
  
  
这里我主要演示一下两种模式的生成步骤  

simple create是针对单个图层的分型  

![](/tb/area4/entry39_pic/14.jpg)
1、启动simple create，将layer设定为要分型的图层  
2、degree意思是度，也就是对于一个图层来说，有多少个子图层  
3、distance意思是子图层到母图层的距离  
4、scale意思是子图层相对母图层的缩放比例  
5、deep：分型深度，最原始的那个图层设定为0，每生成一代，深度加1  
6、above ，子图层是在母图层的上面还是下面  
  
  
一键生成  
这里我选择degree = 4，distance=100，scale=50，deep=4，生成如下图形
![](/tb/area4/entry39_pic/15.jpg)
  
  
实际上在新生成的合成内，你还以做调整（除了deep、degree、layer以外，实际上还多了几个angle、position，和下面的自定义生成有关，  


![](/tb/area4/entry39_pic/16.jpg)
  

![](/tb/area4/entry39_pic/17.jpg)
比如稍稍给rootTransform的angle打一下关键帧  
  
  
  
下面我会通过custom create具体介绍这些参数的含义  


![](/tb/area4/entry39_pic/18.jpg)
进去之后，有一个rootTransform和多个childTransform  
这里我要讲一下我这个脚本的核心了，首先，我们把图形用有起点的向量来表示图形（或者说箭头）  

![](/tb/area4/entry39_pic/19.jpg)
黑色表示母向量，而红色的表示子向量，然后下一步，红色的向量长大了，要继续生成以红色向量为母向量的子向量  
  

![](/tb/area4/entry39_pic/20.jpg)
  

而对于一些图形来说，有些分量只有根才有，比如雪花，或者就拿我上面的那个simple create生成的图形，对于每一个母向量来说，实际上只有3个子向量，而对于根来说有4个子向量，也就是说，背对着母向量的那个向量是rootOnly的，  

![](/tb/area4/entry39_pic/21.jpg)
  
  
我在simple create里面做了规定，一定有一个相对母向量反向的子向量，是rootOnly的  

rootTransform里面只有angle是有效的，也就是说，对于一次分型来说，母向量不一定是竖直向上的，而是可以旋转的，如果旋转的话，子向量对于母向量来说的相对位置和方向也就一同发生了改变  
  
  
childTransform就代表每一个子分量的起点位置和方向，scale代表的是这个子分量相对于母分量的缩放，rootOnly意思就是说只有根（也就是最初的那个图形）才具有的子分量
![](/tb/area4/entry39_pic/22.jpg)
  

最终要的：source layer、root only，哪怕你其他参数一个都没填也无所谓，因为你可以在生成之后调整，我们这里把两个子分量的source layer都设置为那个A  
  
  
于是我们就可以继续设置了（你也可以先生成，再设置下面的），首先是对于中间那个A，子分量的位置  

![](/tb/area4/entry39_pic/23.jpg)
这里我设置成-100,-30  
  
另一边设置成100,-30  
  
  

![](/tb/area4/entry39_pic/24.jpg)
  

![](/tb/area4/entry39_pic/25.jpg)
angle这么设置，另一边对称一下选+66  

scale就设置为50%，然后点击生成  

![](/tb/area4/entry39_pic/26.jpg)
  
  
然后对于刚刚的参数可以随意调整（scale、position、angle），自行体会  

生成的图层的数量的计算公式：N=(degree^(deep+1)-1)/(degree-1)，自己看看自己的ae能承受多少的图层，不要把电脑玩坏了  

另外的用法：degree设置为1，可以起到一个螺旋的效果（有点类似repeat  
然后实际上那个scale也可以大于100的，也就是逐渐放大  
  
  

![](/tb/area4/entry39_pic/27.jpg)
  
  
  
  
还可以生成雪花、电路板、树之类的东西，还有各种不明觉厉的效果也能做出来，自行尝试吧  

![](/tb/area4/entry39_pic/28.jpg)
  

![](/tb/area4/entry39_pic/29.jpg)顺便一提，英文版ae测试通过，中文版不可知  
  
  
英文大法好  

