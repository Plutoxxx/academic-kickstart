---
title: SSD目标检测详解
summary: ssd是典型的Single Shot MultiBox Detector，运行速度与Faster R-CNN相比提升了很多
# View.
#   1 = List
#   2 = Compact
#   3 = Card
view: 2

# Optional header image (relative to `static/img/` folder).
image:
  focal_point: "Left"
  preview_only: false
header:
  caption: ""
  image: ""
---
##SSD算法流程：
###1.输入一幅图片，让图片经过卷积神经网络提取特征，并生成feature map.
###2.抽取其中6层的feature map，在每层feature map的每个像素点上生成default box.
###3.将生成的所有default box集合起来，全部丢到NMS(极大值抑制)中，输出筛选后的default box.

##损失函数
###包含三部分的loss：前景分类loss、背景分类loss、位置回归loss。
