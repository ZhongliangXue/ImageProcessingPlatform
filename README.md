## [图像处理云平台](https://github.com/ZhongliangXue/ImageProcessingPlatform/blob/master/%E9%A1%B9%E7%9B%AE%E5%BB%BA%E8%AE%AE%E4%B9%A6.md) web第三组
---
### 小组成员：谢成斌    薛忠良   商潇潇
---
### 任务分工安排：
* 谢成斌：负责前端页面的设计与实现，数据库的设计与实现，后端的工作
- 薛忠良：负责图像处理部分算法的设计与实现，规范算法的接口及说明文档，后端的工作
+ 商潇潇：前端页面的设计，需求分析，功能设计，单元测试与持续集成测试，大部分的文档整理工作

### 医学图像简介
主要涉及到的两种医学数据格式：[DICOM](https://www.dicomstandard.org/)和[NIfTY](https://brainder.org/2012/09/23/the-nifti-file-format/)
1. CT图像 <br>
![CT图像](https://github.com/ZhongliangXue/ImageProcessingPlatform/blob/master/images/CT.PNG)
2. PET_SUV图像
![PET图像](https://github.com/ZhongliangXue/ImageProcessingPlatform/blob/master/images/PET_SUV.PNG)
3. CT图像上的Ground Truth
![CT图像上的病灶](https://github.com/ZhongliangXue/ImageProcessingPlatform/blob/master/images/CT_Ground%20Truth.PNG)
4. PET图像上的Ground Truth
![PET图像上的病灶](https://github.com/ZhongliangXue/ImageProcessingPlatform/blob/master/images/PET_Ground%20Truth.PNG)

### 预期实现的网站为一个图像处理的平台，参考了[这个网站](http://www.niftynet.io/),我们的功能点：
1. 用户选择服务器上的一例医学数据（Nifti格式）后，前端展示改数据的切片数量和其他数据信息。 
   用户选择切片的序号，点击提交，服务端开始过分割(LRW)，分割结束后将分割的结果和病变 
   概率最大的一个区域传递到前端。
2. 用户上传服务器上的一张图片，进行图像的分割，最终分割结果为超像素的形式，传递到前端。
3. 用户选择服务器上的一张图片，点击提交后，将图片分割成前景和背景区域（类似于PS中的抠图），展示到前端。
4. 用户选择服务器上的一例医学数据，使用RW直接划分病变区域（分割速度很快，分割效果不如LRW）。
5. 用户选择一张含有文字的图片，点击提交后，服务端识别出图片中的文字，将文字传递到前端。
---

### 预期分割结果展示：
* 待分割普通图像 <br>
![普通图像](https://github.com/ZhongliangXue/ImageProcessingPlatform/blob/master/images/LD.jpg)

* 普通图像LRW分割结果 <br>
![分割结果图像](https://github.com/ZhongliangXue/ImageProcessingPlatform/blob/master/images/LD.bmp)

* 待分离普通图像 <br>
![普通图像](https://github.com/ZhongliangXue/ImageProcessingPlatform/blob/master/images/222.jpg)

* 普通图像前景与背景分离<br>
![前景与背景分离](https://github.com/ZhongliangXue/ImageProcessingPlatform/blob/master/images/result.PNG)

* 待分割PET <br>
![医学图像](https://github.com/ZhongliangXue/ImageProcessingPlatform/blob/master/images/P1-134.png)

* 病灶预测 <br>
![病灶预测](https://github.com/ZhongliangXue/ImageProcessingPlatform/blob/master/images/Top-134.bmp)


