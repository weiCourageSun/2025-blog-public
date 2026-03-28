# PCB设计读书(一)

## 在 Layout 和 IPC 中,A级表示一般设计复杂度。标准 IPC‐2221A 包含与所  谓标准制造余量(SFA)相关的表格。Layout 使用 SFA 设置基线布线和间距规则。  例如,在 Layout 中,A级技术文件只允许 DIP IC 引脚之间有一条走线,并使用 62  密尔(0.062 英寸)焊盘和 38 密尔钻孔用于 IC 引脚,25 密尔布线和过孔网格,100  密尔元件放置网格,以及 12 密尔走线间距。

![image-20260327141329465](https://beifengcourage.site/PicGo/image-20260327141329465.png)

![image-20260327151943447](https://beifengcourage.site/PicGo/image-20260327151943447.png)

![image-20260327190025041](https://beifengcourage.site/PicGo/image-20260327190025041.png)

![image-20260327190338680](https://beifengcourage.site/PicGo/image-20260327190338680.png)

![image-20260327190718175](https://beifengcourage.site/PicGo/image-20260327190718175.png)

![image-20260327190856917](https://beifengcourage.site/PicGo/image-20260327190856917.png)



![](https://beifengcourage.site/PicGo/image-20260328093235908.png)

![](https://beifengcourage.site/PicGo/image-20260328100535645.png)

![](https://beifengcourage.site/PicGo/image-20260328100611551.png)

![](https://beifengcourage.site/PicGo/image-20260328100826246.png)

![](https://beifengcourage.site/PicGo/image-20260328101118289.png)

![](https://beifengcourage.site/PicGo/image-20260328101644904.png)

![](https://beifengcourage.site/PicGo/image-20260328102102009.png)

![](https://beifengcourage.site/PicGo/image-20260328104617162.png)

![](https://beifengcourage.site/PicGo/image-20260328104642847.png)

![](https://beifengcourage.site/PicGo/image-20260328110121318.png)

![](https://beifengcourage.site/PicGo/image-20260328110152299.png)

![](https://beifengcourage.site/PicGo/image-20260328110229264.png)

![](https://beifengcourage.site/PicGo/image-20260328110316414.png)

![](https://beifengcourage.site/PicGo/image-20260328111217118.png)

![](https://beifengcourage.site/PicGo/image-20260328111649626.png)

![](https://beifengcourage.site/PicGo/image-20260328122418908.png)

![](https://beifengcourage.site/PicGo/image-20260328123733852.png)

## 更正：表5-13上面数据提到的最大引脚的最小孔径应该是35.2+10=45.2

![](https://beifengcourage.site/PicGo/image-20260328124022760.png)

![](https://beifengcourage.site/PicGo/image-20260328125534293.png)

## 例如给出一个32密尔的引脚，给出孔径50密尔，在计算外部焊盘(布局在顶部和底部)的尺寸，希望达到最高等级的精度C,可以计算出



### 	a = DH - 2Tp  = 50 -  2*1(内部)

### 						b = 2*  2(外部)

### 	c = 8(公差)

### 	D = a + 2b + c = 50 - 2 + 4 + 8 = 60



![](https://beifengcourage.site/PicGo/image-20260328132251849.png)

## 这里挺有意思的，作者指出焊盘既不能太大也不能太小，太大会与上平面层产生耦合电容，太小会导致和地线或电源线相接导致短路

![](https://beifengcourage.site/PicGo/image-20260328132642151.png)

### 下面给出基于走线的问题，直接给出作者的结论：1、首先对于信号线与回流平面(狭义上指的是接地面)，两者贴的越近越好。2对于不相关的导线，越远越好

#### 理由：首先是环路电感的产生，它是由于导体自身的特性会产生电感，而通过回流平面的导线自感产生的磁感线会和正向导线产生的磁感线相抵消，导致原来导线的磁感线减小，自感也就变小，回路中的环路电感就减小

![](https://beifengcourage.site/PicGo/image-20260328171630616.png)

#### 另一方面，由于导线自身会向外辐射电场，这个干扰电场需要被“束缚”，就得需要靠近回流平面，它与回流平面构成平行板电容器，可以讲“噪声电场”束缚

![](https://beifengcourage.site/PicGo/image-20260328172008505.png)

#### 但是由于平行版电容器具有容抗，是否会带来不好的效果呢？作者指出反而是促进了噪音的减少

![](https://beifengcourage.site/PicGo/image-20260328172418541.png)

## 接地平面与接地

![](https://beifengcourage.site/PicGo/image-20260328172720591.png)









