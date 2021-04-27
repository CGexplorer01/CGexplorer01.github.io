# []()【N卡独享】新一代图片放大神器waifu2x-caffe  
原作者 百度贴吧:V-R- [原地址](https://tieba.baidu.com/p/3999123538) 首发时间:2015-08-25 21:31  
最新获取时间:2021-04-26  
  
1L效果图镇楼  
原图（432x336）  

![](/tb/area4/entry24_pic/0.jpg)
  
  
3倍放大(不知道度娘会不会缩图)  

![](/tb/area4/entry24_pic/1.jpg)
  

waifu2x　一个新式的图片放大&降噪算法,或许不少人早已听说过了。据说开发时有针对性地考虑了2次元类图片,因此对动画截图、galgameCG之类的图片效果更佳出众。  
测评信息：http://tieba.baidu.com/p/3787405675  

![](/tb/area4/entry24_pic/2.jpg)
  
  

![](/tb/area4/entry24_pic/3.jpg)
  
  

![](/tb/area4/entry24_pic/4.jpg)
  
  
(左nnedi3右waifu2x)  
先前吧里有人推荐过用PhotoZoom.Pro这款工具放大。LZ先前也时不时在用它,然而它最新版中最强的放大算法也不过是S-Spline MAX,终究还是Spline的范畴,远逊于nnedi3。而从上图可以看出waifu2x的效果又强于nnedi3,可见它是多么恐怖了  
其实nnedi3问世已久,只是无人GUI化,导致调用起来略麻烦,LZ以前也只能通过AVS调用。然而waifu2x很快就有日本友人弄出了图形界面工具waifu2x-caffe,支持批处理、降噪等多项功能,可谓是极大的福音  

![](/tb/area4/entry24_pic/5.jpg)
  
  
唯一可惜的是强大的算法肯定需要辅助支撑的,而这个辅助支撑就是CUDA——因此A卡就byebye了,只有支持CUDA的N卡才能使用之(无CUDA的电脑课使用纯CPU模式,但速度很慢,不推荐)  
下载及使用方式见楼下  

下载：百度盘点COM/s/1pJta86f 密码:2phm  
要求：64位windows系统,显卡支持CUDA  
使用前电脑必须装有VC++ 2013 x64库,不过上面的链接中包含了安装文件(rar中的vcredist_x64.exe)  
waifu2x-caffe文件夹免安装,解后即可(建议放置在全英文&数字路径下)  
运行waifu2x-caffe.exe文件即打开  

![](/tb/area4/entry24_pic/6.jpg)
  
  
直接把需要放大的图片拖入“入力パス”右边的框栏即可,也可直接拖入文奸夹进行批量处理  
左侧的变换模式依次为“纯降噪”、“纯放大”、“降噪&放大”、“降噪(自动)&放大”,一般选第3个就OK  
放大倍数可精确到2位小数点  
全部设置好后点最右的“実行”即可开始处理  
对于有CUDA的电脑处理速度很不错,LZ的笔记本一张图放大3-4倍只需要4秒左右  

