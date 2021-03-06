# 渲染耳机教程
先说这张吧
比较暗的那张是 KS 出的，后面 PS 拉了下对比度，让高光的地方更亮了，然后调了一下色温
![](http://ox55f9bg6.bkt.clouddn.com/2017-10-03-190114.jpg)

因为我比较习惯先出一张布光相对准确，但是对比不那么强烈的，这样有相对来说比较好的后期空间。

当然另外一点也是 KS 对于高光部分的渲染效果不是很准，体现在像白色的物体渲染不准确。
所以基本上无论是这张图还是另外一张都是这么处理的。![](http://ox55f9bg6.bkt.clouddn.com/2017-10-03-190117.jpg)
![](http://ox55f9bg6.bkt.clouddn.com/2017-10-03-190119.jpg)

然后说下材质这部分。
![](http://ox55f9bg6.bkt.clouddn.com/2017-10-03-190120.jpg)这个是黑色塑料的参数。其实用的是 KS7默认的黑色塑料材质。
原因我在 http://www.zhihu.com/question/53106224/answer/208900051 这篇文章里有提到，就不多说了 应该不少童鞋都看过吧~

然后皮革在这里我其实做过一些调整，会比 OC 里面要麻烦一些
![](http://ox55f9bg6.bkt.clouddn.com/2017-10-03-190121.jpg)
主要调整的地方是粗糙度，这个是取消掉粗糙度后的效果
![](http://ox55f9bg6.bkt.clouddn.com/2017-10-03-190122.jpg)
![](http://ox55f9bg6.bkt.clouddn.com/2017-10-03-190123.jpg)
这个是增加了粗糙度的效果

粗糙度会影响整个反射情况
如果不加粗糙度，我自己感觉不像皮革，像是橡胶

粗糙度其实并不是颗粒感，凹凸才是颗粒感

粗糙度控制的是反射的强弱程度（粗糙度是细的看不到的颗粒）

![](http://ox55f9bg6.bkt.clouddn.com/2017-10-03-190126.jpg)

然后关于地板的材质 我用的是Poliigon 的一个贴图， 用法还有点讲究的，我有写过一个回答：[如何让渲染场景更加真实？](http://www.zhihu.com/question/49491866/answer/207591570)大家可以去看看。


就是有 颜色、反射、粗糙图和凹凸
最后那个标签其实可以忽略掉，后来我发现加了和没加没啥区别…

材质这部分就差不多到这里。和 OC 对比下来其实感觉复杂不少，尤其是皮革那边。可能是材质算法也不一样

接下来说一下环境光源吧

首先 我会先加一张环境光，但是调的比较暗一些，然后把饱和度调为0。
![](http://ox55f9bg6.bkt.clouddn.com/2017-10-03-190128.jpg)

加一张背景的原因是，不加的话这几个地方就会看着特别黑，并不是非常真实。
所以会用一张自带的环境光当背景，但是把颜色啊 亮度都调小，这样不会干扰。
![](http://ox55f9bg6.bkt.clouddn.com/2017-10-03-190131.jpg)

 
然后一盏光一盏光加上去。
![](http://ox55f9bg6.bkt.clouddn.com/2017-10-03-190136.jpg)

![](http://ox55f9bg6.bkt.clouddn.com/2017-10-03-190145.jpg)
![](http://ox55f9bg6.bkt.clouddn.com/2017-10-03-190156.jpg)
![](http://ox55f9bg6.bkt.clouddn.com/2017-10-03-190215.jpg)

这边需要说的是一个灯光衰减的意义。

大家默认的光可能是下图这样的，高光那边看着就会比较平，不丰富。
![](http://ox55f9bg6.bkt.clouddn.com/2017-10-03-190239.jpg)

![](http://ox55f9bg6.bkt.clouddn.com/2017-10-03-190244.jpg)
这是经过调整过参数的光，看着就会更层次感，更加真实。

大家会发现有衰减的灯光效果会更加真实。
原因其实是现实生活中的灯光衰减模式是二次衰减。每经过单位1的路程，灯光衰减为员原来的平方分之一。

这里主要调整的是灯光的衰减，衰减值为1 衰减模式为二次。


![](http://ox55f9bg6.bkt.clouddn.com/2017-10-03-190246.jpg)
![](http://ox55f9bg6.bkt.clouddn.com/2017-10-03-190248.jpg)

看灯其实也能看出来差异



然后布光要讲的差不都就这么多，我感觉下来的确是KS 的渲染算法在一些要求高一点的场景下会比较吃力后布光要讲的差不都就这么多，我感觉下来的确是KS 的渲染算法在一些要求高一点的场景下会比较吃力。

就像这样的场景必须要设定好各种参数才能保证看着比较真实。而在其他软件里面可能就一张HDR 或者一盏灯就差不多了。也不是说不能做，就是会比较麻烦一些。


