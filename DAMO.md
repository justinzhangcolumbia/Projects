# Notes
Class Projects and Notes

## FFMPEG 命令

### 抽帧
 ffmpeg -i Drone.mp4 -ss 00:00:00 -t 10 -r 5 -q:v 1 -f image2 pic-%03d.jpg
### 合成
 ffmpeg -threads 2 -y -r 5 -i pic-%03d.jpg  output.mp4
