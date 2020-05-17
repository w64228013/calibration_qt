# 手眼标定软件

## 开发环境
+ Windows
+ Opencv 3.4
+ Qt 5.10.1
+ C++ 17


## 采集

可使用Kinect2.0摄像头，对标定板进行拍照。

## 相机标定

支持棋盘格标定板，手动设定棋盘格的角点数量。

![image](https://github.com/w64228013/calibration_qt/blob/master/calibration.gif)

## 畸变校正

![image](https://github.com/w64228013/calibration_qt/blob/master/calibration_res.gif)

## 坐标转换

根据相机标定步骤设定的`标定格尺寸`，求得图像坐标，在世界坐标系（棋盘坐标系）中的坐标。下图中，每张图都显示对应世界坐标系坐标轴。

![image](https://github.com/w64228013/calibration_qt/blob/master/calibration_convert.gif)


## 手眼标定

机械臂TCP坐标系Z轴与棋盘格垂直，给出三个基于Base坐标系的匹配点，即可求出基于2D的转换关系，即2D手眼标定。进而可以以图像坐标转换至机械臂坐标，实现手眼动作。

![image](https://github.com/w64228013/calibration_qt/blob/master/calibration_convert2.png)
