# Single Shot MultiBox Detector Keras version.

SSD是一种Object Detection方法。本文是基于论文[SSD: Single Shot MultiBox Detector](http://arxiv.org/abs/1512.02325)，实现的keras版本。

> 该文章在既保证速度，又要保证精度的情况下，提出了SSD物体检测模型，与现在流行的检测模型一样，将检测过程整个成一个single deep neural network。便于训练与优化，同时提高检测速度。
> SSD将输出一系列离散化（discretization）的bounding boxes，这些bounding boxes是在不同层次（layers）上的feature maps上生成的，并且有着不同的aspect ratio。

## 模型效果
- 模型对载具的检测
<p align="center">
<img src="https://github.com/RussellCloud/SSD_keras/raw/master/source/Aeroplane.png" height="300">
</p>
<p align="center">
<img src="https://github.com/RussellCloud/SSD_keras/raw/master/source/Bicycle.png" height="300">
</p>

- 模型对动物的检测
<p align="center">
<img src="https://github.com/RussellCloud/SSD_keras/raw/master/source/Dog.png" height="300">
<img src="https://github.com/RussellCloud/SSD_keras/raw/master/source/Cat.png" height="300">
</p>


- 模型的视频检测
<p align="center">
<img src="https://github.com/RussellCloud/SSD_keras/raw/master/source/car.gif">
</p>

---

## 如何使用

### 所需依赖
```
cv2==3.3.0
keras==1.2.2
matplotlib==2.1.0
tensorflow==1.3.0
numpy==1.13.3
```
如果想跑通视频模块，则需额外`pip install scikit-video`

### 具体操作

在[RussellCloud](http://russellcloud.com)上新建名为`SSD_keras`的项目

```
git clone git@github.com:RussellCloud/SSD_keras.git
cd SSD_keras
russell init --name SSD_keras
russell run --mode jupyter --data 8a327f008d654293a02f496b791ccc56
```

- 对于图片的检测

参考SSD.ipynb

- 若要剪切图片为下一步处理做准备

参考SSD_crop.py

- 检测视频
```
cd video_utils
python videotest_example.py hy.mp4
```



---
参考资料

- [SSD: Single Shot MultiBox Detector](http://arxiv.org/abs/1512.02325)
- [论文阅读：SSD: Single Shot MultiBox Detector](http://blog.csdn.net/u010167269/article/details/52563573)
- [kuhung/SSD_keras](https://github.com/kuhung/SSD_keras)
- [rykov8/ssd_keras](https://github.com/rykov8/ssd_keras)
