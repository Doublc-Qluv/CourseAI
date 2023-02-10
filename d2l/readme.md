动手学习深度学习
====
# 资料
[官网：https://zh.d2l.ai/](https://zh.d2l.ai/)

[Github: https://github.com/d2l-ai/d2l-zh](https://github.com/d2l-ai/d2l-zh)

[d2l包源码](https://github.com/d2l-ai/d2l-zh/tree/master/d2l)

[视频课程：B站](https://space.bilibili.com/1567748478/channel/seriesdetail?sid=358497)


# 内容
1. 深度学习基础
   1. 线性神经网络
   2. 多层感知机
2. 卷积神经网络
   1. LeNet
   2. AlexNet
   3. VGG
   4. Inception
   5. Resnet
3. 循环神经网络
   1. RNN
   2. GRU
   3. LSTM
   4. seq2seq
4. 注意力机制
   1. Attention
   2. Transformer
5. 优化算法
   1. SGD
   2. Momentum
   3. Adam
6. 高性能计算
   1. 并行
   2. 多GPU
   3. 分布式
7. 计算机视觉
   1. 目标检测
   2. 语义分割
8. 自然语言处理
   1. 词嵌入
   2. BERT


# 前置

1. 注意广播机制所造成的需的结果的不匹配
   1. 从numpy过来的广播机制，当运算两个量维度不同时，在运算前会变为一样，再进行运算
   ```python
   a = torch.arange(3).reshape((3, 1))
   b = torch.arange(3).reshape((1, 2))
   a, b

   # 得到
   (tensor([[0],
            [1],
            [2]]),
    tensor([[0,1]]))
   ```
   ```python
   a + b

   # 得到
   tensor([[0, 1],
           [1, 2],
           [2, 3]])
   ```