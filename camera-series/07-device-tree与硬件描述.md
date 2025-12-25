# 07 Device Tree 与硬件描述

## 目标
给出 Device Tree 中 sensor 节点、ports/endpoint 配置、clocks 与 resets 的模板与示例。

## 示例片段

```
&cam0 {
    status = "okay";
    port@0 {
        camera_in: endpoint@0 {
            remote-endpoint = <&csi0_in 0>;
            reg = <0>;
        };
    };
};
```

## 验证
- `media-ctl` 查看 media graph
- `v4l2-ctl --list-formats-ext` 验证 formats
