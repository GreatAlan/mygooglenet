# Googlenet

GoogleNet，又称为Inception v1，是由Google开发的深度卷积神经网络架构之一。它是使用Inception模块概念的先驱模型之一，Inception模块包含多个并行的不同大小的卷积滤波器。以下是GoogleNet的简要介绍：

输入层：

输入尺寸：224x224x3（RGB图像）
起始阶段（Stem）：

7x7的卷积层，64个过滤器，步幅为2，使用ReLU激活函数
3x3的最大池化层，步幅为2
Inception模块（重复使用）：

Inception模块 1：

1x1的卷积层，64个过滤器
3x3的卷积层，128个过滤器
5x5的卷积层，32个过滤器
1x1的最大池化层，32个过滤器
沿深度方向连接各层的输出
Inception模块 2：

类似的结构，使用不同的过滤器大小
（重复使用Inception模块结构）

全连接层：

全局平均池化层
包含1000个单元的全连接层（用于ImageNet分类）
Softmax激活函数
输出层：

输出尺寸：1000（用于ImageNet类别）