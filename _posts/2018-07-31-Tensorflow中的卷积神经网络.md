# Tensorflow中的卷积神经网络

#### 卷积层

定义一个卷积核（filter）去扫描目标图像，一般卷积核的大小为3x3、5x5、7X7，卷积核为奇数的原因：

- 保证了 **锚点** 刚好在中间，方便以模块中心为标准进行滑动卷积，避免了位置信息发生 **偏移** 。
- 保证了 **padding** 时，图像的两边依然相 **对称** 。

一般卷积核的大小根据输入的层的神经元大小来指定，小的卷积核的计算复杂度要小于大的卷积复杂度，比如一个3层3X3的卷积，和一个7X7的卷积，他们覆盖的输入层连通性一致，但各自的复杂度为3x3x3=27;1x7x7=49。

对于多通道的输入层，卷积核的大小也将变成3维，kernel_size * kernel_size *  channel_num ,卷积核的结果为每一个通道核对应的2维卷积进行运算后，最后3个通道的值相加，再加上**biases**成为该点的卷积值。

tesorflow中的卷积层权重定义为**[kernel_size , kernel_size , num_channels, num_filters]**

卷积核的深度（数量）一般都是16的倍数。

 

#### 池化层

池化层用的比较多的是max池化方法，池化层的shape为**[batch, height, width, channels]** ，一般batch、channels为1，height、width为2.即将2x2的格子中取最大的那个数作为最终输出。池化层对基础的特征做一次高层的抽象。每经过一次池化层，数量都相应x2，**【why？】**

#### 归一化层（Batch Normalization ）



#### 



#### 全连接层



### 总结

小而深：卷积核小，层数多



### 参考

Batch Normalization ：https://blog.csdn.net/fate_fjh/article/details/53375881