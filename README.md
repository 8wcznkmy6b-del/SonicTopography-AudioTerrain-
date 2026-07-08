# 🌊 AudioTerrain (桌面音频地貌) for macOS

> **基于 Swift + Metal 开发的 macOS 原生 3D 实时动态音频地貌壁纸**。
> 本项目是对 Windows 端经典开源项目 [Sonic Topography](https://github.com/yin-yizhen/sonic-topography) 的 macOS 原生复刻与深度升级，专为 Apple Silicon 芯片（M1/M2/M3/M4 系列）进行了 GPU 硬件级性能极致优化。

---

## ✨ 核心特性 (Key Features)

- 🎵 **高保真免声卡系统内录**：基于 macOS `ScreenCaptureKit` 系统 API，无需安装 BlackHole 或 Loopback 等任何虚拟声卡，即可完美内录扬声器/耳机的所有音频，并完美支持系统音量键直接控制。
- ⚡ **多线程分离渲染 (CVDisplayLink)**：渲染回路完全移至后台专用硬件同步线程，即使进行系统重度操作，壁纸也永远保持满帧（30/60 FPS）丝滑运行，绝不卡顿。
- 🪄 **着色器级网格抗锯齿 (Shader AA)**：内置屏幕空间导数几何防闪烁算法（`fwidth`）与 4x MSAA 物理抗锯齿，网格线条边缘锐利平滑，旋转时无闪烁与摩尔纹。
- 🔋 **零能耗自动休眠模式 (Zero-Footprint)**：智能监听音频状态与系统锁屏。音乐暂停或系统锁屏时，渲染管线自动完全挂起，GPU 负载归零，极致省电。
- 🎛️ **原生联动控制面板**：使用原生 `NSPopover` 磨砂玻璃气泡窗口，支持 0.2 秒状态栏连击防抖、预设值与滑块双向智能联动微调。
- 🎨 **白平衡级色温微调**：色温调节与亮度彻底解耦，往左偏冷（赛博森林），往右偏暖（黄金时刻），提供 10 款精心调配的渐变色主题。
- 🌌 **丰富三维动效**：支持涟漪波纹（Ripple）、流星陨石（Meteor）、尘埃粒子（Particle）以及静默空闲起伏（Idle Wave）等多重动效自由组合。

---

## 📦 如何下载与安装

### 1. 下载正式版
1. 点击本仓库右侧的 **[Releases]** 区域。
2. 下载最新版本的 `SonicTopography-macOS.zip`。
3. 解压后将 `AudioTerrainMetal.app` 拖入您的 **应用程序 (Applications)** 文件夹。

### 2. 首次运行配置与授权
1. **屏幕录制权限**：由于系统 API 内录声音的机制，首次运行会弹出权限申请，请在 `系统设置 -> 隐私与安全性 -> 屏幕录制` 中为 `AudioTerrainMetal` 勾选授权并重启应用。
2. **麦克风权限**：用于备用的麦克风环境声音分析，首次弹窗时请点击允许。

---

## ⚙️ 技术栈 (Technology Stack)

- **语言**：Swift 6
- **图形 API**：Metal (Native GPU Pipeline / Instanced Rendering)
- **音频分析**：AVFoundation + Accelerate (vDSP FFT)
- **支持系统**：macOS 14.0+ (原生适配 Apple Silicon M 系列芯片)

---

## 📄 免责与许可说明 (License)

本项目仅用于学习、个人研究和壁纸美化。保留所有权利。
