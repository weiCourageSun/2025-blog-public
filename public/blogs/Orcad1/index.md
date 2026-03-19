# Orcad和Cadence的学习心得(一)

## Capture

### capture是绘制电路原理图，目前都是打开dsn项目，在此基础上系统参照软件自带的各个组件的画法可以直接加以改进。里面在元器件绘制中有一些小技巧。包括公共断点(busconnection)，还有导线的网络名称要配有，这一步是在最后DRC检查必不可少的

![image-20260319202919615](https://beifengcourage.site/PicGo/image-20260319202919615.png)

![image-20260319203026597](https://beifengcourage.site/PicGo/image-20260319203026597.png)

![image-20260319211011543](https://beifengcourage.site/PicGo/image-20260319211011543.png)

### 然后就是对于所需要的元器件找商城，看手册，具体数据画封装启动下面的软件



![image-20260319211253813](https://beifengcourage.site/PicGo/image-20260319211253813.png)

## Padstakc Editor

![image-20260319211455589](https://beifengcourage.site/PicGo/image-20260319211455589.png)

### 进来界面如下，以电阻封装为例子，下面是数据手册，可以看到CFR200的引脚直径为0.8mm

![image-20260319211636534](https://beifengcourage.site/PicGo/image-20260319211636534.png)

### 可以看到左下角有一个单位切换，基于1mm对应39.37mils，引脚取整40mils

### ![image-20260319212140738](https://beifengcourage.site/PicGo/image-20260319212140738.png)然后在第一层一般是引脚的2倍，取80mils，thermal pad 和 anti pad都是比之前多6mils

![image-20260319212504946](https://beifengcourage.site/PicGo/image-20260319212504946.png)

### 最后是丝印层，和第三次大小一样即可

![image-20260319212740028](https://beifengcourage.site/PicGo/image-20260319212740028.png)

## 接着我们打开PCB Editor

### 接下来要通过它把封装画好，选图示symbol package。

![image-20260319212943199](https://beifengcourage.site/PicGo/image-20260319212943199.png)

### 进来以后先改设置，右边都勾上，然后 设置setup grids 全设置0.1。接着再Desgin,Extents设置中心点坐标，就可以找到绿色的中心圈

![image-20260319213154041](https://beifengcourage.site/PicGo/image-20260319213154041.png)

![image-20260319213245773](https://beifengcourage.site/PicGo/image-20260319213245773.png)

![image-20260319213349223](https://beifengcourage.site/PicGo/image-20260319213349223.png)

![](https://beifengcourage.site/PicGo/image-20260319213456332.png)

下面就是添加在Pad上画好的封装

![image-20260319213658362](https://beifengcourage.site/PicGo/image-20260319213658362.png)

### 接着x轴设置2个，间隔为20，offset偏移量改为0

![image-20260319213846842](https://beifengcourage.site/PicGo/image-20260319213846842.png)

### 下面是防止引脚编辑准确快捷方式，黑框输入 x -(间隔/2) 0 

![](https://beifengcourage.site/PicGo/image-20260319213912270.png)

### 由内向外画，一共3层

![image-20260319214210231](https://beifengcourage.site/PicGo/image-20260319214210231.png)

![image-20260319214326123](https://beifengcourage.site/PicGo/image-20260319214326123.png)

![image-20260319214400589](https://beifengcourage.site/PicGo/image-20260319214400589.png)

![image-20260319214438651](https://beifengcourage.site/PicGo/image-20260319214438651.png)

### 当然里面有个小层不能忘，PLACE_BOUND_TOP

![image-20260319214623952](https://beifengcourage.site/PicGo/image-20260319214623952.png)

### 最后画上指代名称

![image-20260319214725865](https://beifengcourage.site/PicGo/image-20260319214725865.png)

![image-20260319214759555](https://beifengcourage.site/PicGo/image-20260319214759555.png)

## 下阶段学习从原理图到板PCB的画法

![image-20260319211119784](https://beifengcourage.site/PicGo/image-20260319211119784.png)