# head_detect
人头检测算法,人流量统计，人头计数,人员聚集分析，人脸测温

应用环境：ARM 边缘设备、PC服务器设备

人头检测在安防监控中是比较常用的功能，而公交车、商场或者大型场馆的拥挤人群计数的精准性也非常重要。

演示视频
https://www.bilibili.com/video/BV13k4y1j7d3/
# 算法思想

拥挤人群计数目前主要有两种实现路径：

1.使用回归的算法思路，直接根据图像回归出拥挤人群密度热图，它的缺点是只能得到场景整体的一个拥挤指数，不能获知人群个体的具体位置，而且这种方法对图像分辨率很敏感。（52CV君曾经分享过：尺度不变网络提升人群计数性能（附Github地址））

2.使用目标检测的方法，比如直接使用Faster RCNN检测人，检测后数目标为“人”的个数。这种方法的缺点是在人物相互遮挡的情况下往往性能较差，而人群越拥挤相互遮挡的可能性越大，导致算法使用受限。

设计更有针对性的精准的人头检测，实现更加精准的人群计数。

创新的两点，轻量级人头检测网络和anchors尺度的选择。
# 目前算法实现效果图
![image](https://github.com/user-attachments/assets/9e93cec0-ee5f-4a9d-a625-499f5d8e9f37)
![image](https://github.com/user-attachments/assets/740113a6-3839-4669-a8cc-24543b8bc953)
![image](https://github.com/user-attachments/assets/22546c12-5e20-4de2-863b-940477814da6)
![image](https://github.com/user-attachments/assets/1bc3ec76-82dd-44bc-ade7-065ab26b89b0)
![image](https://github.com/user-attachments/assets/fd405981-92e6-4057-b335-d2cc08b160d0)
![image](https://github.com/user-attachments/assets/2fb5ad51-0449-4771-9845-342975672f77)
![image](https://github.com/user-attachments/assets/45a7623a-9ed1-4d0f-aa24-0616fb95d9ef)
![image](https://github.com/user-attachments/assets/a24c6233-6506-4067-9610-7acfa174a3b8)
