# Notes
Class Projects and Notes

## FFMPEG 命令

### 抽帧
```linux
 ffmpeg -i Drone.mp4 -ss 00:00:00 -t 10 -r 5 -q:v 1 -f image2 pic-%03d.jpg
```
### 合成
```linux
 ffmpeg -threads 2 -y -r 5 -i pic-%03d.jpg  output.mp4
```
## SSD 学习笔记
### Permute（通道顺序交换）
Permute层就是交换的作用，比如你卷积后的维度是32×24×19×19，那么经过交换层后就变成32×19×19×24，顺序变了而已。

### Flatten（压扁）
而flatten层的作用就是将32×19×19×24变成32*8664，32是batchsize的大小。
