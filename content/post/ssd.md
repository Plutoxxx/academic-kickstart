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
  focal_point: "Smart"
  preview_only: true
header:
  caption: ""
  image: ""
slides:
  theme: "black"  # Reveal JS theme name
  highlight_style: "dracula"  # Highlight JS theme name
---
SSD算法流程：
1.输入一幅图片，让图片经过卷积神经网络提取特征，并生成feature map.

