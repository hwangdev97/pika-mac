# pika-mac

拍一下 MacBook，皮卡丘就会叫！

<video src="https://github.com/hwangdev97/pika-mac/releases/download/assets/export_1772268000098.mp4" controls width="300"></video>

利用 Apple Silicon 内置加速度计（Bosch BMI286 IMU）检测拍击，播放皮卡丘音效。需要 `sudo` 权限。

> 本项目灵感来源于 [taigrr/spank](https://github.com/taigrr/spank)，核心的加速度计读取与震动检测算法均来自该项目。pika-mac 将音效替换为皮卡丘主题，并新增了 battle / happy 模式。

## 使用

```bash
# 默认模式 — 随机皮卡丘叫声
sudo pika-mac

# 战斗模式 — 十万伏特！
sudo pika-mac --battle

# 开心模式 — 拍得越多越开心（5 分钟窗口内升级）
sudo pika-mac --happy
```

## 构建

```bash
go build -o pika-mac .
```

## 致谢

- [taigrr/spank](https://github.com/taigrr/spank) — 原始项目，提供了加速度计接入与震动检测的完整实现
- [taigrr/apple-silicon-accelerometer](https://github.com/taigrr/apple-silicon-accelerometer) — Apple Silicon 加速度计库
