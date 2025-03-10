# Chicago_21_无人驾驶城市_07_点模式的生成

无人驾驶城市在分析车载激光雷达与城市环境的关系时，其基本流程如下：无人车实际城市区段扫描，获得点云数据、以及对应的惯性测量单元（Inertial Measurement Unit，IMU）姿态和影像信息等；-->由点云数据提取特征点用于导航评估；-->评估实际测量下，当前城市环境对车载激光雷达导航系统的影响；-->由点云数据构建三维模型，并增加或减少构筑（landmarks），即改变城市局部环境的特征；--->在ROS下使用Gazebo模拟无人车行驶（基于新建立的城市环境三维模型），获取模拟的点云数据，并提取特征点进行评估。

为了观察特征点的空间模式与评估值之间的关系，在之前的探索中采用了方向划分、样方采样、最近邻等分析手段，分析空间模式对导航的影响。而为了进一步验证分析的结果，可以固定某些条件，生成符合条件的空间点模式，用这些具有特殊属性的空间点模式重新模拟，再通过相关性分析等手段，分析该条件是否对导航有所影响。这种生成特定空间点模式的方法，可以避免盲目不断的对环境的改变，来试验结果的方式。在尝试过程中，初步生成了两种类型的空间点模式，一种是固定方向；再者为固定数量。如下图所示：

* 固定方向
![](https://github.com/richieBao/python-urbanPlanning/blob/master/images/51_01.gif)

![](https://github.com/richieBao/python-urbanPlanning/blob/master/images/51_02.gif)

* 固定数量

![](https://github.com/richieBao/python-urbanPlanning/blob/master/images/51_03.gif)

![](https://github.com/richieBao/python-urbanPlanning/blob/master/images/51_04.gif)
