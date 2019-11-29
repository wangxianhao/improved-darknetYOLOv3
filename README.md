![Darknet Logo](http://pjreddie.com/media/files/darknet-black-small.png)

# Darknet #
Darknet is an open source neural network framework written in C and CUDA. It is fast, easy to install, and supports CPU and GPU computation.

For more information see the [Darknet project website](http://pjreddie.com/darknet).

For questions or issues please use the [Google Group](https://groups.google.com/forum/#!forum/darknet).


文中，首先处理好KITTI车辆数据集，采用随机多尺度变化增强车辆训练集样本数量，采用k-means聚类获取最优先验候选框大小，引入到YOLOv3模型中，提升模型的车辆检测精度和鲁棒性。通过实验数据分析对比原始模型，得到最优的检测精度等参数。最后，通过优化后的模型测量前方车辆距离，并与真实车距对比分析，建立模型修正测距算法。

模型中测距算法放在了image.c文件中，通过训练得到的最优车辆检测权重为25000轮训练权重，权重下载地址：


