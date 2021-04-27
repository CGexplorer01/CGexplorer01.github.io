# []()【新人求教】关于AE的一个随机表达式.谢谢各位前辈了————  
原作者 百度贴吧:Sakyoha [原地址](https://tieba.baidu.com/p/1726679145) 首发时间:2012-07-15 13:31  
最新获取时间:2021-04-26  
  
想做一个方格随机出现的方格蒙版.但是在写表达式的时候遇到了一点问题.所以就来求教了  
大概是这样的.方格会在不同的位置出现.没有规律.但是位置属性是有规律的.  
所以自己就写了个表达式.但是表达式写出来出现了一点问题.那就是因为方块是随机的.问题就是因为是随机的所以会重复， random没能满足不重复复制，60X60规格的小方格.从第一个开始复制重复的概率是1/36， 当你复制到第35个的是后，你想要复制出最后一个没有复制的空位的可能性只有1/36.这样.复制出6X6的大方块的时候.大概就需要90个层.所以会造成很多不必要的麻烦  
希望有人能解决这一点.最好是能够重新写一下表达式.讲一下思路  
感谢了  

顺便说一下.我用的是random.先用SeedRandom控制位置属性random的速率  
然后再用Mathfloor控制random1-6出现规格的整数性.这样我就可以保证方格随机出现的位置肯定是按照60X60的规格出现的  

这里补上我的表达式吧  
位置属性：seedRandom(index+1,true);  
transform.position+[Math.floor(random(1,6))*62,Math.floor(random(1,6))*62];  
透明属性：thisComp.layer("空白 1").effect("transfor***ider")-((index-2)*100);  
链接的一个滑块控制  
大家看看能否改进  
  

![](/tb/area4/entry75_pic/0.jpg)
  
如图  
确实达到了随机的目的  
但是重复了将近20个层  

对了 还有这个表达式  
myEndTime = 60;  
thisTime = time*thisLayer.inpoint; segMin = 0.8; //minimum segment duration  
segMax = 0.8; //maximum segment duration  
minVal = [0,0];  
maxVal = [11.99,11.99]; end = 0;  
j = 0 ;  
if (thisTime < myEndTime) t = thisTime else t = myEndTime;  
while ( t >= end){  
j = 1;  
seedRandom(j,true);  
start = end;  
end = random(segMin,segMax);  
}  
endVal = random(minVal,MaxVal);  
seedRandom(j-1,true);  
dummy=random();  
startval = random(minVal,maxVal); [Math.floor(startval[0]), Math.floor(startval[1])]*60+[40,40];  
这里面的的阵列应该如何对应  
inpoint的类型的属性  
有几个地方有Bug 但是不知道哪里错了  
求前辈们指导啊![](/tb/area4/entry75_pic/1.jpg)  
  


![](/tb/area4/entry75_pic/2.jpg)
  
这是LP大07年OP的 这里是按顺序出现的 从左边到右边 现在要让它任意方向出现 出现后不消失 7L那个表达式先晒一边吧  

