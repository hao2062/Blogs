# 13 应用层示例：v4l2 与 GStreamer

## 目标
给出常见的用户层采集与显示/保存示例，包括 `v4l2` ioctl 示例和 `gst-launch-1.0` 管线。

## 示例
- 使用 `v4l2-ctl` 抓图
- `gst-launch-1.0 v4l2src ! videoscale ! videoconvert ! autovideosink`

## 性能测试
- 测量帧率、CPU 使用与带宽占用
