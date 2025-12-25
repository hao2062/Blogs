# Camera 系列（RK3568 & OV13850 等）

本系列从硬件到应用层逐步讲解 camera 视频流全流程，适合嵌入式工程师与内核驱动开发者。为便于阅读，文章按序号排列（文件名前缀用于保证排序）。

## 目录（按阅读顺序）

1. 系列导读与工程准备 — [01-系列导读与工程准备.md](01-系列导读与工程准备.md) — 系列目标、复现环境与硬件/软件清单。
2. 数据手册快速阅读 — [02-datasheet-快速阅读.md](02-datasheet-快速阅读.md) — 如何在 datasheet 中快速定位关键信息。
3. 原理图与硬件连线 — [03-原理图与硬件连线.md](03-原理图与硬件连线.md) — 引脚、电源序列与差分线布线要点。
4. MIPI D-PHY 与 CSI-2 基础 — [04-mipi-dphy-csi2基础.md](04-mipi-dphy-csi2基础.md) — LP/HS 模式、lane、时序与包结构。
5. 像素与 ISP 基础 — [05-像素与ISP基础.md](05-像素与ISP基础.md) — 像素阵列、Bayer、binning 与 3A 概念。
6. I2C/SCCB 与初始化流程 — [06-i2c-sccb初始化流程.md](06-i2c-sccb初始化流程.md) — 寄存器初始化与 OTP 校准加载。
7. Device Tree 与硬件描述 — [07-device-tree与硬件描述.md](07-device-tree与硬件描述.md) — sensor 节点与 endpoint 示例。
8. RK3568 摄像头控制器概览 — [08-rk3568-camctl概览.md](08-rk3568-camctl概览.md) — 控制器架构与常用设置要点。
9. V4L2 与 Media Framework — [09-v4l2与media-framework.md](09-v4l2与media-framework.md) — media graph、subdev 与 video 节点关系。
10. 驱动实现拆解 — [10-驱动实现拆解.md](10-驱动实现拆解.md) — probe、pad ops、fmt negotiation 与 s_stream 流程。
11. ISP 与调参 — [11-ISP与调参.md](11-ISP与调参.md) — RK 系列 ISP 流程与 tuning 方法。
12. 调试工具与排障实战 — [12-调试工具与排障实战.md](12-调试工具与排障实战.md) — 常用命令与示波器/抓包技巧。
13. 应用层示例：v4l2 与 GStreamer — [13-应用层示例-v4l2与GStreamer.md](13-应用层示例-v4l2与GStreamer.md) — 采集、显示与保存示例。
14. 多摄像头与切换 — [14-多摄像头与切换.md](14-多摄像头与切换.md) — 多摄像头拓扑、带宽管理与切换策略。
15. 案例：OV13850 端到端移植 — [15-案例-OV13850-端到端移植.md](15-案例-OV13850-端到端移植.md) — 从 datasheet 到用户态的完整实操案例。
16. 附录：寄存器表与常见问题 — [16-附录-寄存器表与常见问题.md](16-附录-寄存器表与常见问题.md) — 常用寄存器片段与快速排查清单。

每篇已包含：目标、前置条件、资源链接、步骤、关键命令、验证方法与排查要点。欢迎告诉我是否需要按平台（Android/Linux）或按读者水平再细分。
